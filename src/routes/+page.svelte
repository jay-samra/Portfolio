<script lang=ts>
    import { onMount } from 'svelte';
    import * as THREE from 'three';
    import NET from 'vanta/dist/vanta.net.min';
    import FOG from 'vanta/dist/vanta.fog.min';

    function vanta(node: HTMLElement) {
        FOG({
            el: "#background",
            // THREE: THREE,
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
            highlightColor: 0xe8d7b7,
            midtoneColor: 0xe83333,
            lowlightColor: 0xdca9bd,
            baseColor: 0x7979dc,
            blurFactor: 0.52,
            speed: 1.40,
            zoom: 3.00
        })
    }
</script>

<style>
    #background {
        width: 100%;
        height: 100vh;
        z-index: 0;
    }
</style>

<!-- <section id="background"/> -->

<!-- ABOVE IS ALL FOG FROM VANTA -->

<section id="background" class="h-15 w-7">
        <!-- put hidden back in this  -->
        <div class="navbar-center justify-center min-w-[500px] lg:flex w-74 h-15 rounded-[50px] border border-solid border-bg-neutral-900" >
          <ul class="menu menu-horizontal px-1">
            <li class="text-lg"><a href = 'https://www.linkedin.com/in/jagroop-s-sam18731/'>LinkedIn</a></li>
            <li><a class="text-lg" href = 'https://github.com/jay-samra'>GitHub</a></li>
            <li><a class="text-lg" href = 'https://www.linkedin.com/in/jagroop-s-sam18731/'>Resume</a></li>
          </ul>
        </div>
        <!-- Right side of navbar-->

</section>

<section>
    <div class="min-h-[1000px]" use:vanta/>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
    <h1> New Section </h1>
</section>