<template>
  <div class="img-container">
    <div class="slide-container">
      <img class="img-asd slide" src="@/assets/mainBanner_01.png" alt="" />
      <img class="img-asd slide" src="@/assets/mainBanner_02.png" alt="" />
      <img class="img-asd slide" src="@/assets/mainBanner_03.png" alt="" />
      <img class="img-asd slide" src="@/assets/mainBanner_04.png" alt="" />
    </div>
    <button class="prevBtn">◀</button>
    <button class="nextBtn">▶</button>
  </div>
  <div class="text-over-image" v-if="slideIndex === 0">
    <p class="img-title">
      미래 산업의 중심 <br />
      <span class="bold">동의대학교 조기취업형 계약학과</span>
    </p>
    <p class="img-sub-title">
      조기취업형 계약학과 입학과 동시에 취업을!<br />
      기업맞춤형 교육과정에 따라 전공교육을 실시합니다.
    </p>
  </div>

  <div class="text-over-image" v-if="slideIndex === 1">
    <p class="img-title">
      4차 산업 시대를 <br />선도하는
      <span class="bold">소프트웨어 융합학과</span>
    </p>
    <p class="img-sub-title">
      빅데이터, 스마트 팩토리, 사물인터넷 등 4차산업 필수 기술을<br />
      효율적으로 익히는 전문 교육과정 제공을 제공합니다.
    </p>
  </div>

  <div class="text-over-image" v-if="slideIndex === 2">
    <p class="img-title">
      맞춤형 기술 인력 양성 <br />
      <span class="bold">미래형자동차학과</span>
    </p>
    <p class="img-sub-title">
      실무 중심의 교육과 산업 연계를 통해 미래 자동차 산업분야에서<br />
      성공적인 경력을 쌓을 수 있습니다.
    </p>
  </div>

  <div class="text-over-image" v-if="slideIndex === 3">
    <p class="img-title">
      현장 중심의 인재 육성 <br />
      <span class="bold">스마트호스피탈리학과</span>
    </p>
    <p class="img-sub-title">
      비대면 서비스 역량 강화와 다양한 기업 연계 프로그램으로<br />
      현장 중심의 스마트호스피탈리티 인재를 육성합니다.
    </p>
  </div>

  <div>
    <div class="introduce">Introduce</div>
    <div class="contract">
      <h1>조기취업형 계약학과 소개</h1>
    </div>

    <div class="image-container2">
      <div class="card" style="position: relative">
        <img class="round-img" src="@/assets/introduce1.png" alt="" />
        <div class="text-over-image2">
          <h2>스마트호스피탈리티학과</h2>
          <p style="color: #d6d6d6">
            현장 실무형 스마트호스피탈리티 인재 육성을 위해 교과과정 및
            실습교육을 진행합니다.
          </p>
          <button class="image-button">학과 바로가기</button>
        </div>
      </div>

      <div class="card" style="position: relative">
        <img class="round-img" src="@/assets/introduce2.png" alt="" />
        <div class="text-over-image2">
          <h2>미래형자동차학과</h2>
          <p style="color: #d6d6d6">
            미래형자동차 핵심 부품 기업과 협업을 통해 지속가능한 기술을
            선도합니다.
          </p>
          <button class="image-button">학과 바로가기</button>
        </div>
      </div>

      <div class="card" style="position: relative">
        <img class="round-img" src="@/assets/introduce3.png" alt="" />
        <div class="text-over-image2">
          <h2>소프트웨어융합학과</h2>
          <p style="color: #d6d6d6">
            IT 기술의 발전 흐름에 맞춰 전기전자, 컴퓨터, 기계 분야 중심으로
            인재를 양성합니다.
          </p>
          <button class="image-button">학과 바로가기</button>
        </div>
      </div>
    </div>
  </div>

  <div class="bg">
    <div class="news">News</div>
    <div class="contract2">
      <h1>사업단 소식</h1>
      <div
        style="
          text-align: left;
          word-wrap: break-word;
          padding-left: 20px;
          white-space: nowrap;
        "
      >
        동의대학교 조기취업형 계약학과 <br />
        사업단의 소식을 알려드립니다.
      </div>

      <button class="prev-button2">◀</button>
      <button class="next-button2">▶</button>
      <button class="image-button2">소식 더보기</button>
    </div>

    <div class="slide-container2">
      <div class="slide-img">
        <img class="slide2" src="@/assets/news1.png" alt="" />
        <div class="caption">
          미래형자동차학과 현대차블루핸즈(부산광역권) 간의 우수 인재 양성을 위한
          MOU체결식 개최
        </div>
        <div class="year">2023.12.07</div>
      </div>
      <div class="slide-img">
        <img class="slide2" src="@/assets/news2.jpg" alt="" />
        <div class="caption">
          스마트호스피탈리티학과 "제2회 호텔&레스토랑 산업전 참가"
        </div>
        <div class="year">2023.12.02</div>
      </div>
      <div class="slide-img">
        <img class="slide2" src="@/assets/new3.jpg" alt="" />
        <div class="caption">
          청년인턴이 바라본 규제 혁신현장-스마트호스피탈리티학과 김권동 교수
          인터뷰
        </div>
        <div class="year">2023.11.14</div>
      </div>
    </div>
  </div>

  <headerView class="header" />
  <router-view />
</template>

