<template>
  <div class="flex-row  py-0  md:py-10  lg:py-16  xl:py-16 md:mb-30 pb-20 justify-center px-4  md:px-0 lg:px-0 ">
      <div class="text-4xl mx-auto pt-0 mt-10 sm:w-11/12 md:w-10/12 lg:w-8/12  xl:w-5/12 2xl:w-5/12 font-extrabold leading-10 text-white ">
        The best free stock photos & videos shared by talented creators.
      </div>
      <div class="mx-auto md:max-w-full md:mb-20 md:w-10/12 lg:w-8/12  xl:w-5/12 mt-4  ">
        <div class="  md:my-5 py-0 md:py-2  px-4 pr-0 sm:pr-0  md:pr-0 lg:pr-0 lg:px-4  rounded-lg bg-white searchInput ">
        <input type="text"  placeholder="Search for free videos and photos" class=" text-gray-500 mr-0 md:mr-4 lg:mr-4  xl:mr-4 py-4 lg:py-3 shadow-none  focus:outline-none font-light w-11/12 md:w-11/12 lg:w-11/12 xl:w-11/12 " />
        <i class="las la-search text-sm md:text-xl xl:text-xl pb-1 font-black text-gray-500"> </i> 
        </div>
        <div class=" mt-3 md:-mt-3 xl:-mt-2 text-sm"><span class="text-white font-sm pr-3 hidden xl:inline-block">Suggested: </span> <span class="text-gray-300 font-normal text-sm"> ice cream  online shopping  healthy food  city night  hair  islamic  more </span></div>
      </div>  
    </div>
    <!-- End Header Search Section-->
</template>
<style>
  .hero-img{
    background: url("../assets/img/p1.jpeg") no-repeat;
    background-position: center;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
  }
  .searchInput i{
    -webkit-transform: rotate(270deg);
    -moz-transform: rotate(270deg);
    -ms-transform: rotate(270deg);
    -o-transform: rotate(270deg);
    transform: rotate(270deg);
  }

  .effect{
    transition: 0.5s;
  }
  .effect:hover{
    margin-top: -1px;
    /* transform: scale(1.1); */
  }
</style>