<template>
  <div class="info-item">
    <span class="menu-icon">
      <div v-for="i in [0,1,2]" :key=i class="h-bar"></div>
    </span>

    <div class="icon">
      <img :src="icon">
    </div>
    <div class="info-col">
      <div class="main">{{main}}</div>
      <div class="sub">{{sub}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfoItem',
  props: {
    icon: String,
    main: String,
    sub: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.menu-icon {
  position: absolute;
  top: 5px;
  right: 10px;
  .h-bar {
    width: 20px;
    height: 2px;
    background-color: rgb(203, 203, 203);
    margin-top: 2px;
  }
}
.info-item {
  position: relative;
  text-align: left;
  margin: 10px;

  padding: 7px;
  background-color: #ffffff;
  border-radius: 5px;
  box-shadow: #b1b1b1 1px 1px 5px;
}

.icon {
  margin-right: 10px;
  padding-top: 14px;
  float: left;
  img {
    width: 40px;
    height: 40px;
  }
}

.info-col {
}
.main {
  font-size: 30px;
  color: black;
  text-shadow: #9a9a9a 0px 1px 2px;
}

.sub {
  font-size: 20px;
  color: rgb(134, 134, 134);
}

</style>
