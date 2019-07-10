<template>
  <div class="container">
    <h1>首页</h1>
    <div>
      <span
        v-for="(v,i) in ['娱乐','体育','军事']"
        :key="i"
        @click="switchs=i"
        :class="{color:switchs===i}"
      >{{v}}</span>
    </div>
    <div v-if="switchs===0">
      <ul>
        <li>华哥和某某女明星结婚了!</li>
        <li>华哥和某某女明星结婚了!</li>
        <li>华哥和某某女明星结婚了!</li>
        <li>华哥和某某女明星结婚了!</li>
      </ul>
    </div>
    <div v-if="switchs===1">
      <ul>
        <li>方泽彬带领中国男足闯进世界杯决赛!</li>
        <li>方泽彬带领中国男足闯进世界杯决赛!</li>
        <li>方泽彬带领中国男足闯进世界杯决赛!</li>
        <li>方泽彬带领中国男足闯进世界杯决赛!</li>
      </ul>
    </div>
    <div v-if="switchs===2">
      <ul>
        <li>台湾成功收复!</li>
        <li>台湾成功收复!</li>
        <li>台湾成功收复!</li>
        <li>台湾成功收复!</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  // data是个函数 返回值是个对象
  data() {
    return {
      switchs: ""
    };
  }
};
</script>

<style scoped lang="less">
.container {
  width: 400px;
  height: 400px;
  background-color: pink;
  margin: 0 auto;
  text-align: center;
  .microcheiria {
    cursor: pointer;
  }
  .color {
    color: red;
  }
}
</style>
