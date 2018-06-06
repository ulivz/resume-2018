<template>
  <div class="gradient-background">
    <slot name="title"></slot>
  </div>
</template>

<script>
  export default  {}
</script>

<style lang="scss">
  .gradient-background {
    color: #fff;
    /*width: 100%;*/
    /*height: 100%;*/
    opacity: 0.8;
    background: linear-gradient(135deg,
      #ED5564 0%,
    #FB6E52 10%,
    #FFCE55 20%,
    #A0D468 30%,
    #48CFAE 50%,
    #4FC0E8 60%,
    #5D9CEC 70%,
    #AC92ED 80%,
    #EC87BF 90%,
    #ED5564 100%

      /*#5073B8 0%,*/
      /*#13a793 10%,*/
      /*#07B39B 20%,*/
      /*#6DBA82 30%,*/
      /*#F37055 50%,*/
      /*#EF4E7B 60%,*/
      /*#C55B95 70%,*/
      /*#A166AB 80%,*/
      /*#A166AB 90%,*/
      /*#5073B8 100%*/
    ) center / cover;

    background-size: 800% 800%;
    animation: AnimationName 30s ease infinite;
  }

  @keyframes AnimationName {
    0% {
      background-position: 0% 50%
    }
    50% {
      background-position: 100% 50%
    }
    100% {
      background-position: 0% 50%
    }
  }
</style>



