<script>
// @ts-nocheck
    import { onMount } from 'svelte';

    // const cursor = {
    //     x: 0,
    //     y: 0
    // };

    // let background = undefined;

    // function handleMouseMove(e) {
    //     cursor.x = Math.round(e.clientX / 10) * 10;
    //     cursor.y = Math.round(e.clientY / 10) * 10;

    //     background.style.backgroundPosition = `-${cursor.x/20}px -${cursor.y/15}px`;
    //     // background.style.animation = 'none';
    // }

    // let smallDevice = false;

    // const attachListener = () => {
    //     const width = window.innerWidth;
    //     smallDevice = width < 768;
    // }

    // const resizeListener = () => {
    //     attachListener();
    // }

    onMount(() => {
      particlesJS.load('particles-js', '/particles.json', function() {
        console.log('callback - particles-js config loaded');
      });
    })
</script>

<!-- <svelte:window use:attachListener on:resize={resizeListener}/> -->

<!-- svelte-ignore a11y-no-static-element-interactions -->
 <div id="particles-js"></div>
<div class="background">
    <slot></slot>
</div>

<style>
    .background {
        width: 100%;
        min-height: 100vh;
        /* padding: 20vmin; */
        /* Add your background pattern here */
        transition: .2s linear;
        color: #784beb;
        display: flex;
        /* animation: blink 1s infinite ease; */
    }

    .background.small{
        animation: transform 50s infinite ease alternate;
    }

    @keyframes transform {
        from {
            background-position: -5px -5px;
        }

        to {
            background-position: 5000px 5000px;
        }
    }
</style>