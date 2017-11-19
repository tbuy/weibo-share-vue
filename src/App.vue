<template>
  <div id="app">
      <div class="demo">
        <wbShare :appkey="appkey" :width="width" :pic="pic" :text="text"></wbShare>
      </div>
  </div>
</template>

<script>
import wbShare from './components/wbShare'

export default {
  components: {
    wbShare
  },
  data() {
    return {
      appkey: 0,
      width: 30,
      text: 'hello',
      pic: 'http%3A%2F%2Ftvax2.sinaimg.cn%2Fcrop.0.0.750.750.50%2F68ce947fly8fh4nk5rh4vj20ku0kuq48.jpg||https://wx4.sinaimg.cn/thumb150/68ce947fly1fkbjtosvulj21jk222alm.jpg'
    }
  },

}
</script>

<style>

</style>
