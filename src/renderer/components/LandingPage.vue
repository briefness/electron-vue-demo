<template>
  <div id="wrapper">
    <el-form :inline="true" :model="mobileInfo" class="demo-form-inline">
      <el-form-item>
        <el-input v-model="mobileInfo.mobile" placeholder="手机号码"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="search">单个查询</el-button>
      </el-form-item>
    </el-form>
    <el-table
     :data="tableData"
     border
     style="width: 100%">
     <el-table-column
       type="index"
       label="序号"
       width="50">
     </el-table-column>
     <el-table-column
       prop="phone"
       label="手机号码">
     </el-table-column>
     <el-table-column
       prop="integral"
       label="积分">
     </el-table-column>
     <el-table-column
       prop="payment"
       label="账期">
     </el-table-column>
     <el-table-column
       prop="attCounties"
       label="归属区县">
     </el-table-column>
   </el-table>
  </div>
</template>

<script>

  export default {
    name: 'landing-page',
    data() {
      return {
        tableData: [
          {
            phone: '2',
            integral: '2',
            payment: '2',
            attCounties: '2'
          }
        ],
        mobileInfo: {
          mobile: ''
        }
      }
    },
    methods: {
      // 单个查询
      search () {}
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }
</style>