<script>
import HeaderView from "./components/HeaderView.vue";
export default {
  components: { HeaderView },
  data() {
    return {
      slideIndex: 0,
    };
  },
  mounted() {
    const slides = document.querySelectorAll(".slide");
    const totalSlides = slides.length;
    const slideContainer = document.querySelector(".slide-container");
    const prevBtn = document.querySelector(".prevBtn");
    const nextBtn = document.querySelector(".nextBtn");

    setInterval(() => {
      this.slideIndex++;
      if (this.slideIndex === totalSlides) this.slideIndex = 0;
      updateSlidePosition();
    }, 3000);

    prevBtn.addEventListener("click", () => {
      this.slideIndex--;
      if (this.slideIndex < 0) this.slideIndex = totalSlides - 1;
      updateSlidePosition();
    });
    nextBtn.addEventListener("click", () => {
      this.slideIndex++;
      if (this.slideIndex === totalSlides) this.slideIndex = 0;
      updateSlidePosition();
    });

    const updateSlidePosition = () => {
      slideContainer.style.transform =
        "translateX(" + this.slideIndex * -100 + "%)";
    };
  },
};
</script>

<style>
.slide-container {
  display: flex;
  transition: all 0.5s ease;
  width: 100%;
  height: 1350px;
  object-fit: cover;
}
.slide-container2 {
  display: flex;
  margin-left: 25%;
  margin-top: -14%;
  overflow: hidden;
}

.slide {
  flex: 1;
  text-align: center;
  font-size: 2em;
  /* padding: 20px; */
  box-sizing: border-box;
}

.slide-img {
  margin-left: 2%;
}

.slide2 {
  border-radius: 3%;
  width: 496px;
  height: 336px;
}

.caption {
  font-size: 24px;
  font-weight: bold;
  text-align: left;
}

.year {
  text-align: left;
  margin-top: 4%;
}

.prevBtn {
  position: absolute;
  margin-left: -30%;
  margin-top: -4%;
  border: none;
  background-color: rgb(255, 255, 255, 0);
  color: white;
  font-size: 1.2em; /* 버튼의 크기를 조정합니다. */
  z-index: 1;
}

.nextBtn {
  position: absolute;
  margin-top: -4%;
  margin-left: -27%;
  background-color: rgb(255, 255, 255, 0);
  border: none;
  color: white;
  font-size: 1.2em; /* 버튼의 크기를 조정합니다. */
  z-index: 1;
}

.prev-button2 {
  background-color: white;
  border: none;
  font-size: 1.2em;
  position: absolute;
  left: 15%;
  margin-top: 1.5%;
}

.next-button2 {
  background-color: white;
  border: none;
  font-size: 1.2em;
  position: absolute;
  margin-left: 11%;
  margin-top: 1.5%;
}

.header {
  position: fixed; /* 헤더를 고정 */
  top: 0; /* 상단에 위치 */
  width: 100%;
  opacity: 0.9;
}

#app {
  max-width: 100vw;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

.img-asd {
  position: relative;
  width: 100%;
  height: 75%;
}

body {
  margin: 0 !important;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.text-over-image {
  position: absolute;
  top: 40%;
  left: 8%; /* transform 대신 left 속성을 사용하여 위치를 설정합니다. */
  color: white;
  font-size: 64px;
  text-align: start;
}
.img-container {
  position: relative;
  overflow: hidden;
}
.bold {
  font-weight: bold;
}

.slide-container {
  display: flex;
}

.slide {
  flex: 0 0 100%; /* 각 슬라이드가 컨테이너의 전체 너비를 차지하도록 합니다. */
  transition: all 0.5s ease;
}

.img-title {
  margin: 0;
  padding: 25px 0;
  line-height: 75px;
}
.img-sub-title {
  font-size: 20px;
  margin: 0;
}

.introduce {
  color: blue;
  font-size: 22px;
  font-weight: bold;
  margin-top: -10%;
}

.news {
  color: blue;
  font-size: 22px;
  font-weight: bold;
  margin-right: 93%;
  margin-top: 25%;
}

.contract {
  font-size: 1.2em; /* 이 값을 조정하여 원하는 크기로 설정하실 수 있습니다. */
  color: #000;
}

.contract2 {
  font-size: 1.2em;
  color: #000;
  margin-right: 85%;
}

.image-container2 {
  display: flex;
  justify-content: center;
  align-items: center;
}

.round-img {
  margin: 10px;
  border-radius: 3%;
  width: 433px;
  height: 600px;
  padding: 0;
}

.card {
  width: 433px;
  height: 600px;
  margin: 0 10px;
}

.text-over-image2 {
  position: absolute;
  top: 58%;
  left: 11%;
  color: white;
  text-align: left;
}

.text-over-image2 h2 {
  font-size: 32px;
}
.image-button {
  position: absolute;
  display: inline-block;
  border: 1px solid #ededed;
  color: #ededed;
  background: transparent;
  padding: 17px 30px;
  text-decoration: none;
  border-radius: 25px;
}

.image-button2 {
  position: absolute;
  display: inline-block;
  border: 1px solid #1035d1;
  color: #1035d1;
  background: transparent;
  padding: 18px 34px;
  text-decoration: none;
  border-radius: 30px;
  font-size: 100%;
  font-weight: bold;
  left: 1%;
  margin-top: 5%;
}

.image-button:hover {
  background: blue;
  color: white;
}

.image-button2:hover {
  background: blue;
  color: white;
}

@media (max-width: 1600px) {
  .text-over-image {
    padding-left: 0;
    left: 1%;
    padding-left: 10px;
    top: 45%;
  }
}
@media (max-width: 1600px) {
  .prevBtn,
  .nextBtn {
    padding-right: 40%;
    top: 27%;
  }
}
</style>
