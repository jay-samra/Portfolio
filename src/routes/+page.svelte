<script lang=ts>
    import { onMount } from 'svelte';
    import * as THREE from 'three';
    import NET from 'vanta/dist/vanta.net.min';
    import FOG from 'vanta/dist/vanta.fog.min';
    import Menu from '../components/menu.svelte'

    function vanta(node: HTMLElement) {
        FOG({
            el: "#background",
            THREE: THREE,
            // mouseControls: true,
            // touchControls: true,
            // gyroControls: false,
            // minHeight: 200.00,
            // minWidth: 200.00
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            minHeight: 200.00,
            minWidth: 200.00,
            highlightColor: 0xffa600,
            midtoneColor: 0xff0000,
            lowlightColor: 0xff0063,
            baseColor: 0xffffff,
            blurFactor: 0.4,
            speed: 1.40,
            zoom: 0.90
        })
    }
</script>




<!-- <section id="background"/> -->

<!-- ABOVE IS ALL FOG FROM VANTA -->

<nav class=" h-15 w-7 pt-0">
        <!-- put hidden back in this  -->
         <div class="fixed top-0 left-0 w-full z-10 flex h-20 justify-center items-center content-center">
            <div class= "mt-2 border-4 bg-white navbar-center content-center items-center justify-center min-w-[500px] lg:flex w-10 h-15 rounded-[50px] border border-solid border-bg-neutral-900" >
              <ul class="menu menu-horizontal px-1">
                <li class="text-lg"><a href = 'https://www.linkedin.com/in/jagroop-s-sam18731/'>LinkedIn</a></li>
                <li><a class="text-lg" href = 'https://github.com/jay-samra'>GitHub</a></li>
                <li><a class="text-lg" href = 'https://www.linkedin.com/in/jagroop-s-sam18731/'>Resume</a></li>
            </ul>
            </div>
          </div>
        <!-- Right side of navbar-->

</nav>

<main>
    <section id="background" class="w-full h-screen" use:vanta>
      <div class ="flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl ">Hello, my name is Jagroop Singh!</h1>
        <h2 class="text-5xl"> I am a full stack developer and data analyst</h2>
        <button type="button" class="cursor-pointer text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2">Blue</button>
        <!-- <div class="absolute bottom-0 w-full h-16 bg-gradient-to-t from-[#f8f8f8] via-transparent"></div> -->
      </div>
      <svg class="absolute bottom-0 w-full z-20" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path fill="#333333" fill-opacity="1" d="M0,128L48,144C96,160,192,192,288,192C384,192,480,160,576,133.3C672,107,768,85,864,106.7C960,128,1056,192,1152,202.7C1248,213,1344,171,1392,149.3L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path>
    </svg>
    </section>

    <!-- add 'second-section' to section class for gradient -->
    <section class="bg-[#333333] min-h-screen ">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl text-[#FAF9F6]">Here are my projects!</h1>
        <h2 class="text-5xl text-[#FAF9F6]"> Here is my Resume! </h2>
        <button type="button" class="cursor-pointer text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2">Blue</button>
      </div>
    </section>

    <section class="bg-[#FAF9F6] min-h-screen">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl">Here are my projects!</h1>
        <h2 class="text-5xl"> Here is my Resume! </h2>
        <button type="button" class="cursor-pointer text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2">Blue</button>
        
        <!-- Project Cards -->
        <div class="flex space-x-5">
          <!-- Card 1 -->
        <div class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Domestic Violence Data Analysis Website</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A Global & National Case Study on Domestic Violence</p>
              <a href="https://github.com/jay-samra/Domestic-Violence-Data-Analysis-Website" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                  Read more
                  <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                      <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                  </svg>
              </a>
          </div>
            <!-- Card 1 -->
          <div class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Tutoring Company Website</h5>
            </a>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A fully functional, responsive website for a tutoring startup</p>
            <a href="https://github.com/wesbruh/TutorWebsite" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                Read more
                <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                </svg>
            </a>
        </div>
      </div>
      
    
    </div>
    </section>

    <section class="bg-[#333333] min-h-screen">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl text-[#FAF9F6]">Here are my projects!</h1>
        <h2 class="text-5xl text-[#FAF9F6]"> Here is my Resume! </h2>
        <button type="button" class="cursor-pointer text-white bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2">Blue</button>
      </div>
    </section>
</main>


<style>
    #background {
        width: 100%;
        height: 100vh;
        /* z-index was 0 originally */
        z-index: -1000;
    }

    .second-section {
    background: linear-gradient(to bottom, #000000, #FAF9F6);
    
    .clip-diagonal {
    clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 75%);
  }
}
</style>
