<template>
  <nav class="w-full fixed shadow-xs navbar-custom">
    <div class="container lg:mx-auto">
      <div class="flex">
        <div class="max-w-sm flex items-center flex-shrink-0 text-white mr-6 lg:p-0 pl-6 py-2">
          <img
            class="lg:fill-current nav-img"
            src="~/assets/icon.svg"
            alt=""
          />
        </div>
        <div class="lg:relative fixed bottom-0 w-full h-14 py-2">
          <ul class="flex flex-row lg:justify-end justify-between text-center ml-3">
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link class="button-link" to="/" :class="activeLink('/')">
                <img
                    class="lg:fill-current nav-ic"
                    src="~/assets/ic-category.svg"
                    alt=""
                  />
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Categories</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <nuxt-link to="/movies" :class="activeLink('/movies')">
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Movies</span>
              </nuxt-link>
            </li>
            <li class="flex-1 lg:flex-none mr-2">
              <!-- <nuxt-link to="/" :class="activeLink('/')"> -->
                <span class="lg:text-base text-super-xs lg:text-white pb-1">Login</span>
              <!-- </nuxt-link> -->
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    activeLink(link) {
      let isActive = this.isActiveLink(link);
      return isActive
        ? "flex flex-col text-white lg:border-b-2 lg:border-white lg:pb-2 lg:mr-5"
        : "flex flex-col lg:border-b-2 lg:border-gray-400 lg:border-none lg:pb-2 lg:mr-5";
    },
    isActiveLink(link) {
      let firtspath = this.$route.path.split("/")[1];
      return link == "/" + firtspath;
    }
  }
};
</script>

<style>
.navbar-custom {
  display: flex;
  align-items: center;
  background-color: #FFFFFF0D;
  height: 66px;
}
.nav-img {
  width: 112px;
  height: 31px;
}
.button-link {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.nav-ic {
  width: 20px;
  height: 20px;
  margin-right: 11px;
}
@media (min-width: 1024px) {
}
</style>
