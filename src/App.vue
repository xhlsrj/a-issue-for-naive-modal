<script setup lang="ts">
import { NModal } from 'naive-ui';
import { ref } from 'vue';
import OneBox from './OneBox.vue';

const isShowModal = ref(false);
const value = ref('');
function fn() {}
</script>

<template>
  <div class="click" @click="isShowModal = true">弹窗</div>
  <NModal v-model:show="isShowModal" :mask-closable="false">
    <div>
      <OneBox>
        <input v-model="value" />
        <div>
          <div style="display: block" @click="fn">fn</div>
        </div>
      </OneBox>
      <div class="click" @click="isShowModal = false">关闭</div>
    </div>
  </NModal>
</template>

<style scoped>
.click {
  cursor: pointer;
  user-select: none;
}
</style>
