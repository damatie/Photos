<template>
  <div class="flex py-0 pt-3 px-4">
    <div class="flex-none md:flex text-xl font-bold text-gray-200 leading-10"><img src="../assets/img/p logo.png" class=" h-10 pr-4"/> <span class="md:block hidden">Pexels</span></div>
    <div class=" flex-1 "></div>
    <div class=" flex px-5">
      <nav class="TopNav md:block hidden">
        <ul class="leading-10 text-white font-normal ">
          <li class="dropdown "><a href="#" class=" px-4 hover:text-gray-100  ">Explore</a></li>
            <div class="child py-3 leading-9 ">
              <i class="fas fa-sort-up"></i>
              <a href="#" class="block">Discover Photos</a>
              <a href="#" class="block ">Popular Searches</a>
              <a href="#" class="block">Leaderboard</a>
              <a href="#" class="block">Challenges</a>
              <a href="#" class="block">Leaderboard</a>
              <a href="#" class="block">Pexels Blog</a>
            </div>
          <li><a href="#" class="px-4 hover:text-gray-200 ">License</a></li>
          <li><a href="#" class="px-4 hover:text-gray-200">Upload</a></li>
        </ul>
        
      </nav>
      <!--End Nav Links -->
    </div>
    <div class=" flex-none leading-1">
      <a href="#" class=" dropdownMd  pl-0 pr-6 align-bottom text-white hover:text-gray-200   "><i class="las la-ellipsis-h font-extrabold text-3xl "></i></a>
      <div class="childMd py-3 leading-9">
        <i class="fas fa-sort-up"></i>
        <a href="#" class="block ">Login</a>
        <a href="#" class="block  ">Join</a>
        <a href="#" class="block ">Change Language <img class=" w-8 inline-flex" src="../assets/img/flag.png"/></a>
        <a href="#" class="block ">Image & Video Api</a>
        <a href="#" class="block ">Apps & Plugins</a>
        <a href="#" class="block ">FAQ</a>
        <a href="#" class="block ">Partnership</a>
        <a href="#" class="block ">Imprint & Terms</a>
        <div class="flex px-2 mt-4 childMdFooter">
          <div class="px-1"><a href="#" class="block ">
            <i class="lab la-facebook-f"></i>
          </a></div>
          <div class="px-1"><a href="#" class="block "><i class="lab la-twitter"></i></a></div>
          <div class="px-1"><a href="#" class="block "><i class="lab la-instagram"></i></a></div>
          <div class="px-1"><a href="#" class="block "><i class="lab la-pinterest-p"></i></a></div>
          <div class="px-1"><a href="#" class="block "><i class="lab la-youtube"></i></a></div>
        </div>
      </div>
      <a href="#" class="inline-block rounded effect text-base
    bg-green-600 py-2 text-gray-100 px-7 font-bold hover:bg-green-800">Join</a></div>
  </div>
</template>
<style scoped>
  .TopNav ul{
    list-style: none;
    }
  .TopNav ul li{
    display: block;
    display: inline-block;
  }
  
 .child i{
    position: absolute;
    top:-12px;
    left: 140px;
    font-size: 32px;
    color: white !important;
    z-index: -1;
  }

  .child{
    min-width: 170px;
    display: none;
    color: gray;
    background: white;
    position: absolute;
    border: solid 1px whitesmoke;
    border-radius: 0.15rem;
    right: 380px;
    box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.308);
    /* border: 1px solid whitesmoke; */
    z-index: 2;
  }

  .dropdown:hover +  .child{
    display: block !important;
  }

  .child:hover{
    display: block !important;
    position: absolute;
  }
  .child a{
    padding: 0;
    margin: 0;
    /* font-size: 15px; */
    font-weight: 500;
    padding-right: 20px;
    padding-left: 20px;
  }
  .child a:hover{
    background: rgba(128, 128, 128, 0.11);
  }
  /* Ends Small Dropdown */

   .childMd i{
    position: absolute;
    top:-12px;
    left: 325px;
    font-size: 32px;
    color: white !important;
    z-index: -1;
  }

  .childMd{
    /* min-width: 330px; */
    display: none;
    color: gray;
    background:white;
    position: absolute;
    border-radius: 0.15rem;
    right: 130px;
    border: solid 1px whitesmoke;
    box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.308);
    /* border: 1px solid whitesmoke; */
    z-index: 2;
  }

  .dropdownMd:hover +  .childMd{
    display: block !important;
  }

  .childMd:hover{
    display: block !important;
    position: absolute;
  }
  .childMd a{
    font-weight: 400;
    padding-right: 20px;
    padding-left: 20px;
  }
  .childMd a:hover{
    background: rgba(128, 128, 128, 0.11);
  }

  .childMdFooter a{
    padding-right: 0px;
    padding-left: 0px;
  }
  .childMdFooter i{
    line-height: 2;
    padding: 1px 20px;
    position: relative;
    top: 0;
    left: 0;
    font-size:larger;
    color: rgba(0, 0, 0, 0.781) !important;
    z-index: 2;
  }

  .childMdFooter a:hover i{
    background: rgba(0, 0, 0, 0.781);
    color: white !important;
  }
 
  /* Ends Medium Dropdown */

</style>