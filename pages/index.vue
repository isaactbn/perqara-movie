<template>
  <div class="w-full view-wrapper py-12 lg:py-24">
    <div class="container mx-auto px-5">

      <!-- BATAS -->
      <vue-slick-carousel class="h-364" v-bind="settings">
        <div class="main-banner mt-6">
          <div
            v-bind:style="{ 'background-image': 'url(' + 'banner2.png' + ')' }"
            class="main-banner-img"
          />
          <div class="main-banner-desc">
            <div style="font-size: 36px; width: 100px; max-width: 100px;" class="main-rating bg-white">
              <img
                class="ic-star-banner mr-1"
                src="~/assets/star.svg"
                alt=""
              />
              7.0
            </div>
            <h1 class="main-title">Space Sweepers</h1>
            <span class="main-genre mt-3">2020 * Sci-Fi</span>
            <p class="main-desc mt-3">
              When the crew of a space junk collector ship called The Victory discovers a humanoid robot named Dorothy that's known to be a weapon of mass destruction, they get involved in a risky business deal which puts their lives at stake.
            </p>
          </div>
        </div>

        <div class="main-banner mt-6">
          <div
            v-bind:style="{ 'background-image': 'url(' + 'banner1.png' + ')' }"
            class="main-banner-img"
          />
          <div class="main-banner-desc">
            <div style="font-size: 36px; width: 100px; max-width: 100px;" class="main-rating bg-white">
              <img
                class="ic-star-banner mr-1"
                src="~/assets/star.svg"
                alt=""
              />
              7.0
            </div>
            <h1 class="main-title">Space Sweepers</h1>
            <span class="main-genre mt-3">2020 * Sci-Fi</span>
            <p class="main-desc mt-3">
              When the crew of a space junk collector ship called The Victory discovers a humanoid robot named Dorothy that's known to be a weapon of mass destruction, they get involved in a risky business deal which puts their lives at stake.
            </p>
          </div>
        </div>

        <div class="main-banner mt-6">
          <div
            v-bind:style="{ 'background-image': 'url(' + 'banner3.png' + ')' }"
            class="main-banner-img"
          />
          <div class="main-banner-desc">
            <div style="font-size: 36px; width: 100px; max-width: 100px;" class="main-rating bg-white">
              <img
                class="ic-star-banner mr-1"
                src="~/assets/star.svg"
                alt=""
              />
              7.0
            </div>
            <h1 class="main-title">Space Sweepers</h1>
            <span class="main-genre mt-3">2020 * Sci-Fi</span>
            <p class="main-desc mt-3">
              When the crew of a space junk collector ship called The Victory discovers a humanoid robot named Dorothy that's known to be a weapon of mass destruction, they get involved in a risky business deal which puts their lives at stake.
            </p>
          </div>
        </div>
        <div class="main-banner mt-6">
          <div
            v-bind:style="{ 'background-image': 'url(' + 'banner1.png' + ')' }"
            class="main-banner-img"
          />
          <div class="main-banner-desc">
            <div style="font-size: 36px; width: 100px; max-width: 100px;" class="main-rating bg-white">
              <img
                class="ic-star-banner mr-1"
                src="~/assets/star.svg"
                alt=""
              />
              7.0
            </div>
            <h1 class="main-title">Space Sweepers</h1>
            <span class="main-genre mt-3">2020 * Sci-Fi</span>
            <p class="main-desc mt-3">
              When the crew of a space junk collector ship called The Victory discovers a humanoid robot named Dorothy that's known to be a weapon of mass destruction, they get involved in a risky business deal which puts their lives at stake.
            </p>
          </div>
        </div>
      </vue-slick-carousel>
      <!-- BATAS -->


      <div class="container mt-12">
        <hr class="top-line-title">
        <h3 class="font-semibold text-2xl mt-3 mb-5 discover-title">Discover Movies</h3>

        <div class="flex flex-col lg:flex-col justify-between mb-4 lg:mb-8">
          
          <v-row
            v-for=" (item, sequence) in Math.ceil(newDate.length / 5) + 1"
            :key="sequence"
            style="justify-content: center; width: 100%; display: flex; justify-content: flex-start;"
            class="mt-10"
            cols="7"
            justify="center"
          >
            <div
              v-for="(n, index) in newDate.slice(sequence == 1 ? 0 : ((sequence * 5) - 5), sequence == 1 ? 5 : (sequence * 5))"
                :key="index"
              class=" rounded text-center bg-transparent shadow w-1/5 mb-4 lg:mb-0 lg:mr-8"
            >
              <div
                v-bind:style="{ 'background-image': 'url(' + n.image + ')' }"
                class="img-wrapper"
              >
                <div class="img-hover lg:fill-current">
                  <div class="rating-hover bg-white">
                    <img
                      class="ic-star"
                      src="~/assets/star.svg"
                      alt=""
                    />
                    {{ n.rating }}
                  </div>
                  <div class="genre-hover bg-white">
                    Action
                  </div>
                  <nuxt-link to="/detail">
                    <div class="button-view bg-white">
                      View
                    </div>
                </nuxt-link>
                </div>
                <div class="rating-view bg-white">{{ n.rating }}</div>
              </div>
              <div class="movie-title text-xl text-gray-600">{{ n.title }}</div>
              <div class="sub-title text-xl text-gray-600">{{ n.title }}</div>
            </div>
          </v-row>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  layout: "home",
  components: {
    VueSlickCarousel,
  },
  data() {
    return {
      settings: {
        dots: true,
        infinite: true,
        rows: 1,
        initialSlide: 1,
        speed: 500,
        slidesToShow: 2,
        slidesToScroll: 1,
        swipeToSlide: true,
        arrows: true,
      },
      newDate: [
        {
          id: "1",
          rating: "7.0",
          image: "img.png",
          title: "Wonder Woman 1984",
          year: "2020"
        },
        {
          id: "2",
          rating: "7.1",
          image: "img2.png",
          title: "Below Zero",
          year: "2021"
        },
        {
          id: "3",
          rating: "7.2",
          image: "img3.png",
          title: "The Little Things",
          year: "2021"
        },
        {
          id: "4",
          rating: "7.3",
          image: "img4.png",
          title: "Outside the Wire",
          year: "2021"
        },
        {
          id: "5",
          rating: "7.4",
          image: "img5.png",
          title: "Black Water: Abyss",
          year: "2020"
        },
        {
          id: "6",
          rating: "7.5",
          image: "img6.png",
          title: "Breach",
          year: "2021"
        },
        {
          id: "7",
          rating: "7.6",
          image: "img7.png",
          title: "Soul",
          year: "2020"
        },
        {
          id: "8",
          rating: "7.7",
          image: "img8.png",
          title: "Fast & Furious Present..",
          year: "2019"
        },
        {
          id: "9",
          rating: "7.7",
          image: "img9.png",
          title: "The Croods: A New Age",
          year: "2020"
        },
        {
          id: "10",
          rating: "7.3",
          image: "img10.png",
          title: "Vanguard",
          year: "2019"
        },
      ],
    };
  },
  created() {
  },
  methods: {
  }
};
</script>

