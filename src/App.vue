<template>
  <el-container>
      <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b">
        <el-menu-item index="1">Home</el-menu-item>
        <el-menu-item index="2">Blog</el-menu-item>
        <el-menu-item index="3">Contact</el-menu-item>
      </el-menu>
    <el-main>
    <div>
    <p>Add a link below and check if it's fake news:</p>
    </div>
    <div>
      <el-input placeholder="Add a link here" v-model="input1">
      </el-input>
      <el-button icon="el-icon-search"></el-button>
    </div>
    </el-main>
  </el-container>
</template>

<script>
export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1',
        input1: ''
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>


<style>
:root {
  background-color: #e4e7ed;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #e4e7ed;
}
.logo {
  width: 50%;
}
.btn {
  margin-top: 100px;
}

.el-menu-demo {
  position: absolute;
  margin-top: -8px;
  margin-left: -8px;
  width: 100%;
}
.el-select .el-input {
    width: 110px;
  }
.input-with-select .el-input-group__prepend {
    background-color: #fff;
}
.el-input__inner {
width: 80%;   
}
.el-button {
position: absolute;
margin-left: -130px;
}

.el-main {
margin-top: 90px;
}
</style>
