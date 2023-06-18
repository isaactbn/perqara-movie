<template>
  <div class="w-full view-wrapper">
    <div>

      <!-- BATAS -->
      <div
        class="banner-wrapper bg-white"
      >
        <div
          v-bind:style="{ 'background-image': 'url(' + 'banner-detail.png' + ')' }"
          class="banner-img mb-10"
        >

          <div class="banner-box mt-6">
            <div
              v-bind:style="{ 'background-image': 'url(' + 'img.png' + ')' }"
              class="img-wrapper-banner lg:mr-[10px] lg:ml-[10px]"
            />

            <div style="font-size: 36px; width: 100px; max-width: 100px;" class="rating-hover bg-white">
              <img
                class="ic-star mr-4"
                src="~/assets/star.svg"
                alt=""
              />
              7.0
            </div>

            <div class="banner-box-label ml-3">
              <span class="banner-title-label">User Score</span>
              <span class="banner-title-value">3621 Votes</span>
            </div>

            <div class="vertical-line" />

            <div class="banner-box-label ml-3">
              <span class="banner-title-label">Status</span>
              <span class="banner-title-value">Released</span>
            </div>

            <div class="vertical-line" />

            <div class="banner-box-label ml-3">
              <span class="banner-title-label">Budget</span>
              <span class="banner-title-value">$200,000,000.00</span>
            </div>

            <div class="vertical-line" />

            <div class="banner-box-label ml-3">
              <span class="banner-title-label">Production</span>
              <span class="banner-title-value">DC Entertainment</span>
            </div>
          </div>

          <div class="banner-title">
            <span style="font-weight: 500; font-size: 18px; color: #FFFFFF;">2020</span>
            <span style="font-weight: 600; font-size: 36px; color: #E5E5E5;">Wonder Woman 1984</span>
            <span style="font-weight: 500; font-size: 14px; color: #FFFFFF;">Fantasy, Action, Adventure</span>
          </div>
        </div>

        <div class="reviews">
          <h1 class="review-title mb-7">REVIEWS</h1>

          <div class="flex w-full">
            <div class="content-wrapper shadow w-1/2 lg:mr-4">
              <div class="content-card">

                <div class="flex justify-between">
                  <div class="flex">
                    <div class="user-image">
                      <img
                        class="user-img"
                        src="~/assets/img.png"
                        alt=""
                      />
                    </div>

                    <div class="user-profile ml-5">
                      <span class="user-name">SWITCH.</span>
                      <span class="date-review">December 18, 2020</span>
                    </div>
                  </div>

                  <div class="user-rating flex justify-center">
                    <img
                      class="user-star mr-2"
                      src="~/assets/star.svg"
                      alt=""
                    />
                    7.0
                  </div>
                </div>

                <p class="mt-8">
                  It isn't as easy as saying 'Wonder Woman 1984' is a good or bad movie. The pieces are there, and there are moments I adore, but it does come across as a bit of a mess, even though the action sequences are breathtaking. If you're a fan of the original film, you'll be more willing to take the ride, but for those more indifferent, it may be a bit of a blander sit. If you can and are planning to watch it, the theatrical experience is the way to go - there is nothing like seeing these stunning sets, fun action scenes and hearing Zimmer's jaw-dropping score like on the big screen. - Chris dos Santos... read the rest.
                </p>
                
              </div>
            </div>
            <div class="content-wrapper shadow w-1/2 lg:ml-4">
              <div class="content-card">

                <div class="flex justify-between">
                  <div class="flex">
                    <div class="user-image">
                      <img
                        class="user-img"
                        src="~/assets/img.png"
                        alt=""
                      />
                    </div>

                    <div class="user-profile ml-5">
                      <span class="user-name">SWITCH.</span>
                      <span class="date-review">December 18, 2020</span>
                    </div>
                  </div>

                  <div class="user-rating flex justify-center">
                    <img
                      class="user-star mr-2"
                      src="~/assets/star.svg"
                      alt=""
                    />
                    7.0
                  </div>
                </div>

                <p class="mt-8">
                  It isn't as easy as saying 'Wonder Woman 1984' is a good or bad movie. The pieces are there, and there are moments I adore, but it does come across as a bit of a mess, even though the action sequences are breathtaking. If you're a fan of the original film, you'll be more willing to take the ride, but for those more indifferent, it may be a bit of a blander sit. If you can and are planning to watch it, the theatrical experience is the way to go - there is nothing like seeing these stunning sets, fun action scenes and hearing Zimmer's jaw-dropping score like on the big screen. - Chris dos Santos... read the rest.
                </p>

                </div>
            </div>
          </div>
        </div>
        
      </div>
      <!-- BATAS -->


      <div style="padding: 0 62px;" class="container mx-auto">
        <h3 class="font-semibold text-2xl mt-12 mb-10 discover-titles">RECOMMENDATION MOVIES</h3>

        <div class="mb-4 lg:mb-8">

          <div
            style="flex-direction: column;"
            class="flex flex-col lg:flex-row justify-between mb-4"
          >
          
            <v-row
              v-for=" (item, sequence) in Math.ceil(newDate.length / 5) + 1"
              :key="sequence"
              style="justify-content: center; width: 100%; display: flex; justify-content: flex-start;"
              cols="7"
              justify="center"
            >
              <div
                v-for="(n, index) in newDate.slice(sequence == 1 ? 0 : ((sequence * 5) - 5), sequence == 1 ? 5 : (sequence * 5))"
                :key="index"
                class=" rounded text-center bg-transparent shadow w-1/5 mb-4 lg:mb-0"
              >
                <div
                  v-bind:style="{ 'background-image': 'url(' + n.image + ')' }"
                  class="img-wrapper lg:mr-[10px] lg:ml-[10px]"
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
                    <div class="button-view bg-white">
                      View
                    </div>
                  </div>
                  <div class="rating-view bg-white">{{ n.rating }}</div>
                </div>
                <div class="movie-title text-xl text-gray-600">{{ n.title }}</div>
                <div class="sub-title text-xl text-gray-600">{{ n.year }}</div>
              </div>
            </v-row>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  layout: "home",
  components: {
  },
  data() {
    return {
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
      ]
    };
  },
  created() {
    console.log('cek array count', (this.newDate.length / 4) + 1)
  },
  methods: {
  }
};
</script>

