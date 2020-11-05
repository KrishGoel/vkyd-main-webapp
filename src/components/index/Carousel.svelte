<script>

    let cdn = "https://lcfr.vkyd.in"

    let slides = [
		{
            url: '/lol',
            label: 'lolol',
            src: 'https://dvyvvujm9h0uq.cloudfront.net/com/articles/1514474020-tips-for-aspiring-fashion-models.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://i.pinimg.com/736x/b8/ea/d7/b8ead72eb31d8918095e83b4fa4cc19e.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://i.pinimg.com/736x/10/a4/8f/10a48fe898aeba869e9180dcdfb6105d.jpg',
            alt: 'lololol'
        },
        {
            url: '/lol',
            label: 'lolol',
            src: 'https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/0414-hoodie-2-1586901031.jpg',
            alt: 'lololol'
        }
    ];

    let slidesCount = slides.length;

</script>

<div class="carousel">
    {#each slides as slide, i}
        <div class="slide">
            {#if i > 0}
                <a href="{slide.url}" aria-label="{slide.label}" style="margin-left: 15px">
                    <img src="{slide.src}" alt="{slide.alt}" />
                </a>
            {:else}
                <a href="{slide.url}" aria-label="{slide.label}">
                    <img src="{slide.src}" alt="{slide.alt}" />
                </a>
            {/if}            
        </div>
    {/each}
</div>

<style>
    :root {
        --carousel-lg-height: 300px; /* Carousel height for large devices */
        --carousel-xs-height: 300px; /* Carousel height for small devices */
        --carousel-border-radius: 20px;
    }
    .carousel {
        width: 100%;
        white-space: nowrap;
        overflow-x: scroll;
        border-radius: var(--carousel-border-radius);
        /* Hiding x-scroll on IE, Edge and Firefox*/
        -ms-overflow-style: none;  /* IE and Edge */
        scrollbar-width: none;  /* Firefox */
    }
    /* Hiding x-scroll on Chrome, Opera and Safari*/
    .carousel::-webkit-scrollbar {
        display: none;
    }
    .slide {
        display: inline-block;
    }
    .slide img{
        height: var(--carousel-lg-height);
        border-radius: var(--carousel-border-radius);
    }
    @media screen and (max-width: 400px) {
        .slide img {
            height: var(--carousel-xs-height);
        }
    }
</style>