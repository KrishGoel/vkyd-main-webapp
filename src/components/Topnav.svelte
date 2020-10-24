<script>
    import { slide } from 'svelte/transition';

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
    <div class="top-nav">
        <div class="width-restriction">
            <div id="hamburger-icon" on:click={openSidenav}>
                <HamburgerIcon />
            </div>
            <!-- <h1 class="head" id="logo">VKYD</h1> -->
            <img src="{cdn}/logos/vkyd-logo.svg" />
            <div id="shopping-cart-icon">
                <img src="media/icons/shopping-bag.png" alt="">
            </div>
        </div>
    </div>
    {#if sidenavState}
        <div class="side-nav" transition:slide>
            <div id="close-icon" on:click={closeSidenav}>
                <img src="media/icons/close.png" alt="">
            </div>
            <br>
            <br>
            <br>
            <br>
            <div id="links">
                <a href="/404"><h3>New Arrivals</h3></a>
                <a href="/404"><h3>Our Story</h3></a>
                <a href="/404"><h3>Lookbook</h3></a>
                <a href="/404"><h3>Wallpapers</h3></a>
                <a href="/404"><h3>The Team</h3></a>
                <br>
                <br>
                <a href="https://instagram.com/vkydclothing" id="instagram">
                    <i class="fab fa-instagram">
                </a>
                <a href="https://instagram.com/vkydclothing">
                    <i class="fab fa-snapchat">
                </a>
                <a href="https://instagram.com/vkydclothing">
                    <i class="fab fa-facebook">
                </a>
                <a href="https://instagram.com/vkydclothing">
                    <i class="fab fa-twitter">
                </a>
                <a href="https://instagram.com/vkydclothing">
                    <i class="fab fa-spotify">
                </a>
                <a href="https://instagram.com/vkydclothing">
                    <i class="fa fa-envelope">
                </a>
            </div>
            <div class="width-restriction">
            </div>
        </div>
    {/if}
</nav>

<style>
    /* Purely topnav styling */
    .top-nav {
        width: 95%;
        background: linear-gradient(266.6deg, #1F2224 46.48%, #1A1D1F 61.97%);
        box-shadow: 14px 14px 50px 10px #0C0D0E, inset 14px 14px 10px rgba(46, 51, 54, 0.2);
        border-radius: 20px;
        position: fixed;
        left: 2.5vw;
        top: 2.5vw;
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
    .top-nav #logo {
        padding-bottom: 6px
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
    
    .side-nav a {
        color: #ffffff;
        transition: 0.2s;
        line-height: 50px;
    }
    .side-nav a:hover {
        text-shadow: 0px 0px 0 #fad276, 1px 1px 0 #f5883b, 2px 2px 0 #f15c32, 3px 3px 0 #eb2c46, 4px 4px 0 #e60361, 5px 5px 0 #da0171, 6px 6px 0 #b00999, 7px 7px 0 #8512be, 8px 8px 0 #661fd1, 9px 9px 0 #5327dc, 10px 10px 0 #4332e6;
    }
    .side-nav a h3 {
        font-weight: 400;
    }
    .side-nav a i {
        font-size: 25px;
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