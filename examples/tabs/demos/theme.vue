<template>
  <div class="tdesign-demo-block-column-large">
    <div class="tdesign-demo-block-column">
      <t-tabs v-model="value1">
        <t-tab-panel value="first" label="选项卡1">
          <p style="padding: 25px">选项卡1</p>
        </t-tab-panel>
        <t-tab-panel value="second" label="选项卡2">
          <p style="padding: 25px">选项卡2</p>
        </t-tab-panel>
        <t-tab-panel value="third" label="选项卡3">
          <p style="padding: 25px">选项卡3</p>
        </t-tab-panel>
      </t-tabs>

      <t-tabs v-model="value2" theme="card">
        <t-tab-panel value="first" label="选项卡1">
          <p style="padding: 25px">选项卡1</p>
        </t-tab-panel>
        <t-tab-panel value="second" label="选项卡2">
          <p style="padding: 25px">选项卡2</p>
        </t-tab-panel>
        <t-tab-panel value="third" label="选项卡3">
          <p style="padding: 25px">选项卡3</p>
        </t-tab-panel>
      </t-tabs>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const value1 = ref('first');
const value2 = ref('first');
</script>
