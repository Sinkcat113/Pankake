<script>
    import sky from "../../lib/Sky.png"
</script>

<main>
    <div class="content">
        <img class="sky" src={sky} alt="">
        <div class="info">
            <h1>Skylar “Sky” Pankake</h1>
            <p><b>Pronouns:</b> she/her</p>
            <p><b>Born: </b>May 29th, 2000</p>
            <p><b>Intrests: </b>Anime, Gaming, Transit, Music, and Cooking!</p>
        </div>
    </div>
    <br>
    <br>
    <div class="bio">
        <h1>Bio</h1>
        <p style="color: white;">Pankake is an electronic music artist, sound designer, audio engineer, and content creator based in the Southwestern US. Their music features an energetic and heart-pumping sound. Pankake has been producing since late 2014, where they started messing around with different DAWs (Digital Audio Workstations) including FL Studio, ProTools, and REAPER. Having been inspired by video games, rhythm games, and anime; as well as artists such as Camellia, Snail’s House, DJ-Genki, D-D-Dice, RUQOA, Yunomi, MYLK, and others, the music and sounds they’ve crafted over the years has captured the hearts of listeners the world over.</p>
    </div>
</main>

<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');

    .content {
        margin-top: 170px;
        display: flex;
        width: 800px;
        margin-left: auto;
        margin-right: auto;
        padding: 20px;
        background-color: rgba(255, 255, 255, 0.034);
        background-image: linear-gradient(140deg, transparent, #0f3326);
        border-radius: 60px;
        animation-name: slideUp;
        animation-duration: 0.90s;
        border-style: solid;
        border-width: 1px;
        border-color: rgba(240, 248, 255, 0.089);
        box-shadow: 3px 12px 50px rgba(0, 0, 0, 0.192);
    }

    .info {
        margin-left: 20px;
    }

    .bio {
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 800px;
    }

    h1 {
        font-family: "DM Sans", sans-serif;
        background-image: linear-gradient(#aaffe0, #4d947a);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        margin-bottom: 5px;
    }

    p {
        margin: 0;
        font-size: 20px;
        font-family: "DM Sans", sans-serif;
        color: rgba(173, 255, 241, 0.459);
    }

    .sky {
        width: 190px;
        height: 190px;
        border-radius: 500px;
    }

    @keyframes slideUp {
        from {
            margin-top: 190px;
            opacity: 0%;
        }

        to {
            margin-top: 170px;
        }
    }
</style>