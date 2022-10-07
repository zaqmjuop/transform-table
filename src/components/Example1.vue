<template>
  <div class="transform-card-table">
    <div class="sprite-586 "></div>
    <div v-for="(item, index) in tableData" :key="index" class="transform-card-item">
      <ul>
        <li>{{item.date}}</li>
        <li>{{item.name}}</li>
        <li>{{item.address}}</li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
const tableData = [
  {
    date: "2016-05-02",
    name: "王小虎",
    address: "上海市普陀区金沙江路 1518 弄",
  },
  {
    date: "2016-05-04",
    name: "王小虎",
    address: "上海市普陀区金沙江路 1517 弄",
  },
  {
    date: "2016-05-01",
    name: "王小虎",
    address: "上海市普陀区金沙江路 1519 弄",
  },
  {
    date: "2016-05-03",
    name: "王小虎",
    address: "上海市普陀区金沙江路 1516 弄",
  },
];
</script>

<style scoped>
.transform-card-table {
  border: 1px solid #eee;
  border-radius: 5px;
  overflow: hidden;
}

.transform-card-item {
  display: inline-block;
  border-radius: 5px;
  border: 1px solid #eee;
}
</style>
