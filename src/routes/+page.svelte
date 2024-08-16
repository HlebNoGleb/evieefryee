<script>
// @ts-nocheck
    import yanka from '$lib/assets/images/yanka.jpg';
    import twitchLogo from '$lib/assets/images/twitch_logo.png';
    import discordLogo from '$lib/assets/images/discord.png';
    import instagramLogo from '$lib/assets/images/instagram.webp';
    import telegramLogo from '$lib/assets/images/telegram.png';
    import donationAlertsLogo from '$lib/assets/images/donationAlerts.png';
    import hots from '$lib/assets/images/hots_full-logo.png';
    import Background from '$lib/components/background.svelte';
    import { register } from 'swiper/element/bundle';
    register();
</script>

<Background>
    <div class="container justify-between" >
        <div class="image">
            <div class="image-container drop-shadow" style="background-image: url('{yanka}');">
                <span>hots | vibe | aesthetic | sexy</span>
                <div class="name-container">
                    <h1 class="neon-text">evieefryee</h1>
                </div>
            </div>
        </div>
        <div class="tv ">
            <div style="position: relative; border: 1vmin solid rgba(255,255,255, .7);  aspect-ratio: 16/9;" class="drop-shadow">
                <swiper-container slides-per-view="1" autoplay="true" speed="500" loop="true" style="height: 100%;">
                    <swiper-slide>
                        <a href="https://twitch.tv/evieefryee" class="tv-container" style="background-image: url('{twitchLogo}');">
                        </a>
                    </swiper-slide>
                    <swiper-slide>
                        <a href="/hots-tournament" class="tv-container" style="background-image: url('{hots}');">
                            <!-- <span>TURNIR byfryee</span> -->
                        </a>
                </swiper-slide>
                </swiper-container>
            </div>
            <div class="social-row">
                <a href="https://discord.gg/jxxVmCr5w7" class="drop-shadow social-container discord" style="background-image: url('{discordLogo}?raw');">
                </a>
                <a href="https://www.instagram.com/evieefryee/" class="drop-shadow social-container instagram" style="background-image: url('{instagramLogo}');">
                </a>
                <a href="https://t.me/byfryee" class="drop-shadow social-container telegram" style="background-image: url('{telegramLogo}');">
                </a>
                <a href="https://www.donationalerts.com/r/evieefryee" class="drop-shadow social-container donationAlerts" style="background-image: url('{donationAlertsLogo}');">
                </a>
                <!-- <a href="" class="drop-shadow social-container donationAlerts" style="background-image: url('{donationAlertsLogo}');">
                </a> -->
            </div>
        </div>
    </div>
</Background>

<style>
    .image{
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-size: 1em;
    }

    .image .name-container{
        display: flex;
        height: 100%;
        align-items: center;
        justify-content: center;
        overflow: hidden;
    }

    .image h1{
        color: #fff;
        font-size: calc(0.75em + 6vmin);
        line-height: 1;
        z-index: 1;
        mix-blend-mode: overlay;
        margin-bottom: 1vmin;
        margin-left: 1vmin;

        /* color: #fff;
    font-size: calc(0.75em + 15vmin);
    line-height: 1;
    z-index: 1;
    mix-blend-mode: overlay;
    margin-bottom: 1vmin;
    margin-left: 1vmin;
    line-break: anywhere;
    text-align: right; */
    }

    .image span{
        position: absolute;
        color: #ccc;
        margin-top: -5vmin;
        top: 0;
        font-size: calc(0.5em + 1vmin);
    }

    .image .image-container{
        width: 35vmax;
        height: 35vmax;
        border: 1vmin solid rgba(255,255,255, .7);
        border-radius: 5px;
        background-size: cover;
        background-position: center;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        /* transition: .6s all ease; */
    }

    .image .image-container:hover{
        /* background-size: 200%; */
    }

    .drop-shadow {
        filter: drop-shadow(0 0 5px rgba(142, 85, 171, 0.8));
    }

    .tv{
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 50vmax;
    }

    .tv > div {
        border-radius: 5px;
        overflow: hidden;
    }

    .tv .tv-container{
        background-size: cover;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        background-size: 60%;
        background-repeat: no-repeat;
        background-position: center;
        background-color: #9146ff;
        position: relative;
        width: 100%;
        height: 100%;
    }

    .tv .tv-container span{
        position: absolute;
        bottom: 1vmin;
        left: 1vmin;
        color: #fff;
        font-size: calc(0.5em + 1vmin);
    }

    .tv .hots{
        position:absolute;
        bottom: 1vmin;
        right: 1vmin;
        width: 10vmax;
        height: 10vmax;
        background-size: 100%;
        background-repeat: no-repeat;
        background-position: center;
        filter: drop-shadow(0 0 10px #5ab6ef) drop-shadow(0 0 20px #30a7f2);
        animation: rotate 10s infinite linear;
    }

    @keyframes rotate{
        from{
            transform: rotate(0deg);
        }

        to{
            transform: rotate(360deg);
        }
    }

    .tv .social-row{
        display: flex;
        justify-content: space-between;
    }

    .tv .social-container{
        border: 1vmin solid rgba(255,255,255, .7);
        border-radius: 5px;
        background-size: cover;
        width: 9vmax;
        aspect-ratio: 16/9;
    }

    .tv .social-container.discord{
        background-size: 70%;
        background-repeat: no-repeat;
        background-position: center;
        background-color: #5865F2;
    }

    .tv .social-container.telegram{
        background-size: 70%;
        background-repeat: no-repeat;
        background-position: center;
        background-color: #28a7e7;
    }

    .tv .social-container.donationAlerts{
        background-size: 70%;
        background-repeat: no-repeat;
        background-position: center;
        background-color: #191919;
    }

    @media (max-width: 1100px) {
        .container{
            flex-direction: column;
            align-items: center;
        }

        .image{
            margin-bottom: 4vmin;
            max-width: 100%;
            display: flex;
            align-items: center;
            /* display: none; */
        }

        .image .image-container{
            width: 90vmin;
        }

        .image span{
            margin-top: -7vmin;
        }

        .tv{
            /* width: 100%; */
            /* display: flex;
            align-items: center; */
        }

        .tv > div{
            margin-bottom: 4vmin;
            width: 90vmin;
        }

        .tv .social-container{
            width: 15vmin;
        }

        .tv .tv-container .hots{
            width: 15vmin;
            height: 15vmin;
        }
    }

    @media (max-width: 500px) {
        .tv .social-row{
            flex-wrap: wrap;
            gap: 4vmin;
        }
        .tv .social-container{
            /* width: 100%; */
            width: 30vmin;
            /* margin: 2vmin; */
            flex-grow: 1;
        }
    }
</style>
