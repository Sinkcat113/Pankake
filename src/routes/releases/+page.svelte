<script>

    import Starblast from "../../lib/StarblastCover.png"
    import Dorayaki from "../../lib/DorayakiCover.png"
    import Hyperdrive from "../../lib/HyperdriveCover.png"

    import { releases } from "./releases.js"

    import Release from "./release.svelte"

</script>

<main>
    <div class="content">
        <h1 class="releasies">Releases</h1>
    </div>
    <div class="releases">
        {#each releases as release}
            {#if release.title === "Starblast"}
                <Release title={release.title} link={release.link} cover={Starblast}/>
            {:else if release.title === "Dorayaki"}
                <Release title={release.title} link={release.link} cover={Dorayaki}/>
            {:else if release.title === "Hyperdrive"}
                <Release title={release.title} link={release.link} cover={Hyperdrive}/>
            {/if}
        {/each}
    </div>
    <div class="usageContent" id="UsagePolicy">
        <h1>Usage Policy</h1>

        <div class="prefix">
            <p style="text-align: center; margin: 2px;">By using my work in your content, you are agreeing to the rules stated below. For any questions or special inquiries about the usage policy, please send an email to PankakeMedia@outlook.com</p>
            <br>
            <u><p style="text-align: center;">If any of the following policies are violated, your content may be claimed and/or copyright striked. If commercial use of my work is executed without a license, proper legal action will be pursued</p></u>
            <br>
            <p style="text-align: center;">This usage policy is current as of January 21, 2024</p>
        </div>

        <br>
        <div class="policy">
            <ul>
                <li style="font-weight: 900; font-size: 20px;">YouYube</li>
                <p>State the artist name (Pankake) and put the song title in the description, as well as a link to my YouTube and Linktree</p>
            </ul>
        </div>
        <div class="policy">
            <ul>
                <li style="font-weight: 900; font-size: 20px;">Livestreams</li>
                <p>CLEARLY display the track name and artist on your livestream (NOT IN THE DESCRIPTION). This applies even if the music is being used as “background music”.</p>
            </ul>
        </div>
        <div class="policy">
            <ul>
                <li style="font-weight: 900; font-size: 20px;">Games</li>
                <p>If you want to use my works in your game, please contact me via email for a licensing fee. If you are a fan wanting to use my music for a FAN-MADE-LEVEL please refer to the below bullet point before deciding to make one.</p>
                <ul>
                    <li>Usage of my music in the following games is NOT allowed:</li>
                    <ul>
                        <li>Geometry Dash</li>
                    </ul>
                </ul>
                <p>(This is subject to change)</p>
            </ul>
        </div>
        <div class="policy">
            <ul>
                <li style="font-weight: 900; font-size: 20px;">Remixes/Edits</li>
                <p>You are more than welcome to remix or make edits of my tracks! I’m honored you’ve considered it. Please follow the guidelines below for publishing your work:</p>
                <ul>
                    <li>If you wish to distrubite the work on platforms such as Apple Music, Apotify, YouTube Music (not a YouTube video), or other streaming services and sotres, you must contact me via email to discuss a licensing fee, as well as distribution. Distribution of this nature makes the work “commercial use”.</li>
                    <li>You may publish the remix/edit on platforms such as SoundCloud or YouTube (as a video) with monetezation turned off. Credit must follow the same guidelines as the YouTube bullet point (yes, even on SoundCloud)</li>
                </ul>
                <p>Oh, and one final thing…have fun with it! And make sure you let me know that you did something through tagging me in a tweet or other social media post, through email, or by saying something in my discord server! This is entirely optional, but I’d love to see what you all end up doing with my works! ❤</p>
            </ul>
        </div>
        <br>
        <br>
        <br>
    </div>
</main>

<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');

    .content {
        width: 800px;
        margin-top: 200px;
        margin-left: auto;
        margin-right: auto;
    }

    .prefix {
        padding: 20px;
        border-style: solid;
        border-width: 1px;
        border-color: #6b6b6b3f;
        border-radius: 20px;
        font-weight: 800;
        background-color: #0d1110;
    }

    .policy {
        padding: 20px;
        background-color: rgba(255, 255, 255, 0.055);
        border-radius: 20px;
        color: white;
        margin-top: 12px;
        transition: 0.12s;
    }

    .policy:hover {
        cursor: pointer;
        scale: 105%;
        background-color: rgba(255, 255, 255, 0.11);
    }

    .usageContent {
        width: 800px;
        margin-top: 100px;
        margin-left: auto;
        margin-right: auto;
        font-family: "DM Sans", sans-serif;
        color: #7fffd0;
    }

    .releases {
        display: flex;
        width: 830px;
        margin-left: auto;
        margin-right: auto;
    }

    .releasies {
        font-family: "DM Sans", sans-serif;
        background-image: linear-gradient(#aaffe0, #4d947a);
        background-clip: text;
        -webkit-text-fill-color: transparent;
        animation-name: slideUp;
        animation-duration: 0.90s;
    }

    @media (max-width: 600px) {
        .content {
            margin-top: 140px;
            animation-name: slideUpFade;
            width: 300px;
        }

        .releases {
            width: 320px;
        }

        .releasies {
            margin-top: 40px;
            animation-name: slideUpFade;
        }

        h1 {
            margin-top: 140px;
        }

        .usageContent {
            width: 300px;
        }

        @keyframes slideUpFade {
            from {
                margin-top: 160px;
                opacity: 0%;
            }

            to {
                margin-top: 140px;
            }
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