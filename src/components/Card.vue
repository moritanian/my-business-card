<template>
  <div class="card">
    <span class="menu-icon">
      <div v-for="i in [0,1,2]" :key=i class="h-bar"></div>
    </span>
    <div class="header">
      <div class="title">
        <div>Graduate School of Information Science and Technology,</div>
        <div>The University of Tokyo</div>
      </div>
    </div>
    <div class="main">
      <div class="name">
        Masahiro Morita
      </div>
      <div class="belongs">
        Kawahara Lab
      </div>
      <div class="location">
        <svg class="octicon octicon-location" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M6 0C2.69 0 0 2.5 0 5.5 0 10.02 6 16 6 16s6-5.98 6-10.5C12 2.5 9.31 0 6 0zm0 14.55C4.14 12.52 1 8.44 1 5.5 1 3.02 3.25 1 6 1c1.34 0 2.61.48 3.56 1.36.92.86 1.44 1.97 1.44 3.14 0 2.94-3.14 7.02-5 9.05zM8 5.5c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"></path></svg>
        <span class="location-name">Tokyo</span>
      </div>

    </div>
    <div class="info">
      <InfoItem
        :icon="PhoneImage"
        main='+81-80-2332-7141'
        sub='Mobile'
      />
       <InfoItem
        :icon="EmailImage"
        main='morita@akg.t.u-tokyo.ac.jp'
        sub='Mail'
      />
       <InfoItem
        :icon="GithubImage"
        main='https://github.com/moritanian'
        sub='Github'
      />
      <div class="footer">
        <div>Faculty of Engineering Building 2 112C1</div>
        <div>7-3-1 Hongo, Bunkyo-ku, Tokyo 113-8656</div>
        <div>Japan</div>

      </div>
    </div>
  </div>
</template>

<script>
import EmailImage from "@/assets/email.svg";
import PhoneImage from "@/assets/phone.svg";
import GithubImage from "@/assets/GitHub-Mark-120px-plus.png";
import InfoItem from './InfoItem.vue';
export default {
  name: 'Card',
  data () {
    return {
      EmailImage, PhoneImage, GithubImage
    }
  },
  components: {
    InfoItem
  },
  props: {
  },
  created () {
    // console.log(EmailImage);
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  width: 100%;
  height: 76px;
  font-size: 17px;
  background-color: #696b00;
  color: white;
  .title {
    padding: 15px 2px 10px 55px;
  }
}

.menu-icon {
  position: absolute;
  top: 20px;
  left: 20px;
  .h-bar {
    width: 20px;
    height: 2px;
    background-color: white;
    margin-top: 3px;
  }
}
.main {
  position: relative;
  height: 420px;
  background-color: #ffffff;
  border-radius: 5px;
  margin: 8px;
  box-shadow: #b1b1b1 1px 1px 5px;

  .name {
    padding-top: 150px;
    font-size: 56px;
    color: #696b00;
    text-shadow: #9a9a9a 0px 1px 3px;
    font-weight: bold;
    text-align: center;
  }
  .belongs {
    color: rgb(117, 117, 117);
    font-size: 25px;
    text-align: right;
    padding-right: 25px;
  }
  .location {
    position: absolute;
    bottom: 10px;
    left: 10px;
    font-size: 18px;
    .octicon {
      width: 22px;
      height: 22px;
      top: 4px;
      position: relative;
    }
    .location-name {
      margin-left: 2px;
    }
  }
}

.info {
  width: 100%;
}

.footer {
  border-top: solid rgb(166, 166, 166) 1px;
  margin-left: 12px;
  margin-right: 12px;
  padding-top: 8px;
  font-size: 19px;
  width: 526px;
  height: 70px;
  color: white;
  position: absolute;
  bottom: 0;
  color: black;
  line-height: 20px;
  text-align: right;
}

</style>