<style>
.main-banner {
  width: fit-content !important;
  height: 364px;
  /* background: rgba(0, 0, 0, 0.5); */
  display: flex !important;
  justify-content: flex-start;
  align-items: center;
}
.main-banner-img {
  z-index: 9999;
  width: 243px;
  height: 364px;
  max-height: 330px;
  background-size: cover;
}
.main-banner-desc {
  width: 300px;
  height: 300px;
  background: #000000;
  padding: 25px;
}
.main-title {
  font-weight: 500;
  font-size: 28px;
  color: #FFFFFF;
}
.main-genre {
  font-weight: 400;
  font-size: 16px;
  color: #FFFFFF;
}
.main-rating {
  background: transparent;
  width: 48px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 18px;
  color: #FFFFFF;
}
.main-desc {
  font-weight: 400;
  font-size: 12px;
  color: #FFFFFF;
}
.view-wrapper {
  background-color: #1E232B;
}
.discover-title {
  color: #E5E5E5;
}
.top-line-title {
  background: #E74C3C;
  width: 112px;
  height: 6px;
  border: none;
}
.img-wrapper {
  height: 330px;
  max-height: 330px;
  display: flex;
  flex-direction: column;
  align-items: end;
  background-size: cover;
}
.rating-view {
  position: absolute;
  background: #1E232BCC;
  width: 48px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #E5E5E5;
  font-size: 18px;
  font-weight: 700;
}
.img-hover {
  opacity: 0;
  width: 100%;
  height: 330px;
  max-height: 330px;
  padding: 40px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  background: rgba(0, 0, 0, 0.8);
  transition: 0.3s;
}
.img-hover:hover {
  opacity: 1;
}
.ic-star-banner {
  width: 16px;
  height: 16px;
}
.ic-star {
  width: 32px;
  height: 32px;
}
.rating-hover {
  background: transparent;
  width: 48px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #E5E5E5;
  font-size: 24px;
  font-weight: 600;
}
.genre-hover {
  background: transparent;
  width: 48px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #E5E5E5;
  font-size: 18px;
  font-weight: 600;
}
.button-view {
  width: 107px;
  height: 32px;
  cursor: pointer;
  border-radius: 32px;
  background: #FF0000;

  display: flex;
  align-items: center;
  justify-content: center;
  color: #E5E5E5;
  font-weight: 700;
  font-size: 14px;
}
.movie-title {
  text-align: left;
  color: #E5E5E5;
  font-size: 16px;
  font-weight: 600;
}
.sub-title {
  text-align: left;
  color: #929292;
  font-size: 14px;
  font-weight: 400;
}
</style>
