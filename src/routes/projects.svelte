<svelte:head>
    <title>Projects</title>
</svelte:head>

<h1>Check out some of my projects</h1>
<div class="gallery">
    <picture>
        <source srcSet="/projects/kebaikan.avif" type="image/avif">
        <img src="/projects/kebaikan.webp" alt="kebaikan" width="462" height="653">
    </picture>
    <a href="/projects/ilmiah.pdf" rel="external">
        <picture>
            <source srcSet="/projects/ilmiah.avif" type="image/avif">
            <img src="/projects/ilmiah.webp" alt="ilmiah" width="462" height="746">
        </picture>
    </a>
    <picture>
        <source srcSet="/projects/warming.avif" type="image/avif">
        <img src="/projects/warming.webp" alt="warming" width="462" height="259">
    </picture>
    <picture>
        <source srcSet="/projects/sidang.avif" type="image/avif">
        <img src="/projects/sidang.webp" alt="sidang" width="462" height="653">
    </picture>
    <picture>
        <source srcSet="/projects/pergaulan.avif" type="image/avif">
        <img src="/projects/pergaulan.webp" alt="pergaulan" width="462" height="259">
    </picture>
</div>

<style>
    .gallery {
        line-height: 0;
        column-count: 2;
        gap: .4em;
    }

    img, picture {
        width: 100%;
        height: auto;
        margin: .2em 0;
        transition: .5s ease-out;
        position: relative;
        overflow: hidden;
    }

    @media (max-width: 1000px) {
        .gallery {
            column-count: 1;
        }
    }
</style>