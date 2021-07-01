<template>
  <div>
    <div class="flex justify-center py-5">
      <div class="w-full sm:w-full md:w-full lg:w-full xl:w-full px-3 lg:px-4 xl:px-5 ">
        <div class="flex xl:mx-auto -mb-3 xl:mb-0 w-full sm:w-full md:w-full lg:w-full  xl:w-full 2xl:w-11/12">
          <div class=" w-8/12 sm:w-11/12 md:w-11/12 lg:w-11/12 xl:w-11/12 text-lg font-bold">Free Stock Photos</div>
          <div class="  w-4/12 md:w-2/12 lg:w-11/12 xl:w-1/12 leading-7 text-right font-normal ">
            <ul>
              <li class="dropdown "><a type="button" class="cursor-pointer text-sm font-bold inline-block "> Trending <i class="fas fa-caret-down "></i></a></li>
              <div class=" childContainer z-30 w-auto absolute   right-3 xl:right-5  2xl:right-20 py-3 leading-9 pt-2  ">
              <div class="child py-3 z-30">
              <i class="fas fa-sort-up"></i>
              <a href="#" class="block">Trending</a>
              <a href="#" class="block">New</a>
              </div>
            </div>
            </ul>
            
          </div>
        </div>
        <!-- End Sort -->
        <div class="flex xl:mx-auto w-full sm:w-full pt-5 xl:pt-0 xl:w-full 2xl:w-11/12 font-normal "> 
          <div class=" w-4/12 column mr-3 xl:mr-5">
            <FirstCol/>
          </div>
          <!-- EndFirst Column -->

          <div class=" w-4/12  column xl:mr-5">
            <SecondCol/>
          </div>

          <div class=" w-4/12  hidden xl:block column">
            <LastCol/>
          </div>
        </div>
        <!-- End Img -->
      </div>

    </div>
  </div>
</template>

<style>
 .childContainer{
    display: none;
    }

 .child i{
    position: absolute;
    top:-3px;
    left: 120px;
    font-size: 32px;
    color: whitesmoke!important;
    z-index:0;
  }
  .child{
    text-align: left;
    min-width: 175px;
    color: gray;
    background: rgb(248, 246, 246);
    border: solid 2px rgb(245, 245, 245);
    border-radius: 0.15rem;
    border: 1px solid whitesmoke;
   
  }

  .dropdown:hover + .childContainer{
    display: block !important;

  }

  .childContainer:hover{
    display: block !important;
  }
  .child a{
    padding: 0;
    margin: 0;
    font-weight: 400;
    padding-right: 20px;
    padding-left: 20px;
  }
  .child a:hover{
    background: rgba(128, 128, 128, 0.11);
  }
  /* Ends Small Dropdown */

.column {
  -ms-flex: 50%; /* IE 10 */
  flex: 50%;
}

.columnInner img {
  vertical-align: middle;
   z-index: 1;
}

.hiddenFeature{
  position: relative;
  /* padding: 15px 15px ; */
  margin-top: -68px;
}
/* .hiddenFeature{
 display: none;
} */

.columnInner:hover .hiddenFeature{
  display: flex;
}
</style>
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
        'https://api.pexels.com/v1/search?query=family&per_page=10',{
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

