<template>
  <footer class="bg-gray-100 app-footer">
    <div class="container mx-auto px-0">
      <div class="px-2">
      <div class="flex -mx-2">
        <div class="w-1/3 px-2">
          <div class="bg-transparent h-12">
            ©  2021 MoovieTime. All rights reserved.
          </div>
        </div>
        <div class="w-1/3 px-2">
          <div class="bg-transparent h-12">
            <img
            class="lg:fill-current footer-img"
            src="~/assets/logo-footer.svg"
            alt=""
          />
          </div>
        </div>
        <div class="w-1/3 px-2">
          <div class="bg-transparent h-12 text-right">
            {{ footerText }}
          </div>
        </div>
      </div>
    </div>

    </div>

  </footer>
</template>

<script>
export default {
  data () {
    return {
      footerText: "Made with <INSERT_FRAMEWORK>",
    }
  },

}
</script>

<style>
.app-footer {
  height: 160px;
  background: #0000004A;
  display: flex;
  align-items: center;
}
.bg-transparent {
  color: #929292;
  font-size: 13px;
  font-weight: 400;
}
.footer-img {
  height: 24px;
  margin: auto;
}
</style>
