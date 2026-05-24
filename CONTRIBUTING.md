# Contributing — V_Tab

## 🔗 远程仓库

- **GitHub:** https://github.com/YDYm233/VTab
- **SSH:** git@github.com:YDYm233/VTab.git


## ✅ 技术栈

- **Vue 3** — Composition API + `<script setup>`
- **TypeScript** — 类型安全，不允许 `any` 偷懒
- **Varlet UI** — 统一 UI 库
- **Pinia** — 状态管理
- **Vue Router 4** — 路由

> 语法稳定正确，不搞花活。

## ✍️ 提交

- **Author:** `Vex@Babata`
- **语言:** 英语
- **风格:** 直接、通俗易懂、严谨的同时可以俏皮一点

```
feat: initial bookmark sync module
fix: search debounce not triggering on mobile
style: make the login button less ugly
feat: add bookmark drag-drop — hope nothing breaks 🤞
```

## 📁 文件路径规则

```
src/
├── components/     # 通用可复用组件 PascalCase.vue
├── views/          # 页面级别组件 PascalCase.vue
├── router/         # 路由配置 index.ts
├── stores/         # Pinia 状态模块 camelCase.ts
├── composables/    # 组合式函数 useCamelCase.ts
├── utils/          # 工具函数 camelCase.ts
├── types/          # TS 类型定义 camelCase.ts
├── assets/         # 静态资源
├── api/            # API 请求模块 camelCase.ts
├── App.vue
└── main.ts
```

## 🏷️ 命名规则

| 类型 | 规则 | 举例 |
|------|------|------|
| **组件文件** | PascalCase | `BookmarkCard.vue` |
| **组件名** | PascalCase | `BookmarkCard` |
| **普通目录** | camelCase | `utils/`, `api/` |
| **TS/JS 文件** | camelCase | `useAuth.ts`, `fetchBookmarks.ts` |
| **Pinia Store** | camelCase | `useBookmarkStore.ts` |
| **Composable** | `use` 前缀 | `useTheme.ts`, `usePagination.ts` |
| **路由 name** | PascalCase | `name: BookmarkDetail` |
| **事件** | kebab-case | `@bookmark-deleted` |
| **CSS 类名** | kebab-case | `.bookmark-card` |

## 🧾 代码规范

- **组件命名:** 多词命名，避免单词组件（`Button` → `VarButton` 用库的，自己的避免）
- **Props 定义:** 尽量用 TS 类型标注，不用运行时 `prop` 对象
  ```ts
  // ✅
  defineProps<{
    bookmark: Bookmark
    editable?: boolean
  }>()

  // ❌
  defineProps({
    bookmark: Object,
    editable: Boolean
  })
  ```
- **Emits:** 同样 TS 标注
  ```ts
  const emit = defineEmits<{
    delete: [id: string]
    update: [data: Partial<Bookmark>]
  }>()
  ```
- **模板:** `<script setup>` + `ref`/`computed`，少用 `watch`
- **样式:** `<style scoped>`，不写全局样式污染
- **import 顺序:** Vue → Router → Pinia → 组件 → 工具函数
- **禁止:** `any`、`// @ts-ignore`、深层嵌套超过 3 层

## 📋 待补充

_领主Lord留着以后补_
