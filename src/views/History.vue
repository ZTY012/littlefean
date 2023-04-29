<script setup lang="ts">
import HistoryItem from '@/components/HistoryItem.vue';
</script>

<template>
  <div>
    <HistoryItem :year="2019" :month="6" :day="8" :hour="12">1111</HistoryItem>
    <HistoryItem :year="2019" :month="6" :day="8" :hour="22" yellow>1111</HistoryItem>
  </div>
</template>

<style scoped lang="scss"></style>
