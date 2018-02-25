<template>
  <div id="app">
    <div v-if="!authorized" class="authorization">
      <div class="placeholder">Please enter the passcode:</div>
      <input v-model="passcode" type="password">
      <button @click="auth">Go</button>
    </div>
    <!--<div @click="downloadPdf">Download PDF</div>-->
    <div v-if="authorized" class="resume markdown-body" v-html="html"></div>
  </div>
</template>

<script>
  function helperTpl(className, content) {
    return `<p class="${className}">${content.slice(5).trim()}</p>`
  }

  import source from './markdown/default.md'
  import marked, { Renderer } from 'marked'
  import hljs from 'highlight.js'
  //  import html2pdf from 'html2pdf.js'
  import 'highlight.js/styles/github.css'
  import 'github-markdown-css'
  import './theme/default.scss'
  export default {
    name: 'app',
    data () {
      return {
        source,
        authorized: false,
        passcode: '',
        html: '',
        msg: 'Welcome to Your Vue.js App'
      }
    },
    methods: {
      auth() {
        if (this.passcode === '949494') {
          this.authorized = true
          this.render()
          localStorage.setItem('auth', true)
        }
      },
      render() {
        const renderer = new Renderer()

        renderer.paragraph = function (text) {
          if (/^!&gt;/.test(text)) {
            return helperTpl('tip', text)
          } else if (/^\?&gt;/.test(text)) {
            return helperTpl('warn', text)
          }
          return `<p>${text}</p>`
        }

        marked.setOptions({
          renderer,
          highlight: function (code) {
            return hljs.highlightAuto(code).value;
          }
        });

        this.html = marked(source);
      }
//      downloadPdf() {
//        const dom = document.querySelector('.resume.markdown-body')
//        const pdf = html2pdf(dom, {
//          margin: 1,
//          filename: 'ulivz-resume.pdf',
//          image: { type: 'jpeg', quality: 1 },
//          html2canvas: { dpi: 300, letterRendering: true },
//          jsPDF: {
//            unit: 'in',
//            format: 'letter',
//            orientation: 'portrait',
//            activeFontKey: '-apple-system'
//          }
//        })
//      }
    },
    mounted() {
//       Create your custom renderer.
      let auth = localStorage.getItem('auth')
      console.log(auth)
      if (auth === 'true') {
        this.authorized = true
        this.render()
      }

      if (!this.authorized) {
        document.addEventListener('keyup', event => {
          if (event.keyCode === 13) {
            this.auth()
          }
        })
      }
    }
  }
</script>

<style>
  html body {
    outline: 0;
    border: 0;
    padding: 0;
    margin: 0;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
  }

  .authorization {
    color: #333;
    width: 300px;
    margin: calc(50vh - 20px) auto 0;
  }

  .authorization .placeholder {
    font-size: 16px;
    margin-bottom: 10px;
    color: #666;
  }

  .authorization input {
    box-sizing: border-box;
    appearance: none;
    border-radius: 5px;
    width: 100%;
    height: 40px;
    font-size: 20px;
    text-indent: 10px;
    border: 2px solid #ccc;
  }

  .authorization button {
    float: right;
    width: 40px;
    margin-top: 10px;
  }

  .markdown-body {
    box-sizing: border-box;
    min-width: 200px;
    max-width: 980px;
    margin: 0 auto;
    padding: 45px;
  }

  @media (max-width: 767px) {
    .markdown-body {
      padding: 15px;
    }
  }

  .markdown-body pre code {
    white-space: pre-wrap;
    word-wrap: break-word;
  }
</style>
