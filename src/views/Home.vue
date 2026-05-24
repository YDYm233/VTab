<script setup lang="ts">
import { ref } from "vue"

const count = ref(0)
const showDialog = ref(false)
const tab = ref("tab1")
</script>

<template>
  <div class="home">
    <var-space align="center" justify="center" direction="column">
      <var-card title="V_Tab" subtitle="巴巴塔的星域仪表盘" style="width: 360px">
        <template #extra>
          <var-chip size="small" color="#9c27b0">Varlet UI</var-chip>
          <var-chip size="small" color="#2196f3" style="margin-left: 6px">Vue 3</var-chip>
          <var-chip size="small" color="#4caf50" style="margin-left: 6px">TS</var-chip>
        </template>

        <var-space direction="column" :size="12">
          <var-button type="primary" block @click="count++">
            点我 {{ count }} 次
          </var-button>

          <var-button type="info" block @click="showDialog = true">
            打开弹窗
          </var-button>

          <var-input placeholder="写点啥..." variant="outlined" clearable />
        </var-space>
      </var-card>

      <var-dialog
        v-model:show="showDialog"
        title="你好领主"
        message="Varlet UI 集成成功，热重载跑着呢！"
        @confirm="showDialog = false"
      />

      <var-pagination :current="1" :total="50" :simple="false" />

      <var-tabs v-model:active="tab" elevation>
        <var-tab name="tab1">书签</var-tab>
        <var-tab name="tab2">收藏</var-tab>
        <var-tab name="tab3">设置</var-tab>
      </var-tabs>

      <var-badge value="hot">
        <var-button type="warning">通知</var-button>
      </var-badge>

      <var-rate v-model="count" />
    </var-space>
  </div>
</template>

<style scoped>
.home {
  padding: 32px 16px;
}
</style>
