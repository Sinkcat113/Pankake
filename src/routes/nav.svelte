<script>
    import { page } from "$app/stores"

    import hamburger from "../lib/more.png"
    import close from "../lib/close.png"
    import Menu from "./menu.svelte";

    let menuOpen = false

    const menu = () => {
        if (menuOpen) {
            menuOpen = false
        } else if (!menuOpen) {
            menuOpen = true
        }
    }
</script>

{#if menuOpen}
    <Menu />
{/if}

<div class="nav">
    {#if menuOpen === false} 
        <button class="burger" on:click={menu}><img class="imgHamMenu" src={hamburger} alt=""></button>
    {:else}
        <button class="burger" on:click={menu}><img class="imgHamMenu" src={close} alt=""></button>
    {/if}

    <a href="/"><h2 class="logo">Pankake</h2></a>
    {#if menuOpen === false}
        <div class="options">
            {#if $page.url.pathname == "/"}
                <a href="/releases"><button class="option">Releases</button></a>
                <a href="/gear"><button class="option">Gear</button></a>
                <a href="/contact"><button class="option">Contact</button></a>
                <a href="/about"><button class="option">About</button></a>
            {:else if $page.url.pathname == "/releases"}
                <a href="/releases"><button class="optionSelected">Releases</button></a>
                <a href="/gear"><button class="option">Gear</button></a>
                <a href="/contact"><button class="option">Contact</button></a>
                <a href="/about"><button class="option">About</button></a>
            {:else if $page.url.pathname == "/gear"}
                <a href="/releases"><button class="option">Releases</button></a>
                <a href="/gear"><button class="optionSelected">Gear</button></a>
                <a href="/contact"><button class="option">Contact</button></a>
                <a href="/about"><button class="option">About</button></a>
            {:else if $page.url.pathname == "/contact"}
                <a href="/releases"><button class="option">Releases</button></a>
                <a href="/gear"><button class="option">Gear</button></a>
                <a href="/contact"><button class="optionSelected">Contact</button></a>
                <a href="/about"><button class="option">About</button></a>
            {:else if $page.url.pathname == "/about"}
                <a href="/releases"><button class="option">Releases</button></a>
                <a href="/gear"><button class="option">Gear</button></a>
                <a href="/contact"><button class="option">Contact</button></a>
                <a href="/about"><button class="optionSelected">About</button></a>
            {/if}
        </div>
    {/if}
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Tiny5&display=swap');

    a {
        text-decoration: none;
    }

    .nav {
        top: 0;
        left: 0;
        right: 0;
        position: fixed;
        padding: 20px;
        background-color: rgba(24, 24, 24, 0.678);
        backdrop-filter: blur(100px);
        -webkit-backdrop-filter: blur(100px);
        z-index: 1000;
        display: flex;
        box-shadow: 0px 0px 80px rgba(0, 0, 0, 0.199);
    }

    .options {
        display: flex;
        margin-left: 20px;
    }

    .option {
        background-color: transparent;
        border: none;
        font-size: 17px;
        color: #dbfff2af;
        font-weight: 500;
        font-family: "DM Sans", sans-serif;
        cursor: pointer;
        transition: 0.20s;
        border-radius: 12px;
        height: 30px;
        padding-left: 15px;
        padding-right: 15px;
        margin-left: 12px;
    }

    .option:hover {
        background-color: rgba(255, 255, 255, 0.041);
        color: #d8fff1;
        text-decoration: underline;
        text-underline-offset: 25px;
    }


    .optionSelected {
        background-color: transparent;
        border: none;
        font-size: 17px;
        color: #dbfff2af;
        font-weight: 500;
        font-family: "DM Sans", sans-serif;
        cursor: pointer;
        transition: 0.20s;
        border-radius: 12px;
        height: 30px;
        padding-left: 15px;
        padding-right: 15px;
        margin-left: 12px;
        background-color: rgba(255, 255, 255, 0.041);
        color: #d8fff1;
        text-decoration: underline;
        text-underline-offset: 25px;
    }


    .logo {
        cursor: pointer;
        font-family: "Tiny5", sans-serif;
        font-weight: 200;
        margin: 0;
        color: #38fdb5;
        transition: 0.12s;
    }

    .logo:hover {
        scale: 105%;
    }

    .logo:active {
        scale: 95%;
    }

    .burger {
        background-color: transparent;
        border-style: none;
        margin-right: 20px;
        cursor: pointer;
        margin-top: 2px;
    }

    .burger:active {
        scale: 90%;
        z-index: 1200;
    }

    .imgHamMenu {
        width: 20px;
        height: 20px;
        filter: invert(1);
    }
    

    @media (max-width:600px) {
        .options {
            display: none;
        }

        .burger {
            display: flex;
        }


    }
</style>