<template>
  
    <el-row type="flex" class="row-bg" justify="center" align="middle">
      <!-- col列 这个插件里面分成了24格 el-col布局组件列组件 span是当前列所占的格数 -->
      <el-col  :xs="14" :sm="12" :md="10" :lg="8" :xl="6">
        <el-form ref="form" :model="form"  class="loginForm" label-position="top" label-width="80px">
          <el-form-item label="用户名">
            <el-input v-model="form.username"></el-input>
          </el-form-item>
          <el-form-item label="密码">
            <el-input v-model="form.password"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="primary" @click="onSubmit">登录</el-button>
            <el-button>重置</el-button>
          </el-form-item>
        </el-form>
      </el-col>
    </el-row>
  
</template>
<script>
export default {
  data() {
    return {
      form: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    }
  }
};
</script>
<style>
  .row-bg {
    height: 100%;
    background-color: #2d434C;
  }
  .loginForm {
    background-color: #fff;
    border-radius: 10px;
    padding: 30px 20px;
    min-width: 400px;
  }
</style>

