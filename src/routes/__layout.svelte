<script>
    import { fade } from 'svelte/transition';
    import { page } from '$app/stores';
</script>

<header>
    <a href="/">
        <img src="/logo.webp" alt="logo" width="134" height="54">
    </a>
    <nav>
        <a href="/" class='{$page.url.pathname === "/" ? "active" : ""}'>Home</a>
        <a href="/projects" class='{$page.url.pathname === "/projects" ? "active" : ""}' sveltekit:prefetch>Projects</a>
        <a href="/contact" class='{$page.url.pathname === "/contact" ? "active" : ""}'>Contact</a>
    </nav>
</header>

{#key $page.url.pathname}
<main in:fade>
    <slot/>
</main>
{/key}

<footer>
    <a target="_blank" href="https://www.instagram.com/alvaro.soewardono/" rel="noopener">@alvaro.soewardono</a>
</footer>

<style>
    header > a {
        position: fixed;
        left: 2em;
        top: 2em;
    }

    header a img {
        width: 8.4em;
        height: auto;
    }

    a {
        text-decoration: none;
        color: inherit;
    }

    header nav {
        display: flex;
        flex-direction: column;
        gap: 2.8em;

        position: fixed;
        left: 1em;
        top: 50%;
        transform: translateY(-50%);
        font-size: 1.8em;
    }

    header nav a {
        padding: .2em .4em;
        align-self: flex-start;

        background: linear-gradient(to left, white 50%, black 50%) right;
        background-size: 197%;
        background-repeat: no-repeat;
    }

    @media (min-width: 1000px) {
        header nav a { transition: background .3s ease-out, color .2s ease-out }
    }

    header nav a:hover, .active {
        background-position: left;
        color: white;
    }

    main {
        font-size: 1.6em;
        margin: 4.8em 8.1em 1em 8.1em;
    }

    footer {
        position: fixed;
        right: 1em;
        top: 50%;
        transform: translateY(-50%);
        font-size: 1.8em;
    }

    @media (max-width: 1000px) {
        main {
            margin: 9em 2em 2em 12em;
            font-size: 1em;
        }

        footer {
            display: none;
        }
    }

    @media (max-height: 640px) and (orientation: landscape) {
        header > a {
            display: none
        }

        header nav {
            font-size: 1.4em;
            gap: 1em;
        }

        main {
            margin-top: 4em;
        }

        footer {
            display: none;
        }
    }

    footer a {
        display: inline-block;
        font-size: .8em;
        transform: rotate(90deg);
        color: #555;
        transition: color .3s ease-out;

        background-image: 
            linear-gradient(-135deg, #f09433 0%,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888 100%);
        background-clip: text;
        -webkit-background-clip: text;
        
    }

    footer a:hover {
        color: #55555509;
    }
</style>