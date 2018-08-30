<template>
    <div class="header">
      <div class="header-main">
          <div class="logo header-float-left">
            <a class="logo-a">
              <img src="">
            </a>
          </div>
          <div class="menu header-float-left">
              <ul>
                <li>首页</li>
                <li>菜单1</li>
                <li>菜单2</li>
                <li>菜单3</li>
              </ul>
          </div>
          <div class="search header-float-left">

          </div>
          <div class="login header-float-left">
          </div>
      </div>
    </div>
</template>

<script>
export default {};
</script>

<style scoped lang="less">
.header-float-left {
  float: left;
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

  ul {
    list-style: none;

    li {
      float: left;
      width: 50px;
      margin: 0 10px;
      height: 50px;
      line-height: 50px;
      cursor: pointer;
    }
  }
}
</style>
