<template>
  <div class="home">
   <div class="add-word">
    <select style="width: 200px;margin-bottom: 20px" v-model="wordTitle">
    <option value="title">标题</option>
    <option value="author">品牌</option>
    <option value="publisher">出版社</option>
    </select>
    <textarea  style="width: 500px; height: 400px"  v-model="input">
    </textarea>
    <button type="button" @click="handleAddWord()" style="margin-top: 20px;width: 100px;">确定</button>
   </div>
  </div>
</template>

<script lang="ts" setup name="HomeView">
import { ref } from 'vue'
import axios from 'axios'
const input = ref('')
const wordTitle = ref('')
const wordsProhibit = ref([])

const handleAddWord = () => {
  console.log(input.value)
  console.log(wordTitle.value)
 
}
</script>

<style scoped lang="less">
.add-word {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  flex-direction: column;
}
</style>
