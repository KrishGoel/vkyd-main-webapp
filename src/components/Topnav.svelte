<script>
    import { slide } from 'svelte/transition';
    import { fade } from 'svelte/transition';
    import { clickOutside } from '../components/mini-js/clickOutside.js';

    import HamburgerIcon from '../components/chunks/hamburger-icon.svelte';

    const cdn = "https://lcfr.vkyd.in";

    var sidenavState = false;
    function openSidenav() {
		sidenavState = true;
	}
    function closeSidenav() {
		sidenavState = false;
	}
</script>

<nav>
    <!-- <Headroom offset={100} tolerance={5}> -->
    <div class="top-nav">
        <div class="width-restriction">
            <div id="hamburger-icon" on:click={openSidenav}>
                <HamburgerIcon />
            </div>
            <!-- <h1 class="head" id="logo">VKYD</h1> -->
            <img src="{cdn}/logos/vkyd-logo.svg" alt="VKYD Logo"/>
            <div id="shopping-cart-icon">
                <img src="{cdn}/icons/website/shopping-bag.png" alt="Shopping Cart">
            </div>
        </div>
    </div>
    <!-- </Headroom> -->
    {#if sidenavState}
        <div class="side-nav" use:clickOutside transition:slide='{{duration: 500}}' on:click_outside={closeSidenav}>
            <div id="close-icon" on:click={closeSidenav}>
                <img src="{cdn}/icons/website/close.png" alt="Close side navigation bar">
            </div>
            <br><br><br><br><br><br>
            <div id="links">
                <a href="/story" aria-label="Our Story"><h3>Our Story</h3></a>
                <a href="/lookbook" aria-label="Lookbook"><h3>Lookbook</h3></a>
                <a href="/wallpapers" aria-label="Wallpapers"><h3>Wallpapers</h3></a>
                <a href="/team" aria-label="The Team"><h3>The Team</h3></a>
                <br>
                <br>
                <div class="social-icons" transition:slide="{{duration: 200}}">
                    <a href="https://instagram.com/vkydclothing" id="instagram" aria-label="VKYD Instagram">
                        <img src="{cdn}/icons/social-media/instagram.svg" alt="Instagram Icon" />
                    </a>
                    <a href="https://instagram.com/vkydclothing" aria-label="VKYD Snapchat">
                        <img src="{cdn}/icons/social-media/snapchat.svg" alt="Snapchat Icons"/>
                    </a>
                    <a href="https://instagram.com/vkydclothing" aria-label="VKYD Facebook">
                        <img src="{cdn}/icons/social-media/facebook.svg" alt="Facebook Icon" />
                    </a>
                    <a href="https://instagram.com/vkydclothing" aria-label="VKYD Spotify">
                        <img src="{cdn}/icons/social-media/spotify.svg" alt="Spotify Icon" />
                    </a>
                    <a href="https://instagram.com/vkydclothing" aria-label="VKYD Twitter">
                        <img src="{cdn}/icons/social-media/twitter.svg" alt="Twitter Icon" />
                    </a>
                </div>
            </div>
            <div class="width-restriction">
            </div>
        </div>
    {/if}
</nav>

<style>
    /* Purely topnav styling */
    :root {
        --topnav-width: 95vw;
    }
    .top-nav {
        width: var(--topnav-width);
        position: fixed;
        left: calc((100vw - var(--topnav-width))/2);
        top: calc((100vw - var(--topnav-width))/2);
        z-index: 1;
        /* margin-left: 2.5vw;
        margin-right: 2.5vw;
        margin-top: 2.5vw; */
        background: linear-gradient(266.6deg, #1F2224 46.48%, #1A1D1F 61.97%);
        box-shadow: 14px 14px 50px 10px #0C0D0E, inset 14px 14px 10px rgba(46, 51, 54, 0.2);
        border-radius: 20px;
        padding: 10px 0;
    }    
    .top-nav .width-restriction {
        display: flex;
		justify-content: space-between;
		align-items: center;
    }
    
    /* Element specific styling */
    .top-nav #shopping-cart-icon img {
        width: 22px
    }
    .top-nav #hamburger-icon {
        padding-top: 6px
    }

    /* Sidenav styling */
    .side-nav {
        height: 100vh;
        width: 400px;
        position: fixed;
        z-index: 5;
        top: 0;
        left: 0;
        overflow-x: hidden;
        border-top-right-radius: 30px;
        border-bottom-right-radius: 30px;
        background-color: var(--dark-smoke);
        box-shadow:  33px 33px 65px #0c0d0e, -33px -33px 65px #2e3336;
        transition: 0.2s;
    }
    @media screen and (max-width: 600px) {
        .side-nav {
            width: 100vw;
        }
    }
    .side-nav #close-icon img {
        width: 22px;
        position: absolute;
        top: calc(2.5vw + 25px);
        left: calc(2.5vw + 0.05*95vw)
    }
    
    .side-nav a h3{
        color: var(--text-gray);
        transition: 0.2s;
        line-height: 50px;
    }
    .side-nav a h3:hover {
        text-shadow: 0px 0px 0 #fad276, 1px 1px 0 #f5883b, 2px 2px 0 #f15c32, 3px 3px 0 #eb2c46, 4px 4px 0 #e60361, 5px 5px 0 #da0171, 6px 6px 0 #b00999, 7px 7px 0 #8512be, 8px 8px 0 #661fd1, 9px 9px 0 #5327dc, 10px 10px 0 #4332e6;
        color: var(--almost-white)
    }
    .side-nav a img {
        padding: 5px;
        background-color: var(--text-gray);
        border-radius: 40%;
        transition: 0.2s
    }
    .side-nav a img:hover {
        box-shadow: 0px 0px 0 #fad276, 1px 1px 0 #f5883b, 2px 2px 0 #f15c32, 3px 3px 0 #eb2c46, 4px 4px 0 #e60361, 5px 5px 0 #da0171, 6px 6px 0 #b00999, 7px 7px 0 #8512be, 8px 8px 0 #661fd1, 9px 9px 0 #5327dc, 10px 10px 0 #4332e6;
        background-color: var(--almost-white)
    }
    .side-nav a h3 {
        font-weight: 400;
    }
    .side-nav a img {
        width: 25px;
        margin-right: 5px
    }
    @media screen and (min-width: 600px) {
        .side-nav #links {
            padding-left: calc(2.5vw + 0.05*95vw)
        }
    }
    @media screen and (max-width: 600px) {
        .side-nav #links {
            text-align: center
        }
    }
</style>