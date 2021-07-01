<template>
  <div>
    <div class="columnInner cursor-pointer  "  v-for="photo in photos.photos" :key="photo.id">
      <img class=" mt-3 xl:mt-6 " :src="photo.src.large2x"/>
      <div class="hiddenFeature sm:flex lg:hidden xl:hidden 2xl:hidden w-full bg-gradient-to-t from-black to-gray-10 bg-opacity-70 pt-4 pb-4  pl-4 cursor-pointer ">
        <div class="w-8/12 lg:w-9/12 text-white">
        <span class=" hidden lg:block ">
          <a href="#">
              <img class=" inline-block w-10  rounded-2xl" src="../assets/img/user.jpeg"/> 
              <span class=" inline-block px-2 "> {{ photo.photographer }} </span>
          </a>
          </span>
        </div>
        <div  class="w-11/12 lg:w-3/12 text-white leading-9 text-xl font-bold pr-0 sm:pr-3 md:pr-3 lg:pr-0">
        <span class="inline-block float-right lg:float-none"><a href="#"><i class="las la-download block"></i></a></span>
        <span class="inline-block"><a href="#"><i class="las la-plus-circle hidden lg:block ml-2 mr-2"></i></a></span>
        <span class="inline-block"><a href="#"><i class="far fa-heart hidden lg:block "></i></a></span>
        </div>
      </div>
      <!-- End Hidden Features -->
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        photos: []
      }
    },

    activated() {
      // Call fetch again if last fetch more than 30 sec ago
      if (this.$fetchState.timestamp <= Date.now() - 30000) {
        this.$fetch()
      }
    },

    async fetch() {
      let photoList = await fetch(
        'https://api.pexels.com/v1/search?query=technology&per_page=10',{
          method: 'GET', 
          headers: {
            'Authorization':'563492ad6f91700001000001ddb6c584efa74c9d80065f624f000434',
            'Content-Type': 'application/json',
          }
        }
      ).then(res => res.json())
    
      this.photos = photoList
        // console.log(photoList);

    }
  }
</script>

