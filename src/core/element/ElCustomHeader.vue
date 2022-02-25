<template>
  <el-header class="btn-bar">
    <slot></slot>
    <el-button v-if="$attrs.uploadJson" type="text" size="default" @click="$emit('uploadJson')">
      <SvgIcon iconClass="upload" />导入JSON
    </el-button>
    <el-button v-if="$attrs.clearable" type="text" size="default" @click="$emit('clearable')">
      <SvgIcon iconClass="clearable" />清空
    </el-button>
    <el-button v-if="$attrs.preview" type="text" size="default" @click="$emit('preview')">
      <SvgIcon iconClass="preview" />预览
    </el-button>
    <el-button v-if="$attrs.generateJson" type="text" size="default" @click="$emit('generateJson')">
      <SvgIcon iconClass="generate-json" />生成JSON
    </el-button>
    <el-button v-if="$attrs.generateCode" type="text" size="default" @click="$emit('generateCode')">
      <SvgIcon iconClass="generate-code" />生成代码
    </el-button>
  </el-header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SvgIcon from '@/components/SvgIcon.vue'

export default defineComponent({
  name: 'CustomHeader',
  components: {
    SvgIcon
  },
  emits: ['uploadJson', 'clearable', 'preview', 'generateJson', 'generateCode']
})
</script>
