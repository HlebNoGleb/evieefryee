<script>
    import Background from "$lib/components/background.svelte";
    import hotsFullLogo from "$lib/assets/images/hots_full-logo.png";
    import Submit from "$lib/components/submit.svelte";
    import Watch from "$lib/components/watch.svelte";
    import TournamentBrackets from "$lib/components/tournamentBrackets.svelte";
    import steps from "$lib/assets/data/steps.json";
    import prize from "$lib/assets/images/prize.jpg";

</script>
<Background>
    <div class="container justify-center">
        <div class="col justify-center">
            <img src={hotsFullLogo} alt="hots full logo" style="position: relative">
            <h1>TURNIR byfryee</h1>
            <div class="row justify-evenly align-center buttons" style="position: relative">
                <Submit/>
            </div>
            <div style="width: 80vmin; height: 50vmin; margin: auto; margin-bottom: 4vmin; position: relative">
                <iframe src="https://challonge.com/ru/byfryee/module" width="100%" height="100%" frameborder="0" scrolling="auto" allowtransparency="true"></iframe>
             </div>


            <!-- <img src={prize} alt="prize" style="margin-bottom: 4vmin; position: relative"> -->

            <!-- <TournamentBrackets steps={steps}/> -->


             <!-- <p>Всем удачи!!</p> -->
        </div>
    </div>
</Background>

<style>
    img{
        width: 70vmin;
        margin: auto;

    }
    h1{
        color: #fff;
        font-size: calc(0.75em + 5vmin);
        line-height: 1;
        text-align: center;
        margin-bottom: 5vmin;
    }

    p{
        color: #fff;
        font-size: calc(0.75em + 1vmin);
        /* line-height: 1; */
        text-align: center;
        width: 70vmin;
        margin: auto;
        margin-bottom: 5vmin;
    }

    .buttons{
        gap: 6vmin;
        margin-bottom: 5vmin;
    }

</style>