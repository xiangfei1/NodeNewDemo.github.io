<template>
  <div class="header">
    <div class="info">
      <a href="/">
        <img :src="require('@/assets/image/cnodejs.svg')" alt="网站Logo" />
      </a>
      <span @click="dialogVisible = true">关于</span>
    </div>
    <el-dialog title="关于本项目" :visible.sync="dialogVisible" width="35%">
      <div class="inside-dialog">
        <p>作者：<a href="http://tanglvewu.top" target="_blank">汤略武</a></p>
        <p>
          源码：
          <el-icon type="star" class="el-icon-star-off" />
          <a href="#">NodeCommunity</a>
          <el-icon type="star" class="el-icon-star-off" />
          &nbsp;欢迎Star&nbsp;
          <el-icon type="star" class="el-icon-star-off" />
        </p>
        <div>
          <p>技术栈：</p>
          <ul>
            <li>Vue</li>
            <li>Vue Router</li>
            <li>ElementUI</li>
            <li>Axios</li>
          </ul>
        </div>
      </div>
      <span slot="footer" class="dialog-footer">
        <el-button type="primary" @click="dialogVisible = false"
          >确 定</el-button
        >
      </span>
    </el-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialogVisible: false //关于
    };
  }
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 50px;
  background: #444;
  > div.info {
    width: 1200px;
    height: 100%;
    margin: auto;
    a {
      width: 120px;
      height: 50px;
      display: block;
      float: left;
      img {
        padding-top: 10px;
        display: block;
        width: 100%;
      }
    }
    span {
      float: right;
      height: 50px;
      line-height: 50px;
      color: #fff;
      cursor: pointer;
      font-size: 15px;
      font-weight: bold;
    }
  }
}
</style>

<style lang="scss">
.header {
  .el-dialog__body {
    padding-top: 10px;
    padding-bottom: 0;
    .inside-dialog {
      p {
        margin: auto;
      }
      .el-icon-star-off::before {
        color: #eb2f96;
      }
    }
  }
}
</style>
