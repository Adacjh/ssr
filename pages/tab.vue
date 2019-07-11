<template>
  <div>
      <div class="ctrl">
          <span v-for="(item,index) in ['体育','新闻','饮食']"
          :key="index"
          @click="handClick(index)"
          :class="{active:current===index}">{{item}}</span>
      </div>
      <div v-if="current===0">
          <ul>
              <li>运动</li>
              <li>运动</li>
              <li>运动</li>
          </ul>
      </div>
      <div v-if="current===1">
          <ul>
              <li>大新闻</li>
              <li>大新闻</li>
              <li>大新闻</li>
          </ul>
      </div>
      <div v-if="current===2">
          <ul>
              <li>吃大餐</li>
              <li>吃大餐</li>
              <li>吃大餐</li>
          </ul>
      </div>
  </div>
</template>

<script>

export default {
   data(){
       return{
           current:0
       }
   },
   methods: {
       handClick(index){
           this.current=index
       }
   }
}
</script>

<style>
.active{
    color: red
}
.ctrl{
    margin-bottom: 10px
}
.ctrl span{
    cursor: pointer;
    margin: 0 10px
}
</style>
