<script setup>
import { storeToRefs } from 'pinia';
import { useMyStore } from '../stores/myStore';

const myStore = useMyStore();
const { message } = storeToRefs(myStore);
</script>

<template>
  <div class="column items-center q-mt-md">
    <div class=" ">
      <q-icon name="face" size="2.1rem" class="q-mb-md q-mr-sm"></q-icon><span class="text-h4">Home</span>
      <q-icon name="account_balance" size="2.1rem" class="q-mb-md q-ml-sm"></q-icon>
    </div>
    <div class="text-h6 text-italic text-weight-light">{{ message }}</div>
  </div>
</template>
