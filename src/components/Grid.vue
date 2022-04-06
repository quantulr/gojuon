<template>
  <h2 class="title">{{ title }}</h2>
  <div class="syllabay-wrap">
    <div class="header-row">
      <span class="header-item" v-for="item in horizontalAxis" :key="item">{{
        item
      }}</span>
    </div>
    <div class="row" v-for="(row, index) in data" :key="row[0].sn">
      <div class="header-column">
        <span>{{ verticalAxis[index] }}</span>
      </div>
      <div class="item" v-for="item in row" :key="item.sn">
        <div class="content" v-if="!item.ue" @click="play(item.p)">
          <span class="hiragana master">
            {{ item.t }}
          </span>
        </div>
      </div>
    </div>
  </div>
  <audio id="voice"></audio>
</template>
<script setup name="Grid">
import { ref, nextTick, toRefs } from "vue";

const props = defineProps({
  source: {
    type: Object,
    required: true,
  },
  column: {
    type: Number,
    default: 5,
  },
});
const { data, horizontalAxis, verticalAxis, title } =
  toRefs(props).source.value;
// const src = ref("");

const play = (p) => {
  const el = document.querySelector(`#voice`);
  // src.value = new URL(`../assets/voice/${p}.mp3`, import.meta.url).href;
  el.src = new URL(`../assets/voice/${p}.mp3`, import.meta.url).href;
  nextTick(() => {
    el.play();
  });
};
</script>
<style scoped lang="scss">
.title {
  text-align: center;
}
.syllabay-wrap {
  box-sizing: border-box;
  .header-row {
    display: flex;
    margin-left: 40px;
    .header-item {
      flex: 1;
      text-align: center;
    }
  }
  .row {
    display: flex;
    .header-column {
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .item {
      //   border: 1px solid blueviolet;
      text-align: center;
      flex: 1;
      .content {
        height: 40px;
        .master {
          font-size: 24px;
        }
      }
    }
  }
}
</style>
