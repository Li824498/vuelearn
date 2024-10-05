<template>
  <div>
    <!-- <h1>message</h1> -->
    <!-- <element-view></element-view> -->
    <emp-view></emp-view>

    <el-container style="height: 700px; border: 1px solid #eee">
      <el-header style="font-size: 40px; background-color: rgb(238, 241, 246)"
        >管理系統</el-header
      >
      <el-container>
        <el-aside width="200px">
          <el-menu :default-openeds="['1', '3']">
            <el-submenu index="1">
              <template slot="title"
                ><i class="el-icon-message"></i>係統信息管理</template
              >
              <el-menu-item index="1-1">部門管理</el-menu-item>
              <el-menu-item index="1-2">員工管理</el-menu-item>
            </el-submenu>
          </el-menu>
        </el-aside>
        <el-main>
          <el-table :data="tableData">
            <el-table-column
              prop="name"
              label="姓名"
              width="180"
            ></el-table-column>
            <el-table-column
              prop="image"
              label="图像"
              width="180"
            ></el-table-column>
            <el-table-column
              prop="gender"
              label="性别"
              width="140"
            ></el-table-column>
            <el-table-column
              prop="job"
              label="职位"
              width="140"
            ></el-table-column>
            <el-table-column
              prop="entrydate"
              label="入职日期"
              width="180"
            ></el-table-column>
            <el-table-column
              prop="updatetime"
              label="最后操作时间"
              width="230"
            ></el-table-column>
            <el-table-column label="操作">
              <el-button type="primary" size="mini">编辑</el-button>
              <el-button type="danger" size="mini">删除</el-button>
            </el-table-column>
          </el-table>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import EmpView from "./views/tlias/EmpView.vue";
// import ElementView from './views/element/ElementView.vue'
export default {
  components: { EmpView },
  // components: { ElementView },
  data: function () {
    return {
      tableData: []
      
    };
  },
  methods: {},
};
</script>

<style>
</style>
