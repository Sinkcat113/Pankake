<script>

    export let link
    export let service
    export let logo

</script>
 
<div class="container">
    <a href={link}>
        <div class="wrapper">   
            <img src={logo} alt="">
            <p>{service}</p>
        </div>
    </a>
</div>


<style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,100..1000;1,9..40,100..1000&family=Tiny5&display=swap');


    .container {
        margin-top: 20px;
        display: flex;
    }

    .wrapper {
        padding-left: 20px;
        padding-right: 20px;
        margin: 5px;
        background-color: rgba(255, 255, 255, 0.096);
        display: flex;
        border-radius: 50px;
        transition: 0.12s;
    }

    .wrapper:hover {
        background-color: rgba(255, 255, 255, 0.247);
    }

    .wrapper:active {
        scale: 95%;
    }

    img {
        width: 27px;
        height: 27px;
        object-fit: contain;
        margin-right: 12px;
        margin-top: 14px;
        filter: invert(1) opacity(80%);
    }

    a {
        text-decoration: none;
        margin: 0;
    }

    p {
        font-family: "DM Sans", sans-serif;
        color: rgba(255, 255, 255, 0.767);    
    }

    @media (max-width: 600px) {
        .container {
            margin: 0;
            display: grid;
            width: 100%;
            display: grid;
            border-radius: 4px;
        }

        p {
            margin: 0;
            margin-top: 12px;
        }

        .wrapper {
            display: block;
            padding: 12px;
            border-radius: 15px;
            display: grid;
            padding-top: 0px;
        }
    }
</style>