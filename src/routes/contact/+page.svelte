<script>
    import discord from "../../lib/discord.png"
    import twitter from "../../lib/twitter.png"
    import instagram from "../../lib/instagram.png"
</script>

<main>
    <div class="content">
        <h1 style="text-align: center;">Contact</h1>
    </div>
    <div class="contact">
        <a href="https://discord.gg/gfqmvGQJvW"><img class="link" src={discord} alt=""></a>
        <a href="https://twitter.com/PankakeMusic42"><img class="link" src={twitter} alt=""></a>
        <a href="https://www.instagram.com/pankake_42/"><img class="link" src={instagram} alt=""></a>
    </div>
    <p style="text-align: center;">Email: <u>PankakeMedia@outlook.com</u></p>
</main>

<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');

    .content {
        width: 800px;
        margin-top: 200px;
        margin-left: auto;
        margin-right: auto;
    }

    .contact {
        width: 220px;
        margin-left: auto;
        margin-right: auto;
        display: flex;
    }

    .link {
        filter: invert(1) opacity(30%);
        width: 50px;
        height: 50px;
        transition: 0.12s;
        cursor: pointer;
        margin-left: 12px;
        margin-right: 12px;
    }

    .link:hover {
        filter: invert(1) opacity(100%);
    }

    h1 {
        font-family: "DM Sans", sans-serif;
        background-image: linear-gradient(#aaffe0, #4d947a);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        animation-name: slideUp;
        animation-duration: 0.90s;
    }

    p {
        font-family: "DM Sans", sans-serif;
        color: #ffffff;
    }

    a {
        color: #aaffe0;
    }

    @media (max-width: 600px) {
        .content {
            width: 300px;
        }
    }

    @keyframes slideUp {
        from {
            margin-top: 220px;
            opacity: 0%;
        }

        to {
            margin-top: 200px;
        }
    }
    
</style>