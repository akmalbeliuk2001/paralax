<template>
  <div>
    <div id="app">
      <div class="swiper openingSwiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <div class="content">
              <h2>Hallo</h2>
            </div>
          </div>
          <div class="swiper-slide">Slide 2</div>
          <div class="swiper-slide">Slide 3</div>
          <div class="swiper-slide">Slide 4</div>
          <div class="swiper-slide">Slide 5</div>
          <div class="swiper-slide">Slide 6</div>
          <div class="swiper-slide">Slide 7</div>
          <div class="swiper-slide">Slide 8</div>
          <div class="swiper-slide">Slide 9</div>
        </div>
        <div class="swiper-pagination"></div>
      </div>
    </div>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quisquam animi
      expedita maxime veniam quod, voluptatum eveniet illum totam beatae?
      Repellat temporibus dolor velit quibusdam, quaerat ratione, quas soluta
      aliquid impedit consectetur voluptatem doloremque nulla commodi
      praesentium molestias laboriosam eos magnam laudantium tempora voluptas
      nobis natus. Nostrum ea quod incidunt esse.
    </p>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  components: {
    // HelloWorld
  },
  data() {
    return {
      openingSwiper: null,
    };
  },
  methods: {
    initOpeningSwiper() {
      /* eslint-disable */
      this.openingSwiper = new Swiper(".openingSwiper", {
        direction: "horizontal",
        slidesPerView: 1,
        effect: "fade",
        spaceBetween: 30,
        mousewheel: true,
        // pagination: {
        //   el: ".swiper-pagination",
        //   clickable: true,
        // },
      });
    },
  },
  mounted() {
    this.initOpeningSwiper();
  },
};
</script>

<style>
#app {
  height: 100vh;
}
html,
body {
  position: relative;
  height: 100%;
}

body {
  background: #eee;
  font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
  font-size: 14px;
  color: #000;
  margin: 0;
  padding: 0;
}

.swiper,
.swiper-slide {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.content {
  width: 100%;
  height: 100%;
  background-color: aquamarine;
}
.content > h2 {
  position: fixed;
  left: 50%;
  transform: translate(-50%, -50%);
  top: 50%;
}
</style>
