<script lang=ts>
    import { onMount } from 'svelte';
    import * as THREE from 'three';
    import NET from 'vanta/dist/vanta.net.min';
    import FOG from 'vanta/dist/vanta.fog.min';
    import GLOBE from 'vanta/dist/vanta.globe.min';
    import Menu from '../components/menu.svelte';
    import Projects from '../components/projects.svelte';

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
            // highlightColor: 0xffa600,
            highlightColor:0x51615,
            midtoneColor: 0xff0000,
            lowlightColor: 0xff0063,
            baseColor: 0xffffff,
            blurFactor: 0.4,
            speed: 1.40,
            zoom: 0.90
        })
      }
        function vantaNET(node: HTMLElement) {
          GLOBE({
          el: "#backgroundNET",
          THREE: THREE,
          mouseControls: true,
          touchControls: true,
          gyroControls: false,
          minHeight: 200.00,
          minWidth: 200.00,
          scale: 1.00,
          scaleMobile: 1.00,
          color: 0xff3f8e,
          color2: 0x0,
          backgroundColor: 0xFAF9F6
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
                <li><a class="text-lg" href = '/resume.pdf' target='_blank'>Resume</a></li>
            </ul>
            </div>
          </div>
        <!-- Right side of navbar-->

</nav>

<main>
    <section id="backgroundNET" class="w-full h-screen" use:vantaNET>
      <div class ="flex flex-col items-left pl-20 justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl ">Hello, my name is Jagroop Singh</h1>
        <h2 class="text-5xl"> Aspiring full stack developer and data analyst</h2>
        <!-- Buttons -->
        <div>
          <button class="relative h-12 overflow-hidden rounded-md bg-neutral-950 px-5 py-2.5 text-white transition-all duration-300 hover:bg-neutral-800 hover:ring-2 hover:ring-neutral-800 hover:ring-offset-2">
              <span class="relative">Contact Me</span>
          </button>
          <a href="/resume.pdf" target="_blank" >
          <button class="group relative inline-flex h-12 items-center justify-center overflow-hidden rounded-md bg-gray-200 px-6 font-medium text-black ml-4">
              <span>View CV</span>
              <div class="w-0 translate-x-[100%] pl-0 opacity-0 transition-all duration-200 group-hover:w-5 group-hover:translate-x-0 group-hover:pl-1 group-hover:opacity-100">
                  <svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5">
                      <path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path>
                  </svg>
              </div>
          </button>
        </a>
      </div>
  
    </section>

    
    <!-- add 'second-section' to section class for gradient -->
     <!-- OR #FAFAFA -->
    <section class="bg-[#FAFAFA] min-h-screen ">
      <div class="py-8">
      <hr class="w-48 h-1 mx-auto my-4 bg-gray-700 border-0 rounded md:my-10 dark:bg-gray-700">
      </div>
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl text-[#333333] ">I'm Jagroop Singh <span class="special-font">| ਜਗ ਸੀਂਗ </span> </h1>
  
        <div class ="flex flex-col items-left pl-20 justify-center align-middle h-full content-between gap-10">
          <h2 class="text-4xl text-[#333333]">  COMPUTER SCIENCE STUDENT @CSUS WHO IS PASSIONATE TO USE TECHNOLOGY IN ORDER TO ADDRESS SOME OF THE MOST PRESSING ISSUES TODAY AND EMBRACES LEADERSHIP POSITIONS TO HELP TEAMS SUCCEED IN THEIR MISSION</h2>
        </div>        
      </div>
    </section>

    <section class="bg-[#FAF9F6] min-h-screen">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <hr class="w-48 h-1 mx-auto my-4 bg-[#333333] border-0 rounded md:my-10 dark:bg-gray-700">
        <h1 class="text-7xl">Here are some of my Projects!</h1>
        
        <!-- Project Cards -->
        <div class="flex flex-nowrap space-x-5">
          <!-- Card 1 -->
          <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <img class="rounded-t-lg" src="/favicon.png" alt="" />
            </a>
            <div class="p-5">
                <a href="#">
                    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Domestic Violence Data Analysis Website</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A Global & National Case Study on Domestic Violence</p>
                <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                    Read more
                     <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                        <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                    </svg>
                </a>
            </div>
        </div>
            <!-- Card 2 -->
            <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
              <a href="#">
                  <img class="rounded-t-lg" src="/favicon.png" alt="" />
              </a>
              <div class="p-5">
                  <a href="#">
                      <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Tutoring Company Website</h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A fully functional, responsive website for a tutoring startup</p>
                  <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                      Read more
                       <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                          <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                      </svg>
                  </a>
              </div>
          </div>
        <!-- Card 3 -->
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
          <a href="#">
              <img class="rounded-t-lg" src="/favicon.png" alt="" />
          </a>
          <div class="p-5">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Portfolio Website</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A personal portfolio website displaying my experience, projects, and skills</p>
              <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                  Read more
                   <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                      <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                  </svg>
              </a>
          </div>
      </div>
        <!-- Card 4 -->
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700">
          <a href="#">
              <img class="rounded-t-lg" src="/favicon.png" alt="" />
          </a>
          <div class="p-5">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Unhoused Assistance Website</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A personal portfolio website displaying my experience, projects, and skills</p>
              <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                  Read more
                   <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                      <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                  </svg>
              </a>
          </div>
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
