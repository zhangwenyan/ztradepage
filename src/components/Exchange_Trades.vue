<template>
  <div class="d">
    <table border="1">
      <tr>
        <td style="height:30px;">
          <ul class="nav nav-tabs">
            <li class="nav-item">
              <a
                @click="tabIndex = 0"
                :class="['nav-link', tabIndex == 0 && 'active']"
                href="javascript:;"
              >
                交易
              </a>
            </li>

            <li class="nav-item">
              <a
                @click="tabIndex = 1"
                :class="['nav-link', tabIndex == 1 && 'active']"
                href="javascript:;"
              >
                账号设置
              </a>
            </li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
            <table v-if="tabIndex==0" border="1" >
                <tr>
                    <td>
                         <Etrade />
                    </td>
                    <td>
                         <Etrade />
                    </td>
                </tr>
            </table>

            <Eaccountsetting v-if="tabIndex==1" />
         
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import Etrade from "@/components/Exchange_Trade";
import Eaccountsetting from "@/components/Exchange_AccountSetting"
export default {
  name: "Exchange_Trades",
  components: {
    Etrade,Eaccountsetting
  },
  data() {
    return {
      tabIndex: 0
    };
  }
};
</script>
<style lang="less" scoped>
.d {
  height: 100%;
  background-color: aqua;
}
table {
  height: 100%;
  width: 100%;
}
</style>


