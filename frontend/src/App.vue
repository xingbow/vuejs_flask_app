<template>
  <div id="app" style="width: 100%">
    <el-container>
      <el-header id="systemHeader">System Name</el-header>
      <el-main id="systemMain">
         <el-row>
            <el-col :span="8" style="padding:2px;">
              <ControlPanel />
            </el-col>
            <el-col :span="16" style="padding:2px;">
              <MainView />
            </el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script>
/* global d3 $ _ */
import ControlPanel from "./components/ControlPanel/ControlPanel.vue"
import MainView from "./components/MainView/MainView.vue"

export default {
  name: "app",
  components: {
    ControlPanel,
    MainView
  },
  data() {
    return {

    };
  },
  watch: {
  },
  mounted: function () {
    console.log("d3: ", d3); /* eslint-disable-line */
    console.log("$: ", $); /* eslint-disable-line */
    console.log("this: ", this, this.components);
    console.log(
      "_",
      _.partition([1, 2, 3, 4], (n) => n % 2)
    ); /* eslint-disable-line */
  },
  methods: {

  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  margin: 0 auto;
}

#systemHeader {
  background-color: #2c3e50;
  color: white;
  text-align: start;
  font-weight: bold;
  font-size: 25px;
  line-height: 60px;
}

#systemMain {
  padding: 5px;
  /* background-color: #E9EEF3; */
  color: #333;
  text-align: center;
  height: 700px;
}

.viewheader {
  font-weight: bold;
  text-align: start;
  padding: 5px;
  background: #e5e9f2;
}

.viewbody {
  height: 610px;
}

</style>
