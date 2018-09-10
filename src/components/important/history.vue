<template>
    <div class="history">
       <el-row>
            <el-col :span="8">
                <div class="energy-list">

                  <h3>推荐</h3>

                    <ul>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                        <li><a href="#">(历史)明天我们还是要吃饭的哦</a></li>
                    </ul>
                </div>
            </el-col>
            <el-col :span="16">
                <div class="energy-vedio">
                  <h3>视频专区</h3>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style scoped lang="less">
.history {
  padding: 5px 5px;
  width: 100%;
}
.energy-list {
  h3 {
    padding: 0 15px;
  }

  ul {
    padding: 0;
    list-style: none;
    text-align: left;

    li {
      height: 35px;
      line-height: 35px;
      padding: 0 15px;
      box-sizing: border-box;
      a {
        color: #555;
        &:hover {
          color: #409eff;
        }
      }
    }
  }
}
</style>
