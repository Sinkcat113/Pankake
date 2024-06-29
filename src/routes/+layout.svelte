<script>
    import Nav from "./nav.svelte";


</script>

<svelte:head>
    <title>Pankake</title>
</svelte:head>

<main>
    <Nav />
    <slot />
</main>

<style>
    :global(body) {
        background-color: #171717;
    }
</style>