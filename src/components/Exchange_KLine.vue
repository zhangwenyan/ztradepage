<template>
  <div class="d">
      <iframe v-bind:src="'./static/aicoin.html?symbol='+symboltrue+'&trader='+tradertrue" />
  </div>
</template>

<script>
export default {
  name: "Exchange_KLine",
  props: ["trader", "symbol"],
  data() {
    return {
      tradertrue: null,
      symboltrue: null
    };
  },
  created: function() {
    var symboltrue = this.symbol;
    var tradertrue = this.trader;
    if (this.trader == "bitfinex") {
      if (this.symbol.endsWith("usdt")) {
        symboltrue = this.symbol.substr(0, this.symbol.length - 1);
      }
      if (this.symbol.startsWith("iota")) {
        symboltrue = this.symbol.replace("iota", "iot");
      }
    }

    if (this.trader == "gate2") {
      tradertrue = "gate";
    }

    this.symboltrue = symboltrue;
    this.tradertrue = tradertrue;
  }
};
</script>

<style lang="less" scoped>
.d {
  height: 100%;
  position: relative;
  
  iframe{
    position: absolute;
    right:0px;
    width:100%;
    height:100%;
    bottom:0px;
    overflow-y: scroll;
  }

  border:3px solid green;



}

</style>


