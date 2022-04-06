<template>
  <Grid :source="voicelessSound"></Grid>
  <Grid :source="voicedSound"></Grid>
</template>
<script setup name="Syllabary">
import Grid from "./Grid.vue";
import { reactive } from "vue";
const voicelessSound = reactive({
  title: "清音",
  horizontalAxis: ["a", "i", "u", "e", "o"],
  verticalAxis: ["a", "k", "s", "t", "n", "h", "m", "y", "l", "w", ""],
  data: [
    [
      {
        sn: "1",
        t: "あ",
        p: "a",
      },
      {
        sn: "2",
        t: "い",
        p: "i",
      },
      {
        sn: "3",
        t: "う",
        p: "u",
      },
      {
        sn: "4",
        t: "え",
        p: "e",
      },
      {
        sn: "5",
        t: "お",
        p: "o",
      },
    ],
    [
      {
        sn: "6",
        t: "か",
        p: "ka",
      },
      {
        sn: "7",
        t: "き",
        p: "ki",
      },
      {
        sn: "8",
        t: "く",
        p: "ku",
      },
      {
        sn: "9",
        t: "け",
        p: "ke",
      },
      {
        sn: "10",
        t: "こ",
        p: "ko",
      },
    ],
    [
      {
        sn: "11",
        t: "さ",
        p: "sa",
      },
      {
        sn: "12",
        t: "し",
        p: "shi",
      },
      {
        sn: "13",
        t: "す",
        p: "su",
      },
      {
        sn: "14",
        t: "せ",
        p: "se",
      },
      {
        sn: "15",
        t: "そ",
        p: "so",
      },
    ],
    [
      {
        sn: "16",
        t: "た",
        p: "ta",
      },
      {
        sn: "17",
        t: "ち",
        p: "chi",
      },
      {
        sn: "18",
        t: "つ",
        p: "tsu",
      },
      {
        sn: "19",
        t: "て",
        p: "te",
      },
      {
        sn: "20",
        t: "と",
        p: "to",
      },
    ],
    [
      {
        sn: "21",
        t: "な",
        p: "na",
      },
      {
        sn: "22",
        t: "に",
        p: "ni",
      },
      {
        sn: "23",
        t: "ぬ",
        p: "nu",
      },
      {
        sn: "24",
        t: "ね",
        p: "ne",
      },
      {
        sn: "25",
        t: "の",
        p: "no",
      },
    ],
    [
      {
        sn: "26",
        t: "は",
        p: "ha",
      },
      {
        sn: "27",
        t: "ひ",
        p: "hi",
      },
      {
        sn: "28",
        t: "ふ",
        p: "hu",
      },
      {
        sn: "29",
        t: "へ",
        p: "he",
      },
      {
        sn: "30",
        t: "ほ",
        p: "ho",
      },
    ],
    [
      {
        sn: "31",
        t: "ま",
        p: "ma",
      },
      {
        sn: "32",
        t: "み",
        p: "mi",
      },
      {
        sn: "33",
        t: "む",
        p: "mu",
      },
      {
        sn: "34",
        t: "め",
        p: "me",
      },
      {
        sn: "35",
        t: "も",
        p: "mo",
      },
    ],
    [
      {
        sn: "36",
        t: "や",
        p: "ya",
      },
      {
        sn: "37",
        t: "い",
        p: "i",
        ue: true,
      },
      {
        sn: "38",
        t: "ゆ",
        p: "yu",
      },
      {
        sn: "39",
        t: "え",
        p: "e",
        ue: true,
      },
      {
        sn: "40",
        t: "よ",
        p: "yo",
      },
    ],
    [
      {
        sn: "41",
        t: "ら",
        p: "ra",
      },
      {
        sn: "42",
        t: "り",
        p: "ri",
      },
      {
        sn: "43",
        t: "る",
        p: "ru",
      },
      {
        sn: "44",
        t: "れ",
        p: "re",
      },
      {
        sn: "45",
        t: "ろ",
        p: "ro",
      },
    ],
    [
      {
        sn: "46",
        t: "わ",
        p: "wa",
      },
      {
        sn: "47",
        t: "い",
        p: "i",
        ue: true,
      },
      {
        sn: "48",
        t: "う",
        p: "u",
        ue: true,
      },
      {
        sn: "49",
        t: "え",
        p: "e",
        ue: true,
      },
      {
        sn: "50",
        t: "を",
        p: "o",
      },
    ],
    [
      {
        sn: "51",
        t: "ん",
        p: "n",
      },
      {
        sn: "52",
        t: "い",
        p: "i",
        ue: true,
      },
      {
        sn: "53",
        t: "う",
        p: "u",
        ue: true,
      },
      {
        sn: "54",
        t: "え",
        p: "e",
        ue: true,
      },
      {
        sn: "55",
        t: "お",
        p: "o",
        ue: true,
      },
    ],
  ],
});

const voicedSound = reactive({
  title: "浊音",
  horizontalAxis: ["a", "i", "u", "e", "o"],
  verticalAxis: ["g", "z", "d", "b", "p"],
  data: [
    [
      {
        sn: "1",
        t: "が",
        p: "ga",
      },
      {
        sn: "2",
        t: "ぎ",
        p: "gi",
      },
      {
        sn: "3",
        t: "ぐ",
        p: "gu",
      },
      {
        sn: "4",
        t: "げ",
        p: "ge",
      },
      {
        sn: "5",
        t: "ご",
        p: "go",
      },
    ],
    [
      {
        sn: "6",
        t: "ざ",
        p: "za",
      },
      {
        sn: "7",
        t: "じ",
        p: "ji",
      },
      {
        sn: "8",
        t: "ず",
        p: "zu",
      },
      {
        sn: "9",
        t: "ぜ",
        p: "ze",
      },
      {
        sn: "10",
        t: "ぞ",
        p: "zo",
      },
    ],
    [
      {
        sn: "11",
        t: "だ",
        p: "da",
      },
      {
        sn: "12",
        t: "ぢ",
        p: "ji",
      },
      {
        sn: "13",
        t: "う",
        p: "zu",
      },
      {
        sn: "14",
        t: "で",
        p: "de",
      },
      {
        sn: "15",
        t: "ど",
        p: "do",
      },
    ],
    [
      {
        sn: "16",
        t: "ば",
        p: "ba",
      },
      {
        sn: "17",
        t: "び",
        p: "bi",
      },
      {
        sn: "18",
        t: "ぶ",
        p: "bu",
      },
      {
        sn: "19",
        t: "べ",
        p: "be",
      },
      {
        sn: "20",
        t: "ぼ",
        p: "bo",
      },
    ],
    [
      {
        sn: "21",
        t: "ぱ",
        p: "pa",
      },
      {
        sn: "22",
        t: "ぴ",
        p: "pi",
      },
      {
        sn: "23",
        t: "ぷ",
        p: "pu",
      },
      {
        sn: "24",
        t: "ぺ",
        p: "pe",
      },
      {
        sn: "25",
        t: "ぽ",
        p: "po",
      },
    ],
  ],
});

// const yoon = reactive({})
</script>
<style scoped lang="scss"></style>
