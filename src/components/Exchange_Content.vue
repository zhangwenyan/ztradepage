<template>
  <div class="d">
    <table border="1">
      <tr style="height:30px;">
        <td>
          <ul class="nav nav-tabs">
            <li class="nav-item">
              <a
                @click="tabIndex = 0"
                :class="['nav-link', tabIndex == 0 && 'active']"
                href="javascript:;"
              >
                K线
              </a>
            </li>

            <li class="nav-item">
              <a
                @click="tabIndex = 1"
                :class="['nav-link', tabIndex == 1 && 'active']"
                href="javascript:;"
              >
                深度
              </a>
            </li>

            <li class="nav-item">
              <a
                @click="tabIndex = 2"
                :class="['nav-link', tabIndex == 2 && 'active']"
                href="javascript:;"
              >
                市场
              </a>
            </li>

            <li class="nav-item">
              <a
                @click="tabIndex = 3"
                :class="['nav-link', tabIndex == 3 && 'active']"
                href="javascript:;"
              >
                工具
              </a>
            </li>
          </ul>
        </td>
      </tr>

      <tr>
        <td class="dd">
          <Ekline v-if="tabIndex == 0" />
          <Edeps v-if="tabIndex == 1" />
          <Emarket v-if="tabIndex == 2" />
          <Etools v-if="tabIndex == 3" />
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import Ekline from "@/components/Exchange_KLine";
import Etools from "@/components/Exchange_Tools";
import Edeps from "@/components/Exchange_Deps";
import Emarket from "@/components/Exchange_Market";
export default {
  name: "Exchange_Content",
  components: {
    Ekline,
    Etools,
    Edeps,
    Emarket
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
  background-color: white;
}
table {
  height: 100%;
  width: 100%;
  .dd{

  }

}
</style>


