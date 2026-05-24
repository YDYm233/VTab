<script setup lang="ts">
import { ref } from "vue"

const email = ref('')
const password = ref('')
const loading = ref(false)

function handleLogin() {
  loading.value = true
  setTimeout(() => {
    loading.value = false
  }, 1500)
}
</script>

<template>
  <div class="about">
    <var-space align="center" justify="center" direction="column">
      <var-card title="关于 V_Tab" style="width: 380px">
        <var-typography>
          基于 Vue 3 + Varlet UI 的书签管理面板。
          热重载已启动，改代码秒生效 🔥
        </var-typography>
      </var-card>

      <var-card title="登录表单" style="width: 380px">
        <var-space direction="column" :size="16">
          <var-input
            v-model="email"
            placeholder="邮箱"
            variant="outlined"
            clearable
          >
            <template #prepend-icon>
              <var-icon name="email" />
            </template>
          </var-input>

          <var-input
            v-model="password"
            type="password"
            placeholder="密码"
            variant="outlined"
            clearable
          >
            <template #prepend-icon>
              <var-icon name="lock" />
            </template>
          </var-input>

          <var-button
            type="primary"
            block
            :loading="loading"
            @click="handleLogin"
          >
            {{ loading ? '登录中...' : '登录' }}
          </var-button>

          <var-checkbox>记住我</var-checkbox>
        </var-space>
      </var-card>

      <var-button type="primary" text @click="$router.push('/')">
        返回首页
      </var-button>
    </var-space>
  </div>
</template>

<style scoped>
.about {
  padding: 32px 16px;
}
</style>
