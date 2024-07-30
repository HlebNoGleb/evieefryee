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
            <img src={hotsFullLogo} alt="hots full logo">
            <h1>Турнир от evieefryee</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum temporibus sequi nihil sit libero. Facere facilis, enim sapiente dolorem voluptatum fugiat ducimus dolorum deleniti nobis laborum, incidunt accusantium quidem distinctio!</p>
            <div class="row justify-evenly align-center buttons">
                <Watch/>
                <Submit/>
            </div>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum temporibus sequi nihil sit libero. Facere facilis, enim sapiente dolorem voluptatum fugiat ducimus dolorum deleniti nobis laborum, incidunt accusantium quidem distinctio!</p>

            <img src={prize} alt="prize" style="margin-bottom: 4vmin;">

            <!-- <TournamentBrackets steps={steps}/> -->
             <div style="width: 70vmin; height: 50vmin; margin: auto; margin-bottom: 4vmin">
                <iframe src="https://challonge.com/ru/6cmu8qbq/module" width="100%" height="100%" frameborder="0" scrolling="auto"></iframe>
             </div>

             <p>Всем удачи!!</p>
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