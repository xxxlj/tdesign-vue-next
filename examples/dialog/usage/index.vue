<!-- 该脚本为自动生成，如有需要请在 /script/generate-usage/index.js 中调整 -->
<template>
  <base-usage :code="usageCode" :config-list="configList" :panel-list="panelList" @PanelChange="onPanelChange">
    <template #dialog="{ configProps }"
      ><div>
        <t-button @click="visible = true">Open Modal</t-button>
        <t-dialog v-bind="configProps" v-model:visible="visible">
          <p>This is a dialog</p>
        </t-dialog>
      </div></template
    >
  </base-usage>
</template>

<script setup lang="jsx">
/* eslint-disable */
import { ref, onMounted } from 'vue';
import configJson from './props.json';
const visible = ref(false);
const handleClick = () => {
  visible.value = !visible.value;
};

const configList = ref(configJson);
const panelList = [{ label: 'dialog', value: 'dialog' }];

const usageCodeMap = {
  dialog:
    '\n        <div>\n          <t-button @click="visible = true">Open Modal</t-button>\n          <t-dialog v-bind="configProps" v-model:visible="visible">\n            <p>This is a dialog</p>\n          </t-dialog>\n        </div>\n      ',
};
const usageCode = ref(`<template>${usageCodeMap[panelList[0].value].trim()}</template>`);

function onPanelChange(panel) {
  usageCode.value = `<template>${usageCodeMap[panel].trim()}</template>`;
}
</script>
