<template>
  <header class="bg-white flex items-center justify-between px-2 shadow">
    <div class=" flex-1 p-4 d-flex align-items-center justify-content-start">
      <nuxt-link to="/">
       <img src="~/assets/media/logo3.jpeg" style="width:38px;height:38px;object-fit:contain" alt="">
      </nuxt-link>
    </div>
    <div class="p-4 d-flex align-items-center justify-content-end">
      <nuxt-link v-if="location=='/'" to="/inscription">
        <button
          class="
            btn btn-success btn-active-light-info
            py-1
            fs-4
            px-4
            border border-blue-100
            rounded
          "
        >
          Quiz
        </button>
      </nuxt-link>
    </div>
  </header>
</template>
<script>

export default {
  data(){
    return {
      location:null
    }
  },
  mounted(){
   this.location = location.pathname
  }
}
</script>

<style scoped>
header {
  height: 60px;
  position: sticky;
  top: 0%;
}
</style>
