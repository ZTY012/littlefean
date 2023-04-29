<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    year: number
    month: number
    day: number
    hour: number
    minute?: number
    yellow?: boolean
    type?: string
  }>(),
  {
    minute: 0,
    yellow: false,
    type: '无',
  }
)
</script>

<template>
  <div>
    <div
      class="left"
      :style="{
        backgroundColor: 6 < hour && hour < 20 ? '#87ceeb' : '#00008b',
        color: 6 < hour && hour < 20 ? '#000' : '#87ceeb',
      }"
    >
      <span class="icon">{{ 6 < hour && hour < 20 ? '🌞' : '🌙' }}</span>
      <div class="small">{{ year }}</div>
      <div class="big">{{ month }} {{ day }}</div>
      <div class="small">
        {{ hour }}:{{ minute < 10 ? `0${minute}` : minute }}
      </div>
    </div>
    <div
      class="right"
      :style="{ backgroundColor: yellow ? '#b57500' : '#000' }"
    >
      <div><slot></slot></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
:deep() {
  display: flex;
  justify-content: center;
  margin-top: 0.5em;
}

.left {
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  width: 5em;
  height: 5em;
  line-height: 165%;
  display: block;
  border-radius: 10px 0 0 10px;
  position: relative;

  * {
    margin: 0;
    justify-content: center;
  }

  .big {
    font-size: 180%;
  }

  .small {
    font-size: 100%;
  }

  .icon {
    position: absolute;
    top: 0;
    right: 0;
  }
}

.right {
  display: block;
  width: 13em;
  height: 5em;
  color: #fff;
  border-radius: 0 10px 10px 0;

  > div {
    margin-top: 0.5em;
    display: flex;
    justify-content: center;
  }
}
</style>
