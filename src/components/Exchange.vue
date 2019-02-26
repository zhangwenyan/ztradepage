<template>
  <div class="d">
    <table border="1">
      <tr style="height:30px;">
        <td>
          <ehead />
        </td>
      </tr>
      <tr>
        <td style="background-color:red;">
          <table border="1">
            <tr style="height:20px;">
              <td>
                  <table border="1">
                      <tr>
                          <econtent/>
                      </tr>
                      <tr style="height:200px;">
                          <td>
                              <eorders/>
                          </td>
                      </tr>
                  </table>
                
              </td>
              <td style="width:450px">
                <table border="1">
                  <tr>
                    <td>
                        <table>
                            <tr>
                                <td>
                                    <edep />
                                </td>
                                <td style="width:240px;">
                                    <edetails/>
                                </td>
                            </tr>
                        </table>
                      
                    </td>
                  </tr>
                  <tr style="height:260px;">
                    <td>
                      <etrades />
                    </td>
                  </tr>
                </table>
              </td>
            </tr>
          </table>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import Ehead from "@/components/Exchange_Head";
import Edep from "@/components/Exchange_Dep";
import Etrades from "@/components/Exchange_Trades";
import Econtent from "@/components/Exchange_Content";
import Eorders from "@/components/Exchange_Orders";
import Edetails from "@/components/Exchange_Details";
export default {
  name: "Exchange",
  components: {
    Ehead,
    Edep,
    Etrades,
    Econtent,
    Eorders,
    Edetails
  }
};
</script>

<style lang="less" scoped>
.d {
  height: 100%;
}
table {
  width: 100%;
  height: 100%;
}
</style>


