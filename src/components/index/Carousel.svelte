<script>
    let cdn = "https://lcfr.vkyd.in"

    let slides = [
		{
            url: '/lol',
            label: 'lolol',
            src: 'https://www.nationalgeographic.com/content/dam/travel/2019-digital/yosemite-guide/yosemite-national-park-california.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://www.nationalgeographic.com/content/dam/travel/2019-digital/yosemite-guide/yosemite-national-park-california.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://www.nationalgeographic.com/content/dam/travel/2019-digital/yosemite-guide/yosemite-national-park-california.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://www.nationalgeographic.com/content/dam/travel/2019-digital/yosemite-guide/yosemite-national-park-california.jpg',
            alt: 'lololol'
        }
	];
</script>

<div class="carousel">
    <div class="slides">
        {#each slides as slide}
            <div class="slide">
                <a href="{slide.url}" aria-label="{slide.label}">
                    <img src="{slide.src}" alt="{slide.alt}" />
                </a>
            </div>
        {/each}
    </div>
</div>

<style>
    :root {
        --carousel-height-large-screen: 200px;
        --carousel-height-small-screen: 150px;
        --scroll-time-large-screen: 20s;
        --scroll-time-small-screen: 10s;
        --carouself-border-radius: 20px
    }
    .carousel {
        height: var(--carousel-height-large-screen);
        position: relative; 
        overflow: hidden;
        border-radius: var(--carouself-border-radius)
    }
    .slides {
        position: absolute; 
        top: 0px; 
        left: 0px; 
        overflow: hidden; 
        white-space: nowrap;
        animation: bannermove var(--scroll-time-large-screen) linear infinite;
    }
    .slide {
        display: inline;
        border-radius: var(--carouself-border-radius);
    }
    .slide img {
        height: var(--carousel-height-large-screen);
        border-radius: var(--carouself-border-radius);
        margin-left: 30px
    }
    @media screen and (max-width: 400px) {
        .slides {
            animation: bannermove var(--scroll-time-small-screen) linear infinite;
        }
        .carousel, .slide img {
            height: var(--carousel-height-small-screen)
        }
    }
    @keyframes bannermove {
        0% {
            transform: translate(0, 0);
        }
        100% {
            transform: translate(-50%, 0);
        }
    }
</style>