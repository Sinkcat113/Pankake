<script>
    import sky from "../lib/Sky.png"
    import Card from "./card.svelte";

    import bandcamp from "../lib/social.png"
    import instagram from "../lib/instagram.png"
    import mastodon from "../lib/mastodon.png"
    import youtube from "../lib/youtube.png"
    import twitter from "../lib/twitter.png"
    import bluesky from "../lib/bluesky.png"
    import spotify from "../lib/spotify.png"
    import soundcloud from "../lib/soundcloud.png"
</script>

<main>
    <div class="content">
        <img class="sky" src={sky} alt="">
        <div class="text">
            <h1>Welcome To My Website!</h1>
            <h4>My name is Pankake! <br> I’m an electronic music producer, sound designer, and <br> audio engineer based in the Southwestern US!</h4>
        </div>
    </div>

    <p>Here are some links to get you started! ❤</p>
    <div class="cards">
        <Card link="https://pankake.bandcamp.com/music" service="Bandcamp" logo={bandcamp} />
        <Card link="https://www.instagram.com/pankake_42/" service="Instagram" logo={instagram} />
        <Card link="https://mastodon.social/@pankakes42" service="Mastodon" logo={mastodon} />
        <Card link="https://www.youtube.com/@pankakes42" service="YouTube" logo={youtube} />
        <Card link="https://twitter.com/PankakeMusic42" service="Twitter" logo={twitter} />
        <Card link="https://bsky.app/profile/pankake.bsky.social" service="Bluesky" logo={bluesky} />
        <Card link="https://open.spotify.com/artist/4hif2fsIckXtDxrgLtjMwT" service="Spotify" logo={spotify} />
        <Card link="https://soundcloud.com/pankakes_music" service="SoundCloud" logo={soundcloud} />
    </div>
</main>

<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');


    .cards {
        display: flex;
        flex-wrap: wrap;
        width: 800px;
        margin-left: auto;
        margin-right: auto;
    }

    h1 {
        text-align: center;
        margin: 0;
        margin-top: 100px;
        font-family: "DM Sans", sans-serif;
        font-weight: 1000;
        font-size: 50px;
        color: #38fdb5;
        background-image: linear-gradient(#aaffe0, #4d947a);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        animation-name: slideDown;
        animation-duration: 1.3s;
    }

    h4 {
        text-align: center;
        font-family: "DM Sans", sans-serif;
        font-weight: 500;
        background-image: linear-gradient(#aaffe0, #7fffd0,#4d947a);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        animation-name: fade;
        animation-duration: 1s;
    }

    .sky {
        margin-top: 10vh;
        display: block;
        height: 300px;
        filter: drop-shadow(100px -30px 200px #00be78);
        animation-name: slideFade;
        animation-duration: 0.80s;
        border-radius: 500px;
        background-image: linear-gradient(110deg,  transparent, #7cf1c6);
    }

    .content {
        display: flex;
        margin-left: auto;
        margin-right: auto;
        width: 800px;
        margin-top: 50px;
    }

    p {
        width: 780px;
        margin: 0;
        margin-left: auto;
        margin-right: auto;
        margin-top: 40px;
        font-family: "DM Sans", sans-serif;
        font-weight: 800;
        color: rgba(240, 248, 255, 0.589);

    }

    @keyframes slideFade {
        from {
            margin-top: 20vh;
            opacity: 0%;
            filter: none;
        }

        to {
            margin-top: 10vh;
        }
    }

    @keyframes slideDown {
        from {
            margin-top: 120px;
            opacity: 0%;
        }

        to {
            margin-top: 100px;
        }
    }

    @keyframes fade {
        from {
            opacity: 0%;
        }

        to {
            opacity: 100%;
        }
    }
</style>