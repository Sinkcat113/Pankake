<script>
    import {page} from "$app/stores"

</script>

<div class="menu">
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

<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');


    .menu {
        left: 0;
        top: 67px;
        bottom: 0;
        position: fixed;
        width: 200px;
        z-index: 100;
        padding: 20px;
        background-color: white;
        background-color: rgba(26, 26, 26, 0.863);
        backdrop-filter: blur(100px);
        -webkit-backdrop-filter: blur(100px);
        box-shadow: 4px 5px 60px rgba(0, 0, 0, 0.233);
        animation-name: slideIn;
        animation-duration: 0.30s;
        animation-timing-function: cubic-bezier(0.165, 0.84, 0.44, 1);
        display: block;
        padding-left: 0;
        padding-right: 0;
    }

    .option {
        width: 100%;
        margin-top: 12px;
        cursor: pointer;
        padding: 20px;
        font-family: "DM Sans", sans-serif;
        font-weight: 800;
        background-color: transparent;
        border: none;
        color: rgba(255, 255, 255, 0.562);
        transition: 0.12s;
    }

    .option:hover {
        background-color: rgba(255, 255, 255, 0.055);
    }

    .optionSelected {
        width: 100%;
        margin-top: 12px;
        cursor: pointer;
        padding: 20px;
        font-family: "DM Sans", sans-serif;
        font-weight: 800;
        background-color: transparent;
        border: none;
        color: rgb(255, 255, 255);
        text-shadow: 0px 0px 30px rgb(56, 255, 145);
        background-color: rgba(255, 255, 255, 0.089);
        border-right-style: solid;
        border-right-color: rgb(56, 255, 145);
        transition: 0.12s;
    }

    @keyframes slideIn {
        from {
            width: 0px;
        }

        to {
            width: 200px;
        }
    }
</style>