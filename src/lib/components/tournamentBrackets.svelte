<script>
    import { onMount } from "svelte";

    export let steps;

    let stepsCount = 0;
    onMount(() => {
        stepsCount = steps.length;
    });


</script>
<div class="row align-center steps justify-between">
    {#each steps as step, i}
        <div class="col step">
            {#each step as teams}
                <div class="col teams">
                    {#each teams as team}
                        <div class="col team">
                            <p>{team.team}</p>
                        </div>
                    {/each}
                </div>
            {/each}
        </div>
        {#if i < stepsCount - 1}
            <div class="col divider" data-step-num={i + 1} style="height: 100%; justify-content: space-around; gap: calc(4vmin * {i+1}); width: 4vmin">
                {#each step as teams, j}
                    <div style="height: calc(100% / {steps.length - i}); display: flex; flex-direction: column; justify-content: center; align-items: center; position: relative">
                        <div class="top"></div>
                        <div class="bottom"></div>
                        <div class="winner"></div>
                        <div class="line"></div>
                    </div>
                {/each}
            </div>
        {/if}
    {/each}
</div>

<style>
    .steps{
        width: 100%;
        border: 3px solid red;
    }

    .step{
        height: 100%;
        justify-content: space-around;
        gap: 4vmin;
        border: 3px solid green;
    }

    .teams{
        gap: 2vmin;
        position: relative;
        flex-grow: 1;
        flex-grow: 1;
        align-items: center;
        justify-content: space-evenly;
        height: 100%;
    }

    /* .teams::after{
        content: "";
        width: 100%;
        height: 3px;
        position: absolute;
        top: 50%;
        left: 210%;
        transform: translateY(-50%);
        background-color: #9146ff;
    } */

    .step:nth-last-child(1) .teams:nth-last-child(1)::after, .step:nth-last-child(1) .teams:nth-last-child(1)::before, .step:nth-last-child(1) .teams .team:last-of-type::after, .step:nth-last-child(1) .teams .team:last-of-type::before{
        display: none;
    }

    .team{
        color: #fff;
        position: relative;
        height: 100%;
        justify-content: center;
    }

    /* .team::after{
        content: "";
        width: 100%;
        height: 3px;
        position: absolute;
        top: 50%;
        left: 110%;
        transform: translateY(-50%);
        background-color: #9146ff;
    } */

    /* .team:last-of-type::after{
        display: none;
    } */

     .top{
         position: absolute;
         width: 100%;
         height: 3px;
         top: 0;
         background-color: #9146ff;
     }

     .bottom{
         position: absolute;
         width: 100%;
         height: 3px;
         bottom: 0;
         background-color: #9146ff;
     }

     .winner{
         position: absolute;
         width: 100%;
         height: 3px;
         background-color: #9146ff;
         left: 100%;
     }

     .line{
         position: absolute;
         width: 3px;
         height: 100%;
         background-color: #9146ff;
         top: 0;
         right: 0;
     }
</style>