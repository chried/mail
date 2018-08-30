<template>
  <div class="main">
      <Header></Header>
      <div class="content">
         <el-row :gutter="20">
            <el-col :span="8">
              
              <div class="content-one">
                <h3>实时军事</h3>
                <hr>
                <h5>来源：网易</h5>
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
              </div>
            </el-col>
            <el-col :span="8">
               <div class="content-three">
                    <h3>热门原创</h3>
                <el-row>
                  <el-col :span="24" v-for="(o, index) in 2" :key="o" :style="card_style">
                    <el-card :body-style="{ padding: '0px' }">
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
  </div>
</template>

<script>
import Header from "@/components/pages/Header";

export default {
  data() {
    return {
      activeName: "first",
      card_style: {
        "margin-bottom": "20px"
      }
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  },
  components: { Header }
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
  margin-bottom: 30px;
}
.content:hover {
  box-shadow: 0 0 8px 0 rgba(232, 237, 250, 0.6),
    0 2px 4px 0 rgba(232, 237, 250, 0.5);
}
.content-one {
  padding-left: 20px;
}
.content-three {
  .image {
    display: inline-block;
    width: 100%;
    height: 140px;
  }
}
</style>
