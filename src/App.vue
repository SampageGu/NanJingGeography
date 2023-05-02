<template>
  <div id="app">
    <div class="col-md-12 text-center">
      <h1 class="title">南京市地理图集</h1>
      <p class="subtitle">Nanjing City Geographic Atlas</p>
    </div>
    <div class="container">
      <div class="instructions-wrapper"></div>
      <div class="instructions">
            <h2>使用说明</h2>
            <p>
              Hi～欢迎使用本网站！
            </p>
            <p>
这里是南京市地理图集，我们将尽可能提供南京市自然地理、人文地理中多类要素的可视化地图，以辅助更好的中学地理教、学。数据均来源于各大官方平台最新发布，未来我们将持续更新数据，完善平台功能。
</p>
<p>
点击右方按钮，即可显示对应地图，部分按钮对应系列组图，点击图片左右侧箭头即可翻页。</p>
<p>金陵风景好，豪士集新亭！让我们一起用地理视角，去发现美丽南京吧～
            </p>
          
        </div>
      <div class="col-md-7">
        <div v-if="showSwiperLeft1" v-show="!showSwiperLeft2">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesleft1[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesleft1.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperLeft2">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesleft2[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesleft2.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperLeft3">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesleft3[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesleft3.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperLeft4">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesleft4[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesleft4.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperLeft5">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesleft5[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesleft5.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperRight1">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesright1[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesright1.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperRight3">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesright3[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesright3.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        <div v-if="showSwiperRight4">
          <div class="row">
            <div class="col">
              <img :src="swiperImagesright4[index]" alt="Image" class="custom-image" />
            </div>
          </div>
          <div class="prev small-button" v-show="index != 0&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="prev">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" />
            </svg>
          </div>
          <div class="next small-button" v-show="index < swiperImagesright4.length - 1&& (showSwiperLeft1 || showSwiperLeft2||showSwiperLeft3||showSwiperLeft4||showSwiperLeft5||showSwiperRight1||showSwiperRight3||showSwiperRight4)" @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" width="24px" height="24px">
              <path d="M0 0h24v24H0z" fill="none" />
              <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" />
            </svg>
          </div>
        </div>
        
      </div>
      <div class="row align-items-center">
        <div class="col-md-1">
          <div class="d-flex flex-column left-buttons-container">
            <button
              v-for="(button, index) in leftButtons"
              :key="index"
              class="btn btn-primary mb-2 custom-button"
              :style="getButtonStyle(index, 'left')"
              @click="index === 0 ? showLeft1() : index === 1 ? showLeft2():index===2?showLeft3() : index===3?showLeft4():index===4?showLeft5():changeImage(index)" 
            >
              {{ button }}
            </button>
          </div>
        </div>
        <div class="col-md-7">
          <transition name="fade">
            <img :key="currentImage" :src="currentImage" alt="" class="custom-image" />
          </transition>
        </div>
        <div class="col-md-1">
          <div class="d-flex flex-column right-buttons-container">
            <button
              v-for="(button, index) in rightButtons"
              :key="`right-${index}`"
              class="btn btn-primary mb-2 custom-button"
              :style="getButtonStyle(index, 'right')"
              @click="index=== 0 ? showRight1() :index===2?showRight3():index===3?showRight4():changeImage(index + leftButtons.length)"
            >
              {{ button }}
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>




<script>
export default {
  data() {
  return {
    index: 0,//表示第一张图片
    currentImage: "",
    displayedImages: [],
    showSwiperLeft1: false,
    showSwiperLeft2: false, 
    showSwiperLeft3: false, 
    showSwiperLeft4: false, 
    showSwiperLeft5: false, 
    showSwiperRight1: false, 
    showSwiperRight3: false, 
    showSwiperRight4: false, 
    swiperImagesleft1: [
      require("@/../picture/1985-2020南京土地覆被类型图/1.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/2.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/3.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/4.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/5.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/6.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/7.jpeg"),
      require("@/../picture/1985-2020南京土地覆被类型图/8.jpeg"),
    ],
    swiperImagesleft2: [
      require("@/../picture/2016年南京交通/1.jpg"),
      require("@/../picture/2016年南京交通/2.jpg"),
      require("@/../picture/2016年南京交通/3.jpg"),
      require("@/../picture/2016年南京交通/4.jpg"),
      require("@/../picture/2016年南京交通/5.jpg"),
      require("@/../picture/2016年南京交通/6.jpg"),
      require("@/../picture/2016年南京交通/7.jpg"),
    ],
    swiperImagesleft3: [
      require("@/../picture/2019年1.7月南京平均气温图/1.jpg"),
      require("@/../picture/2019年1.7月南京平均气温图/2.jpg"),
      
    ],
    swiperImagesleft4: [
      require("@/../picture/2020年每月南京市降水分布图/1.png"),
      require("@/../picture/2020年每月南京市降水分布图/2.png"),
      require("@/../picture/2020年每月南京市降水分布图/3.png"),
      require("@/../picture/2020年每月南京市降水分布图/4.png"),
      require("@/../picture/2020年每月南京市降水分布图/5.png"),
      require("@/../picture/2020年每月南京市降水分布图/6.png"),
      require("@/../picture/2020年每月南京市降水分布图/7.png"),
      require("@/../picture/2020年每月南京市降水分布图/8.png"),
      require("@/../picture/2020年每月南京市降水分布图/9.png"),
      require("@/../picture/2020年每月南京市降水分布图/10.png"),
      require("@/../picture/2020年每月南京市降水分布图/11.png"),
      require("@/../picture/2020年每月南京市降水分布图/12.png"),
      
    ],
    swiperImagesleft5: [
      require("@/../picture/2021年南京人口、GDP/1.jpg"),
      require("@/../picture/2021年南京人口、GDP/2.jpg"),
      
    ],
    swiperImagesright1:
    [
    require("@/../picture/2022年1.7月南京植被覆盖度图/1.jpg"),
    require("@/../picture/2022年1.7月南京植被覆盖度图/2.jpg"),
    ],
    swiperImagesright3: [
    require("@/../picture/南京市地理位置图/1.jpg"),
      require("@/../picture/南京市地理位置图/2.jpg"),
      
      
    ],
    swiperImagesright4: [
      require("@/../picture/南京市地形地势图/1.jpg"),
      require("@/../picture/南京市地形地势图/2.jpg"),
      require("@/../picture/南京市地形地势图/3.jpg"),
      
    ],
    leftButtons: [
      "1985-2020年南京土地覆被类型图",
      "南京市交通概况图",
      "南京市1/7月平均气温图",
      "2020年南京市每月降水分布图",
      "南京市人口与地区生产总值图",
    ],
    rightButtons: [
      "南京植被覆盖度图",
      "南京市土地利用分布图",
      "南京市地理位置图",
      "南京市地形地势图",
      "南京市水系图",
      "南京市行政区划图",
    ],
    images: [
     
    ],
    imagePaths: [
      "", 
      "", 
      "", 
      "", 
      "", 
      "", 
      require("@/../picture/2021年南京市土地利用分布图.jpg"), 
      "", 
      "", 
      require("@/../picture/南京市水系图.jpg"), 
      require("@/../picture/南京市行政区划图.jpg"), 
      // ... 其他按钮
    ],
  };
},

methods: {
//图片切换的动画效果
  beforeChange() {
    const img = document.querySelector(".custom-image");
    img.style.opacity = 0;
    img.style.transform = "scale(0.9)";
  },

  afterChange() {
    const img = document.querySelector(".custom-image");
    img.style.opacity = 1;
    img.style.transform = "scale(1)";
  },
  // 切换8张图片的代码
  showLeft1() {
    this.index=0;
    this.currentImage = ""; // 清除当前图片
    this.showSwiperLeft1 = true;
    this.showSwiperLeft2 = false;
    this.showSwiperLeft3 = false;
    this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 
  },
  showLeft2() {
    this.index=0;
   this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft1 = false;
    this.showSwiperLeft2 = true;
    this.showSwiperLeft3 = false;
    this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 },
 showLeft3() {
  this.index=0;
   this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = true;
   this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;

 },
 showLeft4(){
  this.index=0;
  this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = false;
   this.showSwiperLeft4=true;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 },
 showLeft5(){
  this.index=0;
  this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = false;
   this.showSwiperLeft4=false;
    this.showSwiperLeft5=true;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 },
 showRight1(){
  this.index=0;
  this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = false;
   this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=true;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 },
 showRight3(){
  this.index=0;
  this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = false;
   this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=true;
    this.showSwiperRight4=false;
 },
 showRight4(){
  this.index=0;
  this.currentImage = ""; // 清除当前图片
   this.showSwiperLeft2 = false;
   this.showSwiperLeft1 = false;
   this.showSwiperLeft3 = false;
   this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=true;
 },
  changeImage(index) {
    if (index === 0||index===1||index===2||index===3||index===4||index===5||index===7||index===8) {return;} // 当点击左侧第一个按钮时，不执行后续操作
    this.showSwiperLeft1 = false;
    this.showSwiperLeft2 = false;
    this.showSwiperLeft3 = false;
    this.showSwiperLeft4=false;
    this.showSwiperLeft5=false;
    this.showSwiperRight1=false;
    this.showSwiperRight3=false;
    this.showSwiperRight4=false;
 
    this.displayedImages = []; // 清空多图展示
    const imagePath = this.imagePaths[index];
    
    if (imagePath) {

      
   
      this.currentImage = imagePath;
      this.showSwiper = false; // 隐藏 swiper
   
    }
  },
  getButtonStyle(index, side) {
    let left = side === "left" ? "-1000px" : "170px";
    return {
      top: `${100 + 110 * index}px`,
      left: left,
      width: "150px",
      height: "40px",
    };
  },
  //进行上一张下一张切换的代码
  prev() 
    {
      if (this.showSwiperLeft1||this.showSwiperLeft2||this.showSwiperLeft3||this.showSwiperLeft4||this.showSwiperLeft5||this.showSwiperRight1||this.showSwiperRight3||this.showSwiperRight4) this.index--;
    },
    next()
     {
      if (this.showSwiperLeft1||this.showSwiperLeft2||this.showSwiperLeft3||this.showSwiperLeft4||this.showSwiperLeft5||this.showSwiperRight1||this.showSwiperRight3||this.showSwiperRight4) this.index++;
    },

},
  mounted() {
    this.currentImage = this.images[0];
  },
  
};
</script>

<style src="./main.css"></style>

<style scoped>
/* 图片切换的特效 */
.fade-enter-active,
  .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter,
  .fade-leave-to {
    opacity: 1;
  }.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.row {
  margin-left: -10px;
  margin-right: -10px;
}
/* 按钮的特效 */
.custom-button {
  letter-spacing: 2px;
  position: absolute;
  margin-left: 1120px;
  margin-right: 10px;
  width: 650px;
  height: 440px;
  font-size: 13px;
  white-space: normal; 
  line-height: 1.1; 
  padding: 5px 10px; 
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  text-align: center;
  transform: scale(1.2);

  background:transparent;
  text-transform: uppercase;
  outline: none;
  overflow: hidden;
    /* cursor: pointer;
    transition: all 0.3s ease; */ 
}
.custom-button:after{
  content: '';
    display: block;
    position: absolute;
    top: -36px;
    left: -100px;
    background: white;
    width: 50px;
    height: 125px;
    opacity: 20%;
    transform: rotate(-45deg);
}
.custom-button:hover:after{
  left: 120%;
  transition: all 600ms cubic-bezier(0.3, 1, 0.2, 1);
   -webkit-transition: all 600ms cubic-bezier(0.3, 1, 0.2, 1);
}
/* 左右切换图片的小按钮 */
.small-button
{
  position: absolute;
  margin-left: 1120px;
  margin-right: 10px;
  width: 300px;
  height: 110px;
   font-size: 14px;
  white-space: normal; 
  line-height: 1.1; 
  padding: 5px 10px; 
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  text-align: center;
}
.small-button:hover{
  background-color: #0056b3;
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}
.custom-button:hover {
    background-color: #0056b3;
    /* transform: translateY(-2px); */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
   
    /* //按钮边框消失 */
  /* border-bottom-right-radius: 50px;
   border-top-left-radius: 50px;
   border-bottom-left-radius: 10px;
   border-top-right-radius: 10px; */
  }

/* 中间显示图像的区域 */
.custom-image {
  border: 10px solid transparent; /*例如：#333, #ccc, #f00 等
  /* border:2px; */
  border-radius: 10px; /* 设置边框圆角，可以根据需要调整大小 */
  position: absolute;
  top: 110px; /* Set the top position */
  left: 430px; /* Set the left position */
  width: 509px; /* Set the width */
  height: 720px; /* Set the height */
  font-size:small;
  transition: opacity 0.5s, transform 0.5s;
}
/* 大标题 */
.title {
  /* font-family: "FZGW Xiaobiao Song", serif;   Set the font family */
  margin-bottom: 20px;
  font-size: 56px; 
  font-family: "SimHei", "Heiti", "黑体", serif;  
  /* font-weight: bold;   */
  /* text-transform: uppercase;  */
 /* font-family: "Roboto", sans-serif;   */

  position:absolute;
  top:-40px;
  left:440px;
  width:1000px;
  color: transparent;
  color: #fafafa;
 letter-spacing: 18px;


text-shadow: 0px 1px 0px #999, 0px 2px 0px #888, 0px 3px 0px #777, 0px 4px 0px #666, 0px 5px 0px #555, 0px 6px 0px #444, 0px 7px 0px #333, 0px 8px 7px #001135;
/* text-align: center; */

} 
.prev{
  position: absolute;
  top:450px;
  left:-715px;
  z-index: 10;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 50%;
  width: 30px;    
  height: 26px;  
  padding: 5px;
 
  cursor: pointer;
}
.next{
  position: absolute;
  top: 450px; 
  left: -210px; 
  z-index: 10;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 50%;
  width: 30px;    
  height: 26px;  
  padding: 5px;
 
  cursor: pointer;
}
@media (max-width: 768px) {
  .custom-button {
    width: 400px;
    height: 500px;
    font-size: 12px;
  }
}
.right-buttons-container {
  position: absolute; /* 设置相对定位，以便在该容器内定位按钮 */
  top: 80px; /* 向下移动按钮，可以根据需要调整 */
  left: -0px; /* 向右移动按钮，可以根据需要调整 */
}
.left-buttons-container {
  position: absolute; /* 设置相对定位，以便在该容器内定位按钮 */
  top: 130px; /* 向下移动按钮，可以根据需要调整 */
  left: 900px; /* 向右移动按钮，可以根据需要调整 */
}
/* 左边的小标题 */
.instructions {
  position: absolute;
  top:120px;
  left:100px;
  width: 250px;
  white-space: normal;
  margin: 10px 0;
  font-size: 20px; /* 根据需要调整字体大小 */
  line-height: 1.6; /* 设置行高以提高可读性 */
  font-family: "楷体", "KaiTi", serif;
  color:#fafafa;
}
/* 左边的介绍部分的正文 */
.instructions h2 {
  font-family: "楷体", "KaiTi", serif;
  font-size: 28px; /* 设置小标题字体大小 */
  margin-bottom: 10px; /* 设置小标题下方的空间 */
}
/* 大标题下面的英文子标题 */
.subtitle{
  margin-bottom: 20px;
  font-size: 30px; 
  font-family: "SimHei", "Heiti", "黑体", serif;  
  position:absolute;
  top:35px;
  left:450px;
  width:1000px;
  color: transparent;
  color: #fafafa;
 letter-spacing: 2px;
text-shadow: 0px 1px 0px #999, 0px 2px 0px #888, 0px 3px 0px #777, 0px 4px 0px #666, 0px 5px 0px #555, 0px 6px 0px #444, 0px 7px 0px #333, 0px 8px 7px #001135;
/* text-align: center; */
}
/*instruction后面的背景*/
.instructions-wrapper{
  background-color: rgba(128, 128, 128, 0.3); /* 灰色背景，透明度 50% */
   padding: 20px;  /*添加内边距以使文本与背景之间有一定间距 */
  width: 250px; /*设置宽度以仅覆盖左侧文本 */
  height: 660px;
  position:absolute;
  top:130px;
  left:70px;
}
</style>
