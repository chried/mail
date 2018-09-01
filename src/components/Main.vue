<template>
  <div class="main">
      <Header></Header>
      <div class="content">
         <el-row :gutter="20">
            <el-col :span="8">
              
              <div class="content-one">
                <h3 class="one-title">实时军事</h3>
                <hr>
                <h5 class="source">来源：网易</h5>
                <ul>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                  <li><a href="#">今晚我们要吃饭</a></li>
                </ul>
                 <hr>
                <h5>来源：腾讯</h5>
                 <ul>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                 </ul>
                   <hr>
                <h5>来源：新浪</h5>
                 <ul>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                  <li><a>今晚我们要吃饭</a></li>
                </ul>
              </div>

            </el-col>
            <el-col :span="8"> 
              <div class="content-two">
                   <h3>今日推荐</h3>
                <hr>
                <ul>
                  <li class="today-hot"><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                  <li><a>今晚明晚我们都要吃饭</a></li>
                </ul>
              </div>
            </el-col>
            <el-col :span="8">
               <div class="content-three">
                    <h3>热门原创</h3>
                <el-row>
                  <el-col :span="24" v-for="(o, index) in 2" :key="o" :style="card_style">
                    <el-card :body-style="{ padding: '0px' }" shadow="hover">
                      <img src="http://element-cn.eleme.io/static/hamburger.50e4091.png" class="image">
                      <div style="padding: 8px;">
                        <span>好吃的汉堡</span>
                        <div class="bottom clearfix">
                          <time class="time">{{ currentDate }}</time>
                          <el-button type="text" class="button">操作按钮</el-button>
                        </div>
                      </div>
                    </el-card>
                  </el-col>
                </el-row>
              </div>
            </el-col>
        </el-row>
      </div>
      <div class="content-important">
         <!--下页菜单导航-->
          <div class="content-left-menu">
            <ul>
              <li><a @mouseenter="overShow" @mouseleave="outHide" href="#">历史长河</a></li>
              <li><a href="#">老兵永存</a></li>
              <li><a href="#">传播正能量</a></li>
            </ul>           
          </div>
        <div class="content" style="height:1200px;display:inline-block;margin-top:20px;margin-bottom:20px;">
         
          <slot name="history"></slot>

        </div>
      </div>
  </div>
</template>

<script>
import Header from "@/components/pages/Header";
import energy from "@/components/important/energy";
import history from "@/components/important/history";
import veteran from "@/components/important/veteran";

export default {
  data() {
    return {
      activeName: "first",
      card_style: {
        "margin-bottom": "20px",
        "padding-right": "15px"
      },
      currentDate: new Date()
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    },
    overShow() {
      console.log("show");
    },
    outHide() {
      console.log("hide");
    }
  },
  components: { Header, energy, history, veteran }
};
</script>

<style scoped lang="less">
.main {
  width: 100%;
  min-width: 800px;
}
.content {
  margin: 0 auto;
  width: 1120px;
  border: 1px solid #ebebeb;
  border-radius: 3px;
  transition: 0.2s;
  margin-top: 50px;
  overflow: hidden;
}
.content:hover {
  box-shadow: 0 0 8px 0 rgba(232, 237, 250, 0.6),
    0 2px 4px 0 rgba(232, 237, 250, 0.5);
}
.content-one {
  padding-left: 20px;
  font-weight: 500;

  .one-title {
    color: #d63333;
  }
  .source {
    color: #888;
  }
  ul {
    list-style: none;
    padding: 0;

    li {
      a {
        display: inline-block;
        height: 30px;
        line-height: 30px;
        text-decoration: none;
        color: #333;
        &:hover {
          color: #409eff;
        }
      }
    }
  }
}
.content-two {
  ul {
    list-style: none;
    padding: 0;
    line-height: 30px;

    li {
      &.today-hot {
        font-weight: bold;
        a {
          font-size: 19px;
        }
      }
      a {
        font-size: 17px;
        color: #404040;
        margin-bottom: 5px;
        display: inline-block;
        width: 100%;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
        vertical-align: middle;
        &:hover {
          color: #409eff;
        }
        cursor: pointer;
      }
    }
  }
}
.content-three {
  .image {
    display: inline-block;
    width: 100%;
    height: 140px;
  }
}
.content-important {
  margin: 0 auto;
  width: 1360px;
  position: relative;
}
.content-left-menu {
  position: sticky;
  display: inline-block;
  margin-top: 20px;
  width: 120px;
  float: left;
  left: 0;
  top: 20px;

  ul {
    list-style: none;
    margin: 0;
    padding: 0;

    li {
      height: 50px;
      margin-bottom: 3px;
      padding-right: 10px;
      line-height: 50px;
      font-size: 16px;
      text-align: center;
      color: #000;
      border-radius: 5px;
      overflow: hidden;
      &.active {
        a {
          display: block;
          background: #d52b2b;
          color: #fff;
        }
      }
      a {
        color: #555;
        text-decoration: none;

        &:hover {
          display: block;
          background: #d52b2b;
          color: #fff;
        }
      }
    }
  }
}
</style>
