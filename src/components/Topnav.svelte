<script>
    import HamburgerIcon from '../components/chunks/hamburger-icon.svelte';

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
            <h1 class="head" id="logo">VKYD</h1>
            <div id="shopping-cart-icon">
                <img src="media/icons/shopping-bag.png" alt="">
            </div>
        </div>
    </div>
    {#if sidenavState}
        <div class="side-nav">
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
        width: 100%;
        background-color: #ffffff;
        box-shadow: 7px 7px 21px -10px #4c00af;
        padding: 15px 0px;
        position: fixed;
        top: 0px
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
        width: 450px;
        position: fixed;
        z-index: 5;
        top: 0;
        left: 0;
        overflow-x: hidden;
        transition: 0.2s;
        background-color: #000000;
    }
    @media screen and (max-width: 600px) {
        .side-nav {
            width: 100vw;
        }
    }
    .side-nav #close-icon img {
        width: 22px;
        position: absolute;
        top: 28px;
        left: calc(5vw + 2px)
    }
    
    .side-nav a {
        color: #ffffff;
        transition: 0.2s;
        line-height: 50px;
    }
    .side-nav a:hover {
        text-shadow: 0px 0px 0 #fad276, 1px 1px 0 #f5883b, 2px 2px 0 #f15c32, 3px 3px 0 #eb2c46, 4px 4px 0 #e60361, 5px 5px 0 #da0171, 6px 6px 0 #b00999, 7px 7px 0 #8512be, 8px 8px 0 #661fd1, 9px 9px 0 #5327dc, 10px 10px 0 #4332e6;
    }
    .side-nav #instagram:hover {
        /* text-shadow: 0px 0px 0 #fad276, 1px 1px 0 #f5883b, 2px 2px 0 #f15c32, 3px 3px 0 #eb2c46, 4px 4px 0 #e60361, 5px 5px 0 #da0171, 6px 6px 0 #b00999, 7px 7px 0 #8512be, 8px 8px 0 #661fd1, 9px 9px 0 #5327dc, 10px 10px 0 #4332e6; */
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
            padding-left: calc(5vw + 2px)
        }
    }
    @media screen and (max-width: 600px) {
        .side-nav #links {
            text-align: center;
        }
    }
</style>