<!-- routify:options preload="proximity" -->
<style>
    header {
        display:grid;
        height: 100vh;
        background-color:aliceblue;
        background: url('/images/vegetables-wallpaper-20.jpg');
        background-repeat: no-repeat;
        background-size: cover;
    }

    h1 {
        align-self: top;
        text-transform:uppercase;
        font-size:max(18vmin, 10em);
        width:100px;
        margin:0;
        line-height:1;
        color:#3F6D49;
        text-shadow:2px 2px 30px rgba(255,255,255.1), 1px 1px 2px rgba(0,0,0,0.4);
    }
</style>
<header>
    <h1>My Vege Garden</h1>
</header>
<slot />
