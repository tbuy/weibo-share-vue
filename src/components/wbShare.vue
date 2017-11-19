<template>
  <div class="c_wbShare" :style="{width: countWidth + 'px',height: countWidth + 'px'}"></div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  props: {
    width: {
      type: Number,
      defalut: 50
    },
    appkey: {
      type: Number,
      require: true
    },
    text: {
      type: String,
      defalut: '分享'
    },
    pic: {
      type: String,
      defalut: ''
    },
  },
  computed:{
    countWidth(){
      if(this.width > 50){
        return 50
      }else{
        return this.width;
      }
    }
  },
  mounted: function() {
    document.querySelector('html').setAttribute("xmlns:wb", "http://open.weibo.com/wb");
    var wb = document.createElement("wb:share-button");
    var st = document.createElement("script");
    wb.setAttribute("appkey", this.appkey);
    wb.setAttribute("addition", "simple");
    wb.setAttribute("type", "icon");
    wb.setAttribute("default_text", this.text);
    wb.setAttribute("pic",this.pic );
    st.src = "http://tjs.sjs.sinajs.cn/open/api/js/wb.js";
    st.type = "text/javascript";
    st.charset = "utf-8";
    document.querySelector('.c_wbShare').appendChild(wb);
    document.querySelector('head').appendChild(st);

  }
}
</script>

<style>
.c_wbShare {
   border-radius: 5%;
  overflow: hidden;
  position: relative;
}

iframe {
  transform: scale(6);
  opacity: 0;
}

.c_wbShare::after {
  pointer-events: none;
  content: '';
  display: block;
  width: 100%;
  height: 100%;
  background-image: url(../assets/big.png);
  background-size: cover;
  position: absolute;
  top: 0;
  left: 0;
}
</style>
