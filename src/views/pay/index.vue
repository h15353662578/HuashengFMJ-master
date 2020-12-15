<template>
  <div class="app-init pay-page scroll-box">
    <header-back title="pay"></header-back>

    <div>
      <img src="https://s3.ax1x.com/2020/12/15/rKNI9e.jpg" />
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import headerBack from "../../components/header-back";

export default {
  name: "pay",
  components: {
    headerBack,
  },
};
</script>

<style type="text/sass" lang="sass">
.pay-page
  background-color: #fff
  .padding-box
    padding: 0.4rem
    color: #333
    .color
      color: orange
      ul
        padding-left: 0.8rem
      li
        list-style: disc
</style>
