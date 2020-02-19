<template>
  <div class="note-content">
    <el-row type="flex" class="row-bg" justify="space-around">
      <el-col :span="6" class="note-menu">
        <div class="note-menu-form">
          <el-input v-model="searchTitle" placeholder="请输入内容" class="input-with-select">
            <el-button slot="append" icon="el-icon-search" />
          </el-input>
          <el-button type="primary" icon="el-icon-plus" class="note-menu-form-insert" />
        </div>
        <div class="note-menu-list">
          <div class="note-menu-item">
            <div class="note-menu-item-content">
              <span class="note-menu-item-content-title">我是内容我是内容我是内容我是内容我是内容我是内容我是内容我是内容我是内容</span>
              <span class="note-menu-item-content-time">2020-02-19</span>
            </div>
            <i class="el-icon-edit note-menu-item-icon" />
            <i class="el-icon-share note-menu-item-icon" />
            <i class="el-icon-delete note-menu-item-icon" />
          </div>
          <div class="note-menu-item">
            <div class="note-menu-item-content">
              <span class="note-menu-item-content-title">ce shi</span>
              <span class="note-menu-item-content-time">2020-02-19</span>
            </div>
            <i class="el-icon-edit note-menu-item-icon" />
            <i class="el-icon-share note-menu-item-icon" />
            <i class="el-icon-delete note-menu-item-icon" />
          </div>
          <div class="note-menu-item">
            <div class="note-menu-item-content">
              <span class="note-menu-item-content-title">hello world</span>
              <span class="note-menu-item-content-time">2020-02-19</span>
            </div>
            <i class="el-icon-edit note-menu-item-icon" />
            <i class="el-icon-share note-menu-item-icon" />
            <i class="el-icon-delete note-menu-item-icon" />
          </div>
        </div>
      </el-col>
      <el-col :span="18" class="note-content-detail"><div>主体内容</div></el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Note',
  data() {
    return {
      searchTitle: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.note-menu{
  background: white;

  &-list{
    height: 100%;
  }
  &-item{
    display: flex;
    flex-direction: row;
    padding: 25px 10%;
    border-bottom: #e0e1e5 solid 1px;
    &-content{
      width: 100%;
      &-title{
        width: 100%;
        white-space: nowrap;
        display: inline-block;
        overflow:hidden;
        text-overflow: ellipsis;
      }
      &-time{
        font-size: 12px;
        color: #c2c2c2;
      }
    }
    &-icon{
      font-size: 24px;
      margin-left: 15px;
      align-self: center;
      display: none;
      &:hover{
        color: #1482f0;
      }
    }
    &:hover {
      background-color: #eaf0fb;
    }
    &:hover &-content{
      width: 70%;
      &-title{
        color: #20a0ff;
      }
    }
    &:hover &-icon{
      display: block;
    }
  }

  &-form{
    margin-top: 5px;
    display: flex;
    flex-direction: row;
    padding: 10px 5px;

    &-insert{
      margin-left: 10px;
    }
  }
}
.note-content{
  height: 100%;
  position: absolute;
  width: 100%;
}
.row-bg {
  width: 100%;
  height: 100%;
  background-color: #f9fafc;
}
</style>
