<script>
// @ts-nocheck

    const cursor = {
        x: 0,
        y: 0
    };

    let background = undefined;

    function handleMouseMove(e) {
        cursor.x = Math.round(e.clientX / 10) * 10;
        cursor.y = Math.round(e.clientY / 10) * 10;

        background.style.backgroundPosition = `-${cursor.x/20}px -${cursor.y/15}px`;
        // background.style.animation = 'none';
    }

    let smallDevice = false;

    const attachListener = () => {
        const width = window.innerWidth;
        smallDevice = width < 768;
    }

    const resizeListener = () => {
        attachListener();
    }
</script>

<svelte:window use:attachListener on:resize={resizeListener}/>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<div class="background" on:mousemove={(e) => handleMouseMove(e)} bind:this={background} class:small={smallDevice}>
    <slot></slot>
</div>

<style>
    .background {
        width: 100%;
        min-height: 100vh;
        /* padding: 20vmin; */
        /* Add your background pattern here */
        background-color: #313131;
        background-image: radial-gradient(rgba(114, 81, 198, .5) 2px, transparent 0);
        background-size: 30px 30px;
        background-position: -5px -5px;
        transition: .2s linear;
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