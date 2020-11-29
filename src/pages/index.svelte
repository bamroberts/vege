<script>
    import RoutifyIntro from './example/_components/RoutifyIntro.svelte'
    import { metatags } from '@roxi/routify'
    metatags.title = 'My Vege Garden'
    metatags.description = 'A subscripotion service for veggies to grow your self'
    import { fly, fade } from 'svelte/transition';

    let sent = false;
</script>
<style>
    form {
        font-size:2vmin;
        width:80ch;
        grid-area:b;
        background-color:rgba(255,255,255,0.8);
        padding:20px;
        border-radius:10px;
        place-self: center;
        margin-bottom:1em;

        font-family: sans-serif;

    }

    p {
        font-size:1.5em;
        font-weight: bold;
    text-align: center;
    }

    label {font-weight:bold;
    margin:40px 0px 20px;
    font-size:2em;
    }

    div {
        display:flex;
        align-items: center;
        justify-content: center;
        
        }

        hr {
            background-color: #3F6D49;
            height:3px;
            width:40ch;
            padding-bottom:10px;
            margin-bottom: 10px;;
        }

        input {flex-grow: 1;}

        input, button {
            font-size: min(2em, 4vw);
        }

        button {background-color:#E48B3E;
        color:white;
        font-weight: bold;
        text-transform:uppercase;
        text-shadow:0 0 1px black;
        cursor: pointer;}

        p.sent {
            text-align:left;
            font-weight:100;

        } 

        p.sent b {
            color:#E48B3E;
        }

        .holder {
            display: grid;
            grid-template-areas: 'c';
        
        } 
        .holder > * {
            grid-area:c;
        }
</style>
<form on:submit|preventDefault={()=>sent=true}>
    <p>
        My Vege Garden is a subscripton based service to deliver both monthly fresh seedlings and the quiptment needed to grow them.
    </p>
    <hr >
    <span class=holder>
    {#if sent} 

   
    <p transition:fade class="sent"> <strong>Thanks!</strong><br />Great to have you on board. We will be in contact when our new vege growing system is closer to launch! Thanks for being a supporter of <b>My Vege Box</b>!</p>
    {:else}
    <span out:fade>
        <label for=email>Sign up to find out more</label>
        <div>
        
        <input type=email name=email />
        <button>Signup</button>
        </div>
    </span>
    {/if}
</span>
</form>
<!-- 
<div>
    <img src="/images/57654451be1169988ac17a8b4b2954aa.jpg" alt="Basket of veg"/>
<p>
    My Vege Garder is a subscripton based service to deliver both monthly fresh seedlings and the quiptment needed to grow them.
</p>
</div> -->