<template>
    <div>
        <el-row :gutter="20" style="height: 400px;">
            <el-col :span="12" style="background-color: lightsalmon;">
                <div class="scrollable-timeline">
                    <h3>今日任务</h3>
                    <el-timeline style="max-width: 600px">
                        <el-timeline-item timestamp="2018/4/12" placement="top">
                            <el-card>
                                <h4>Update Github template</h4>
                                <p>Tom committed 2018/4/12 20:46</p>
                            </el-card>
                        </el-timeline-item>
                        <el-timeline-item timestamp="2018/4/3" placement="top">
                            <el-card>
                                <h4>Update Github template</h4>
                                <p>Tom committed 2018/4/3 20:46</p>
                            </el-card>
                            <el-card>
                                <h4>Update Github template</h4>
                                <p>Tom committed 2018/4/3 20:46</p>
                            </el-card>
                        </el-timeline-item>
                        <el-timeline-item timestamp="2018/4/2" placement="top">
                            <el-card>
                                <h4>Update Github template</h4>
                                <p>Tom committed 2018/4/2 20:46</p>
                            </el-card>
                        </el-timeline-item>
                    </el-timeline>
                </div>
            </el-col>
            <el-col :span="12">
                <div class="grid-content ep-bg-purple">
                    <el-row :span="8" style="background-color: yellowgreen;height: 200px;">
                        <h4 style="margin-left: 10px;">今日截至/重要任务</h4>
                    </el-row>
                    <el-row :span="8" style="background-color: brown;height: 200px;">
                        <h4 style="margin-left: 10px;">助手tips</h4>
                    </el-row>
                    <el-row :span="8" style="background-color: goldenrod;height: 200px;">
                        <h4 style="margin-left: 10px;">结算</h4>
                    </el-row>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script lang="ts" setup>
</script>

<style scoped>
/* 添加滚动条的样式 */
.scrollable-timeline {
  height: 600px; /* 根据需要调整高度 */
  overflow-y: auto; /* 启用垂直滚动条 */
  scrollbar-width: thin; /* 设置滚动条的宽度（可以设置为'auto', 'thin', 或 'none'） */
  scrollbar-color: #888 #f1f1f1; /* 设置滚动滑块和滚动条轨道的颜色 */
}
</style>