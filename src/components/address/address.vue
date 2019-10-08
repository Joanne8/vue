<template>
  <div class="address-box border-1px" v-if="seller.infos">
    <span class="addrIcon"></span>
    <div class="addrText">
      <div class="addr">{{seller.infos[2]}}</div>
      <div class="addrLine">{{seller.infos[3]}}</div>
    </div>
    <div class="telPhone">
      <img src="./phone.png" alt="">
      <a :href="'tel:'+seller.telephone" class="contact">联系商家</a>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props: {
      seller: {
        type: Object
      }
    }
  };
</script>


<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixin";

  .address-box
    display:flex
    justify-content: space-between
    padding-bottom:12px
    margin: 12px 12px 0
    border-1px(rgba(7, 17, 27, 0.1))
    .addrIcon
      display: inline-block
      vertical-align: top
      width: 16px
      height: 16px
      bg-image('addr')
      background-size: contain
      background-repeat: no-repeat
      opacity: 0.7
    .addrText
      line-height: 20px
      border-right: 1px solid rgba(7,17,27,0.1)
      padding-right: 10px
      .addr
        color: #522C0F
        font-size: 16px
        overflow: hidden
        text-overflow: ellipsis
        white-space: nowrap
        width: 254px
      .addrLine
        color: #999
        font-size: 12px;
    .telPhone
      img
        width: 20px
        height: 20px
        margin: 0 auto 3px
        display: block
      .contact
        font-size: 10px
        color: #999
</style>
