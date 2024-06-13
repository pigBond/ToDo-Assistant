<template>
    <div class="common-layout">
        <el-container>
            <el-aside width="50px" style="background-color: lightblue;">
                <div style="margin-top: 10px;">
                    <el-row class="button-row">
                        <el-col :span="24">
                            <el-button type="primary" :icon="Check" circle class="button-spacing"
                                @click="currentComponent = 'currentDay'" />
                        </el-col>
                        <el-col :span="24">
                            <el-button type="success" :icon="Edit" circle class="button-spacing" 
                            @click="currentComponent = 'taskLists'" />
                        </el-col>
                        <el-col :span="24">
                            <el-button type="danger" :icon="Message" circle class="button-spacing" 
                            @click="currentComponent = 'calendarTasks'" />
                        </el-col>
                        <el-col :span="24">
                            <el-button type="warning" :icon="Star" circle class="button-spacing" 
                            @click="currentComponent = 'dailyTasks'" />
                        </el-col>
                    </el-row>
                </div>
            </el-aside>
            <el-container style="height: 700px;">
                <el-header height="40px" style="background-color: lightcoral;">Header</el-header>
                <el-main style="background-color: lightgreen;">
                    <component :is="components[currentComponent]"></component>
                </el-main>
            </el-container>
        </el-container>
    </div>
</template>

<style>
.button-row {
    display: flex;
    flex-direction: column;
    align-items: center;
    /* 可选，用于居中对齐按钮 */
}

.button-spacing {
    margin-bottom: 10px;
    /* 设置按钮之间的垂直间隔 */
}
</style>

<script lang="ts" setup>
import { ref } from 'vue';
import {
    Check,
    Edit,
    Message,
    Star,
} from '@element-plus/icons-vue'

import calendarTasks from './components/calendar_tasks.vue'
import currentDay from './components/current_day.vue'
import dailyTasks from './components/daily_tasks.vue'
import taskLists from './components/task_lists.vue'

const currentComponent = ref('calendar_tasks');


const components = {
    currentDay,
    taskLists,
    calendarTasks,
    dailyTasks
}

</script>