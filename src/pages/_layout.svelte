<!-- routify:options preload="proximity" -->
<style>
    :global(body) {
        background-color:#3F6D49;
        margin:0;
        padding:0;
    }
    header {
        display:grid;
        height:100vh;
        min-height:100%;
        background-color:aliceblue;
        background: url('/images/vegetables-wallpaper-20.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        grid-template-areas: 'a'
        'b';
        grid-template-rows: 1fr min-content;
    }

    h1 {
        grid-area: a;
        align-self: top;
        text-transform:uppercase;
        font-size:clamp(5em, 10vmin, 10em);
        width:100px;
        margin:0;
        line-height:1;
        color:#3F6D49;
        text-shadow: 1px 1px 2px rgba(0,0,0,0.4), 2px 2px 150px rgba(255,255,255.1), 2px 2px 50px rgba(255,255,255.1);
    }
    h3 {
        grid-area: a;
    color: #E48B3E;
    font-size: 1.5em;
    width: 300px;
    border-bottom: 0.4em solid #E48B3E;
    right: 0;
    justify-self: end;
    text-align: right;
    margin-right: 2em;
    align-self: baseline;
    padding-bottom: 20px;
    overflow: visible;
    padding-top: 00;
    margin-top: 10px;
    margin-right: 3vw;
    text-shadow: 1px 1px 2px rgba(0,0,0,0.4), 2px 2px 150px rgba(255,255,255.1), 2px 2px 50px rgba(255,255,255.1);

    }

    h3 span {display:block;}
</style>
<header>
    <h1>My Vege Garden</h1>
    <h3>Exceed <span>in Gardening</span></h3>
    <slot />
</header>


