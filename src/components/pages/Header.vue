<template>
    <div class="header">
      <div class="header-main">
          <div class="logo header-float-left">
            <a class="logo-a">
              <img src="">
            </a>
          </div>
           <div class="login header-float-right">
              <div class="in-login" v-if="isLogin">

              </div>
              <div class="not-login" v-if="!isLogin">
                <a href="#">登陆</a>
                <a href="#">注册</a>
              </div>
          </div>
          <div class="search header-float-right">
              <el-input placeholder="请输入内容" v-model="input5" class="input-with-select">
                <el-button slot="append" icon="el-icon-search"></el-button>
              </el-input>
          </div>
          <div class="menu header-float-right">
              <ul>
                <li><a>首页</a></li>
                <li><a>菜单1</a></li>
                <li><a>菜单2</a></li>
                <li><a>菜单3</a></li>
              </ul>
          </div>
          
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      isLogin: false
    };
  }
};
</script>

<style scoped lang="less">
.header-float-left {
  float: left;
  margin-right: 20px;
}

.header-float-right {
  float: right;
  margin-right: 20px;
}

.header {
  width: 100%;
  height: auto;
}

.header-main {
  margin: 0 auto;
  width: 1120px;
  height: 50px;
  box-shadow: 2px 2px 2px #e9eef3;
}
.logo {
  a {
    display: inline-block;
    text-decoration: none;
    width: 50px;
    height: 50px;
  }
}

.menu {
  height: 50px;
  width: 460px;
  color: #888;
  line-height: 50px;
  ul {
    list-style: none;
    margin: 0;

    li a {
      display: block;
      float: left;
      width: 80px;
      text-align: center;
      margin: 0 10px;
      cursor: pointer;
    }
    li a:hover {
      background-color: #555;
      color: white;
    }
  }
}
.login {
  height: 50px;
  width: 120px;
  text-align: center;
  line-height: 50px;

  a {
    text-decoration: none;
    font-size: 14px;
    color: #888;
    padding: 0 12px;
  }
  a:hover {
    color: #555;
  }
}
.search {
  height: 50px;
  width: 220px;
  line-height: 50px;
}
</style>
