<script lang=ts>
    import { onMount } from 'svelte';
    import * as THREE from 'three';
    import NET from 'vanta/dist/vanta.net.min';
    import FOG from 'vanta/dist/vanta.fog.min';
    import GLOBE from 'vanta/dist/vanta.globe.min';
    import Menu from '../components/menu.svelte';
    import Wave from '../components/wave.svelte';
    import Carousel from '../components/carousel.svelte';

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
          // ff3f8e
          color: 0xffb766,
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
                <li class="text-lg"><a href = '/contact' target = '_blank'>Contact Me</a></li>
                <li><a class="text-lg" href = 'http://www.linkedin.com/in/jagroop-s-sam18731' target="_blank">LinkedIn</a></li>
                <li><a class="text-lg" href = '/newResume.pdf' target='_blank'>Resume</a></li>
            </ul>
            </div>
          </div>
        <!-- Right side of navbar-->

</nav>

<main>
    <section id="backgroundNET" class="w-full h-screen" use:vantaNET>
      <div class ="flex flex-col items-left pl-20 justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl ">Hello, my name is Jagroop Singh</h1>
        <h2 class="text-5xl "> Aspiring full stack developer & data analyst</h2>
        <!-- Buttons -->
        <div>
          <a href="/contact" target="_blank">
          <button class="relative h-12 overflow-hidden rounded-md bg-neutral-950 px-5 py-2.5 text-white transition-all duration-300 hover:bg-neutral-800 hover:ring-2 hover:ring-neutral-800 hover:ring-offset-2">
              <span class="relative">Contact Me</span>
          </button>
        </a>
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
        <!-- Arrow -->
         <button>
          <a href="#section1">
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2">
          <div class="animate-bounce">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"  class="w-10 h-10 text-black" >
              <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
            </svg>
          </div>
        </div>
      </a>
      </button>
      </div>




  
    </section>

    <!-- About Me -->
    <!-- add 'second-section' to section class for gradient -->
     <!-- OR #FAFAFA -->
    <section id = "section1" class="bg-[#FAF9F6] min-h-screen ">
      <div class="py-8">
      <hr class="w-48 h-1 mx-auto my-4 bg-gray-700 border-0 rounded md:my-10 dark:bg-gray-700">
      </div>
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl text-[#333333] ">I'm Jagroop Singh  <span class="special-font"> | ਜਗਰੂਪ ਸਿੰਘ </span> </h1>
  
        <div class ="flex flex-col items-left pl-20 justify-center align-middle h-full content-between gap-10">
          <h2 class="text-3xl text-[#333333] indent-10">  COMPUTER SCIENCE STUDENT @CSUS WHO IS PASSIONATE TO USE TECHNOLOGY IN ORDER TO ADDRESS SOME OF THE MOST PRESSING ISSUES TODAY AND EMBRACES LEADERSHIP POSITIONS TO HELP TEAMS SUCCEED IN THEIR MISSION.</h2>
          <h2 class="text-3xl text-[#333333] indent-10">  THROUGH MY ACADEMIC JOURNEY AND HANDS-ON EXPERIENCE, I HAVE DEVELOPED STRONG FOUNDATIONS IN INDUSTRY-POPULAR LANGUAGES & TECHNOLOGIES SUCH AS PYTHON, JAVASCRIPT, JAVA, AND MACHINE LEARNING.</h2>
          <h2 class="text-3xl text-[#333333] indent-10">  I HAVE ALSO DEVELOPED VARIOUS DATA ANALYSIS SKILLS SUCH AS REGRESSION ANALYSIS, CLUSTERING, AND DATA PREPROCESSING. I AM EAGER TO APPLY THESE SKILLS IN REAL-WORLD CONTEXTS WHERE I CAN LEARN FROM MENTORS, AND ADVANCE ORGANIZATIONAL PROJECTS. </h2>


        </div>  
        <div class="pt-10">
        <h1 class="text-6xl"> My Skills</h1>
      </div>
      
      
      <div class="pb-10 flex flex-wrap justify-evenly gap-6 mx-8" >
            <!-- Card #1 -->      
                <div class="relative group duration-500 cursor-pointer group overflow-hidden relative text-gray-50 h-72 w-96  rounded-2xl hover:duration-700 duration-700  border-black">
                  <div class="w-96 h-72 bg-[#c2edda] text-gray-800">
                    <div class="flex flex-row justify-between">
                  <path class="" d="M15.8,32.9V15.8m0,0H32.9m-17.1,0L37.2,37.2m47-4.3V15.8m0,0H67.1m17.1,0L62.8,37.2m-47,29.9V84.2m0,0H32.9m-17.1,0L37.2,62.8m47,21.4L62.8,62.8M84.2,84.2V67.1m0,17.1H67.1" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                  <path class="svg-stroke-primary" d="M50,17.4h0M50,50h0m0,32.6h0M50,22a4.7,4.7,0,1,1,4.7-4.6A4.7,4.7,0,0,1,50,22Zm0,32.7A4.7,4.7,0,1,1,54.7,50,4.7,4.7,0,0,1,50,54.7Zm0,32.6a4.7,4.7,0,1,1,4.7-4.7A4.7,4.7,0,0,1,50,87.3Z" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                    </div>
                  </div>
                  <div class="absolute bg-gray-50 -bottom-24 w-96 p-5 flex flex-col gap-1 group-hover:-bottom-0 group-hover:duration-600 duration-500">
                    <span class="text-lime-400 font-bold text-s">#1</span>
                    <span class="text-gray-800 font-bold text-3xl"> UI Design</span>
                    <p class="text-neutral-800">I have built various user-friendly UIs with conscious effort of making the customer experience as smooth as possible</p>
                  </div>

                </div>


                           <!-- Card #2 -->      
                <div class="relative group duration-500 cursor-pointer group overflow-hidden relative text-gray-50 h-72 w-96  rounded-2xl hover:duration-700 duration-700">
                  <div class="w-96 h-72 bg-lime-400 text-gray-800">
                    <div class="flex flex-row justify-between">
                  <path class="" d="M15.8,32.9V15.8m0,0H32.9m-17.1,0L37.2,37.2m47-4.3V15.8m0,0H67.1m17.1,0L62.8,37.2m-47,29.9V84.2m0,0H32.9m-17.1,0L37.2,62.8m47,21.4L62.8,62.8M84.2,84.2V67.1m0,17.1H67.1" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                  <path class="svg-stroke-primary" d="M50,17.4h0M50,50h0m0,32.6h0M50,22a4.7,4.7,0,1,1,4.7-4.6A4.7,4.7,0,0,1,50,22Zm0,32.7A4.7,4.7,0,1,1,54.7,50,4.7,4.7,0,0,1,50,54.7Zm0,32.6a4.7,4.7,0,1,1,4.7-4.7A4.7,4.7,0,0,1,50,87.3Z" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                    </div>
                  </div>
                  <div class="absolute bg-gray-50 -bottom-24 w-96 p-5 flex flex-col gap-1 group-hover:-bottom-0 group-hover:duration-600 duration-500">
                    <span class="text-lime-400 font-bold text-s">#2</span>
                    <span class="text-gray-800 font-bold text-3xl">Backend Execution</span>
                    <p class="text-neutral-800">I have experience implementing a wide range of backend services tailored to meet the specific needs of a variety of clients</p>
                  </div>

                </div>

                   <!-- Card #3 -->      
                <div class="relative group duration-500 cursor-pointer group overflow-hidden relative text-gray-50 h-72 w-96  rounded-2xl hover:duration-700 duration-700">
                  <div class="w-96 h-72 bg-[#C0D6E8] text-gray-800">
                    <div class="flex flex-row justify-between">
                  <path class="" d="M15.8,32.9V15.8m0,0H32.9m-17.1,0L37.2,37.2m47-4.3V15.8m0,0H67.1m17.1,0L62.8,37.2m-47,29.9V84.2m0,0H32.9m-17.1,0L37.2,62.8m47,21.4L62.8,62.8M84.2,84.2V67.1m0,17.1H67.1" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                  <path class="svg-stroke-primary" d="M50,17.4h0M50,50h0m0,32.6h0M50,22a4.7,4.7,0,1,1,4.7-4.6A4.7,4.7,0,0,1,50,22Zm0,32.7A4.7,4.7,0,1,1,54.7,50,4.7,4.7,0,0,1,50,54.7Zm0,32.6a4.7,4.7,0,1,1,4.7-4.7A4.7,4.7,0,0,1,50,87.3Z" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="8">
                  </path>

                    </div>
                  </div>
                  <div class="absolute bg-gray-50 -bottom-24 w-96 p-5 flex flex-col gap-1 group-hover:-bottom-0 group-hover:duration-600 duration-500">
                    <span class="text-lime-400 font-bold text-s">#3</span>
                    <span class="text-gray-800 font-bold text-3xl">Data Analysis</span>
                    <p class="text-neutral-800">I enjoy working on meaningful Data Analysis projects through the utilization of new technologies to support my community</p>
                  </div>

                </div>
        </div>
      
      
          </div>
      
    </section>

    <section class="bg-[#FAF9F6] min-h-screen">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <hr class="w-48 h-1 mx-auto my-4 bg-[#333333] border-0 rounded md:my-10 dark:bg-gray-700">
        <h1 class="text-7xl">Here Are Some Projects That I am Proud Of!</h1>
        
        <!-- Project Cards -->
        <div class="flex flex-wrap justify-center space-x-7 space-y-8">
          <!-- Card 1 -->
          <div class="w-full md:w-1/3 max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
            <a href="#">
                <img class="w-full h-56 object-cover rounded-t-lg " src="/newplot.png" alt="" />
            </a>
            <div class="p-5">
                <a href="#">
                    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Domestic Violence Data Analysis Website</h5>
                </a>
                <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A Global & National Case Study on Domestic Violence</p>
                <div class="space-y-10">
                  <a href="https://github.com/jay-samra/Domestic-Violence-Data-Analysis-Website" target = "_blank">
                <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
              </a>
              </div>
            </div>
        </div>
            <!-- Card 2 --> 
            <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
              <a href="#">
                  <img class="w-full h-56 object-cover rounded-t-lg" src="/tutor2.png" alt="" />
              </a>
              <div class="p-5">
                  <a href="#">
                      <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Tutoring Company Website</h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A fully functional and robust website for a tutoring startup built by utilzing the MERN stack</p>
                  <div class="space-y-10">
                    <a href="https://github.com/wesbruh/TutorWebsite" target = "_blank">
                      <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
                    </a>                
                  </div>
              </div>
          </div>
              <!-- Card 3 -->
    <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
      <a href="#">
          <img class="w-full h-56 object-cover rounded-t-lg" src="/energy.png" alt="" />
      </a>
      <div class="p-5">
          <a href="#">
              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">NYC Energy Analysis Dashboard</h5>
          </a>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Analyzing New York City's energy usage through data visualizations and interactive graphs</p>
          <a href="https://github.com/jay-samra/NYC-Energy-Analysis" target = "_blank">
            <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
          </a>   
      </div>
  </div>
        <!-- Card 4 -->
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
          <a href="#">
              <img class="w-full h-56 object-cover rounded-t-lg" src="/svelteKit.png" alt="" />
          </a>
          <div class="p-5">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Portfolio Website</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">A personal portfolio website displaying my experience, projects, and skills</p>
              <a href="https://github.com/jay-samra/Portfolio" target = "_blank">
                <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
              </a>   
              
          </div>
      </div>
              <!-- Card 5 -->
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
          <a href="#">
              <img class="w-full h-56 object-cover rounded-t-lg" src="/java.png" alt="" />
          </a>
          <div class="p-5">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Ant Escape</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400"> Mobile game developed using Java with a heavy emphasis on OOP principles and scalability </p>
              <a href="https://github.com/jay-samra/Ant-Escape" target = "_blank">
                <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
              </a>   
          </div>
      </div>
        <!-- Card 5 -->
        <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
          <a href="#">
              <img class="w-full h-56 object-cover rounded-t-lg" src="/journal.png" alt="" />
          </a>
          <div class="p-5">
              <a href="#">
                  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Mental Health Tracking Journal</h5>
              </a>
              <p class="mb-3 font-normal text-gray-700 dark:text-gray-400"> Journaling website which allows users to track their mental health status, set goals, and improve their well-being</p>
              <a href="https://github.com/jay-samra/HealthTracker" target = "_blank">
                <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
              </a>   
          </div>
      </div>
      <!-- Card 6 -->
      <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
        <a href="#">
            <img class="w-full h-56 object-cover rounded-t-lg" src="/java.png" alt="" />
        </a>
        <div class="p-5">
            <a href="#">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Movie Recommender</h5>
            </a>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Recommends movies based on characteristics and filters chosen by customer</p>
            
            <a href="https://github.com/jay-samra/MovieRecommender" target = "_blank">
              <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
            </a>           
          </div>
    </div>
    <!-- Card 7 -->
    <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
      <a href="#">
          <img class="w-full h-56 object-cover rounded-t-lg" src="/clogo.jpg" alt="" />
      </a>
      <div class="p-5">
          <a href="#">
              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Vending and Loan Operations Automation System</h5>
          </a>
          <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Processes vending and loan options in an automated fashion, developed in C</p>
          <a href="https://github.com/jay-samra/Vending-And-Loan-Operations-Automation" target = "_blank">
            <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
          </a>   
      </div>
  </div>

              <!-- Card 8 -->
              <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
                <a href="#">
                    <img class="w-full h-56 object-cover rounded-t-lg" src="/neetcode.png" alt="" />
                </a>
                <div class="p-5">
                    <a href="#">
                        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Neetcode: Blind 75</h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Solving Neetcode's Blind 75 practice interview questions in an efficient manner to help students prepare for technical interviews</p>
                    <a href="https://github.com/jay-samra/blind75" target = "_blank">
                      <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
                    </a>   
                </div>
            </div>

                          <!-- Card 9 -->
              <div class="max-w-sm bg-white border border-gray-200 rounded-lg shadow-xl dark:bg-gray-800 dark:border-gray-700">
                <a href="#">
                    <img class="w-full h-56 object-cover rounded-t-lg" src="/tcp.jpg" alt="" />
                </a>
                <div class="p-5">
                    <a href="#">
                        <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">TCP Live Chat Room</h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">TCP Live Chat Room which can support multiple users with live messaging, broadcasting, and various other communication features</p>
                    <a href="https://github.com/jay-samra/Final-Project" target = "_blank">
                      <button class="group relative inline-flex h-[calc(48px+8px)] items-center justify-center rounded-full bg-neutral-950 py-1 pl-6 pr-14 font-medium text-neutral-50"><span class="z-10 pr-2">View Project</span><div class="absolute right-1 inline-flex h-12 w-12 items-center justify-end rounded-full bg-neutral-700 transition-[width] group-hover:w-[calc(100%-8px)]"><div class="mr-3.5 flex items-center justify-center"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-neutral-50"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></div></button>
                    </a>   
                </div>
            </div>

      </div>
      <div class = "pt-8">
    <a href="https://github.com/jay-samra" target="_blank">
    <button class="group relative inline-flex h-24 items-center justify-center overflow-hidden rounded-md bg-neutral-950  px-6 font-medium text-neutral-200"><span>View My Entire Github Repository</span><div class="ml-1 transition group-hover:translate-x-1"><svg width="15" height="15" viewBox="0 0 15 15" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5"><path d="M8.14645 3.14645C8.34171 2.95118 8.65829 2.95118 8.85355 3.14645L12.8536 7.14645C13.0488 7.34171 13.0488 7.65829 12.8536 7.85355L8.85355 11.8536C8.65829 12.0488 8.34171 12.0488 8.14645 11.8536C7.95118 11.6583 7.95118 11.3417 8.14645 11.1464L11.2929 8H2.5C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7H11.2929L8.14645 3.85355C7.95118 3.65829 7.95118 3.34171 8.14645 3.14645Z" fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path></svg></div></button>
    </a>
    </div>
    </div>
    </section>

    <!-- Essays/Blogs -->
    <section class="bg-[#FAF9F6] min-h-screen ">
      <div class="py-8">
      <hr class="w-48 h-1 mx-auto my-4 bg-gray-700 border-0 rounded md:my-10 dark:bg-gray-700">
      </div>
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl text-[#333333] "> My Blogs & Essays</h1>

        <div class = "flex space-x-4 flex-wrap justify-center space-x-8 space-y-8">
          <div class="card card-side bg-base-100 shadow-xl ">
            <figure>
              <img
                src="fastifylogo.png"
                alt="Movie" />
            </figure>
            <div class="card-body max-w-[500px]">
              <h2 class="card-title">Fastify Framework Investigation</h2>
              <p>A deep dive into Fastify's codebase in order to determine the most efficient way to implement custom attribute keys, similar to Pino-HTTP.</p>
              <div class="card-actions justify-end">
                <a href="OpenSourceBlog.pdf" target="_blank">
                <button class="btn btn-black">Read</button>
              </a>
              </div>
            </div>
          </div>
      <!-- 2 Card -->
      <div class="card card-side bg-base-100 shadow-xl ">
        <figure>
          <img
            src="mlphoto.png"
            alt="Movie" />
        </figure>
        <div class="card-body max-w-[500px]">
          <h2 class="card-title">Machine Learning: An Automated Future</h2>
          <p>Writing sample on the importance of Machine Learning, its implications, and areas in which it can still grow as technology advances.</p>
          <div class="card-actions justify-end">
            <a href="writingsample.pdf" target="_blank">
            <button class="btn btn-black">Read</button>
          </a>
          </div>
        </div>
      </div>
            <!-- 3 Card -->
            <!-- <div class="card card-side bg-base-100 shadow-xl ">
              <figure>
                <img
                  src="mlphoto.png"
                  alt="Movie" />
              </figure>
              <div class="card-body max-w-[500px]">
                <h2 class="card-title">Integrating Vanta.js into a SvelteKit Project</h2>
                <p>Documentation on how to incorporate one of Vanta.js's animated backgrounds into a SvelteKit project</p>
                <div class="card-actions justify-end">
                  <a href="writingsample.pdf" target="_blank">
                  <button class="btn btn-black">Read</button>
                </a>
                </div>
              </div>
            </div> -->
  </div>


      </div>
      
    </section>

    <!-- Wave Divider -->
    <div class="bg-[#FAF9F6] pt-48">
      <svg class="h-24 w-full" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" preserveAspectRatio="none">
      <path class="text-[#333333] fill-current" fill-opacity="0.99"
              d="M0,288L60,245.3C120,203,240,117,360,112C480,107,600,181,720,229.3C840,277,960,299,1080,256C1200,213,1320,107,1380,53.3L1440,0L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path>
      </svg>
  </div>


    <!-- End -->
    <section class="bg-[#333333] ">
      <div class ="bg-green flex items-center justify-center align-middle h-full content-between gap-10 pb-4">
        <a href="http://www.linkedin.com/in/jagroop-s-sam18731" target="_blank">
        <span class="[&>svg]:h-7 [&>svg]:w-7 [&>svg]:fill-[#0077b5]">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc. -->
            <path
              d="M100.3 448H7.4V148.9h92.9zM53.8 108.1C24.1 108.1 0 83.5 0 53.8a53.8 53.8 0 0 1 107.6 0c0 29.7-24.1 54.3-53.8 54.3zM447.9 448h-92.7V302.4c0-34.7-.7-79.2-48.3-79.2-48.3 0-55.7 37.7-55.7 76.7V448h-92.8V148.9h89.1v40.8h1.3c12.4-23.5 42.7-48.3 87.9-48.3 94 0 111.3 61.9 111.3 142.3V448z" />
          </svg>
        </span>
      </a>

        <a href="https://github.com/jay-samra" target="_blank">
        <span class="[&>svg]:h-7 [&>svg]:w-7 [&>svg]:fill-[#f7f1f1] ">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512">
            <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc. -->
            <path
              d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3 .3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5 .3-6.2 2.3zm44.2-1.7c-2.9 .7-4.9 2.6-4.6 4.9 .3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3 .7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3 .3 2.9 2.3 3.9 1.6 1 3.6 .7 4.3-.7 .7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3 .7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3 .7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z" />
          </svg>
        </span>
      </a>
        
      </div>
      <div class="pb-4 space-y-8">
        <h3 class="text-white text-center ">&#127880 Made by Jagroop Singh &#127880</h3>
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

.wave-divider {
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    overflow: hidden;
    line-height: 0;
  }

  .wave-divider svg {
    position: relative;
    display: block;
    width: calc(100% + 1.3px);
    height: 60px;
  }

  @media (min-width: 768px) {
    .wave-divider svg {
      height: 150px;
    }
  }
</style>
