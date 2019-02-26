<template>
  <div class="d">
    <table>
      <tr>
        <td>
          <exchange />
        </td>
      </tr>
    </table>

  </div>
</template>

<script>
import Exchange from "@/components/Exchange";

export default {
  name: "App",
  components: {
    Exchange
  }
};
</script>
<style lang="less" scoped>
.d {
  background-color: green;
  height: 100%;
}
table {
  border: 1px solid orange;
  width: 100%;
  height: 100%;
}
</style>

