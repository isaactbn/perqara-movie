<template>
  <div class="w-full view-wrapper py-12 lg:py-24">
    <div class="container mx-auto">

      <!-- BATAS -->

      <!-- BATAS -->


      <div class="container">
        <hr class="top-line-title">
        <h3 class="font-semibold text-2xl mt-3 mb-5 discover-title">Movies</h3>

        <div class="flex flex-col lg:flex-row justify-between mb-4 lg:mb-8">
          <div
            class=" rounded text-center bg-transparent shadow w-1/5 mb-4 lg:mb-0 lg:mr-8"
          >
            <div
              class="filter-menu text-left shadow mb-4 lg:mb-0"
            >
              <span class="filter-title">Sort Result By</span>

              <hr class="sidebar-line">
             
              <span class="filter-title">Genres</span>

              <div
                v-for="item in checkList"
                class="mt-[18px] mb-[17px] block"
              >
                <input
                  class="relative float-right h-[1.125rem] w-[1.125rem] appearance-none rounded-[0.25rem] border-[0.125rem] border-solid border-neutral-300 before:pointer-events-none before:absolute before:h-[0.875rem] before:w-[0.875rem] before:scale-0 before:rounded-full before:bg-transparent before:opacity-0 before:shadow-[0px_0px_0px_13px_transparent] before:content-[''] checked:border-primary checked:bg-primary checked:before:opacity-[0.16] checked:after:absolute checked:after:-mt-px checked:after:ml-[0.25rem] checked:after:block checked:after:h-[0.8125rem] checked:after:w-[0.375rem] checked:after:rotate-45 checked:after:border-[0.125rem] checked:after:border-l-0 checked:after:border-t-0 checked:after:border-solid checked:after:border-white checked:after:content-[''] hover:cursor-pointer hover:before:opacity-[0.04] hover:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:shadow-none focus:transition-[border-color_0.2s] focus:before:scale-100 focus:before:opacity-[0.12] focus:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:before:transition-[box-shadow_0.2s,transform_0.2s] focus:after:absolute focus:after:z-[1] focus:after:block focus:after:h-[0.875rem] focus:after:w-[0.875rem] focus:after:rounded-[0.125rem] focus:after:content-[''] checked:focus:before:scale-100 checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca] checked:focus:before:transition-[box-shadow_0.2s,transform_0.2s] checked:focus:after:-mt-px checked:focus:after:ml-[0.25rem] checked:focus:after:h-[0.8125rem] checked:focus:after:w-[0.375rem] checked:focus:after:rotate-45 checked:focus:after:rounded-none checked:focus:after:border-[0.125rem] checked:focus:after:border-l-0 checked:focus:after:border-t-0 checked:focus:after:border-solid checked:focus:after:border-white dark:border-neutral-600 dark:checked:border-primary dark:checked:bg-primary dark:focus:before:shadow-[0px_0px_0px_13px_rgba(255,255,255,0.4)] dark:checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca]"
                  type="checkbox"
                  value=""
                  id="checkboxDefault"
                  :checked="item.isChecked"
                />
                <label
                  class="checkbox-label inline-block hover:cursor-pointer"
                  for="checkboxDefault">
                  {{ item.name }}
                </label>
              </div>

            </div>
          </div>

          <div
            style="flex-direction: column;"
            class="flex flex-col lg:flex-row justify-between w-4/5 mb-4"
          >
          
            <v-row
              v-for=" (item, sequence) in Math.ceil(newDate.length / 4) + 1"
              :key="sequence"
              style="justify-content: center; width: 100%; display: flex; justify-content: flex-start;"
              class="mt-10"
              cols="7"
              justify="center"
            >
              <div
                v-for="(n, index) in newDate.slice(sequence == 1 ? 0 : ((sequence * 4) - 4), sequence == 1 ? 4 : (sequence * 4))"
                :key="index"
                class=" rounded text-center bg-transparent shadow w-1/4 mb-4 lg:mb-0"
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
                    <nuxt-link to="/detail">
                      <div class="button-view bg-white">
                        View
                      </div>
                    </nuxt-link>
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
      checkList: [
        {
          name: "Action",
          isChecked: true
        },
        {
          name: "Adventure",
          isChecked: false
        },
        {
          name: "Animation",
          isChecked: false
        },
        {
          name: "Comedy",
          isChecked: false
        },
        {
          name: "Crime",
          isChecked: false
        },
        {
          name: "Documentary",
          isChecked: false
        },
        {
          name: "Drama",
          isChecked: false
        },
        {
          name: "Family",
          isChecked: false
        },
        {
          name: "Fantasy",
          isChecked: false
        },
        {
          name: "History",
          isChecked: false
        },
        {
          name: "Horor",
          isChecked: false
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
.filter-menu {
  height: 586px;
  padding: 20px 18px;

  background: linear-gradient(180deg, #0E1723 0%, rgba(30, 35, 42, 0) 100%);
  border-radius: 8px;
}
.filter-title {
  color: #E5E5E5;
  font-size: 16px;
  font-weight: 600;
}
.checkbox-label {
  font-weight: 400;
  font-size: 14px;
  color: #FFFFFF;
}
.sidebar-line {
  margin: 18px -18px;
  border: 1px solid rgba(255, 255, 255, 0.07);
  height: 0;
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
