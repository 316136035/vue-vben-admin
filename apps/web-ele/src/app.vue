<script lang="ts" setup>
/**
 * 导入 Element Plus 的设计令牌钩子函数，用于在应用中使用 Element Plus 的设计系统。
 */
import { useElementPlusDesignTokens } from '@vben/hooks';

/**
 * 导入 Element Plus 的配置提供者组件，用于全局配置 Element Plus 的行为和样式。
 */
import { ElConfigProvider } from 'element-plus';

/**
 * 导入 Element Plus 的本地化配置，用于设置组件的语言和区域设置。
 */
import { elementLocale } from '#/locales';

/**
 * 定义组件的名称为 'App'，用于调试和开发工具中识别该组件。
 */
defineOptions({ name: 'App' });

/**
 * 调用 useElementPlusDesignTokens 钩子函数，应用 Element Plus 的设计令牌。
 */
useElementPlusDesignTokens();
</script>

<template>
  /**
   * 使用 ElConfigProvider 组件包裹整个应用，并传入本地化配置。
   * RouterView 是 Vue Router 的视图组件，用于渲染当前路由对应的组件。
   */
  <ElConfigProvider :locale="elementLocale">
    <RouterView />
  </ElConfigProvider>
</template>