<style>
.banner-wrapper {
  width: 100%;
}
.banner-img {
  width: 100%;
  height: 468px;
  max-height: 468px;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  flex-direction: column-reverse;
  align-items: stretch;
}
.banner-box {
  width: 100%;
  height: 80px;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 124px;
}
.banner-title {
  padding: 0 371px;
  display: flex;
  flex-direction: column;
}
.banner-box-label {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.banner-title-label {
  font-weight: 500;
  font-size: 12px;
  text-transform: uppercase;
  color: rgba(255, 255, 255, 0.5);
}
.banner-title-value {
  font-weight: 500;
  font-size: 12px;
  text-transform: uppercase;
  color: #FFFFFF;
}
.vertical-line {
  width: 0;
  height: 41px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  margin: 0 33px;
}
.reviews {
  padding: 0 124px;
  margin-top: 200px;
}
.review-title {
  font-weight: 600;
  font-size: 14px;
  color: #FF0000;
}
.content-wrapper {
  border: none;
  margin-bottom: 58px;
}
.content-card {
  height: 284px;
  padding: 24px;
  background: #F9F9F9;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.1);
  border-radius: 14px;
}
.user-img {
  width: 48px;
  height: 48px;
  border-radius: 50%;

  background: rgba(30, 35, 43, 0.21);
}
.user-profile {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}
.user-name {
  font-weight: 700;
  font-size: 14px;
  color: #1E232A;
}
.date-review {
  font-weight: 400;
  font-size: 12px;
  color: #666666;
}
.user-rating {
  width: 97px;
  height: 52px;

  background: rgba(196, 196, 196, 0.28);
  border-radius: 7px;
  align-items: center;

  font-weight: 600;
  font-size: 36px;
  color: #000000;
}
.user-star {
  width: 17px;
  height: 17px;
  margin-top: -8px;
}
p {
  font-weight: 400;
  font-size: 13px;
  line-height: 150%;
  color: #000000;
}
.sidebar-line {
  margin: 18px -18px;
  border: 1px solid rgba(255, 255, 255, 0.07);
  height: 0;
}
.view-wrapper {
  background-color: #1E232B;
}
.discover-titles {
  font-weight: 600;
  font-size: 14px;
  color: #FFFFFF;
}
.top-line-title {
  background: #E74C3C;
  width: 112px;
  height: 6px;
  border: none;
}
.img-wrapper-banner {
  width: 220px;
  height: 330px;
  max-height: 330px;
  background-size: cover;
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
.ic-star {
  width: 32px;
  height: 32px;
}
.rating-hover {
  background: transparent;
  width: 48px;
  height: 32px;
  margin-left: 29px;
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
