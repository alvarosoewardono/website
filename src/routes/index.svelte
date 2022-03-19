<svelte:head>
    <title>Home</title>
</svelte:head>

<h1>A little about me...</h1>
<h2>My name's <span class="name">Alvaro Raditya Soewardono</span>. I'm a <span class="profession">student</span> born in <span class="location">Jakarta, Indonesia</span>. I like learning web & system technologies.</h2>

<style>
    h1 {
        font-size: 2.4em;
    }

    h2 {
        font-size: 1.6em;
        font-weight: 400;
    }

    span {
        text-decoration: underline;
        color: #00000020;
    }

    .name {
        background: linear-gradient(90deg, #1CB5E0 0%, #000851 100%);
        background-clip: text;
        -webkit-background-clip: text;
    }

    .profession {
        background: linear-gradient(to right, #ef473a, #cb2d3e);
        background-clip: text;
        -webkit-background-clip: text;
    }

    .location {
        background: linear-gradient(90deg, #9ebd13 0%, #008552 100%);
        background-clip: text;
        -webkit-background-clip: text;
    }
</style>