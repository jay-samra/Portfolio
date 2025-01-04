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
            blurFactor: 0.52,
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
        <h1 class="text-7xl">Hello, my name is Jagroop Singh!</h1>
        <h2 class="text-5xl"> I am a full stack developer and data analyst</h2>
      </div>
    </section>
    
    <section class="bg-green-500">
      <div class ="bg-green flex flex-col items-center justify-center align-middle h-full content-between gap-10">
        <h1 class="text-7xl">Here are my projects!</h1>
        <h2 class="text-5xl"> Here is my Resume! </h2>
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
</style>