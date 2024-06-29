<script>
    export let title
    export let link
    export let cover
</script>


<a href={link}>
    <div class="wrapper">
        <img class="cover" src={cover} alt="">
        <h3>{title}</h3>
        {#if title === "Starblast"}
            <p>Debut</p>
        {/if}
        {#if title === "Hyperdrive"}
            <p>Latest</p>
        {/if}
    </div>
</a>



<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');

    .wrapper {
        margin-left: 12px;
        margin-right: 12px;
        padding: 10px;
        background-image: linear-gradient(rgba(255, 255, 255, 0.075), rgba(255, 255, 255, 0.075), transparent);
        border-radius: 20px;
        transition: 0.12s;
        animation-name: slideUp;
        animation-duration: 0.90s;
    }

    .wrapper:hover {
        scale: 105%;
        background-color: rgba(255, 255, 255, 0.144);
    }

    .cover {
        width: 210px;
        height: 210px;
        border-radius: 20px;
    }

    a {
        text-decoration: none;
    }

    p {
        font-family: "DM Sans", sans-serif;
        color: rgba(14, 17, 16, 0.808);
        font-weight: 700;
        text-align: center;
        margin: 0;
        margin-top: 12px;
        padding: 5px;
        padding-left: 12px;
        padding-right: 12px;
        background-color: #61ffc5;
        border-radius: 100px;
        display: flex;
        margin-left: auto;
        margin-right: auto;
        width: 50px;
    }

    h3 {
        font-family: "DM Sans", sans-serif;
        color: rgb(206, 255, 239);
        text-align: center;
        margin: 0;
        margin-top: 12px;
    }

    @media (max-width: 600px) {
        .cover {
            width: 80px;
            height: 80px;
        }

        .wrapper {
            margin: 0;
            margin-right: 3px;
            margin-left: 3px;
        }

        h3 {
            font-size: 14px;
        }

        p {
            font-size: 13px;
            width: 39px;
        }
    }

    @keyframes slideUp {
        from {
            margin-top: 20px;
            opacity: 0%;
        }

        to {
            margin-top: 0px;
        }
    }
</style>