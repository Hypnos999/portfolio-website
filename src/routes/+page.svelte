<script>
    import selfie from "$lib/file1.png"
    import its_logo from "$lib/its_logo.png"
</script>

<section>
    <div id="first-pannel">
        <div id="foto">
            <img src={selfie} alt="A photo of myself">
        </div>
    
        <nav>
            <h1>Hi, i'm <h1 class="dark-text">Flavio Manna</h1></h1>
            <p>Mi chiamo Flavio Manna e sono un
                giovane studente e praticante nel
                campo del Machine Learning.
                Ciò che mi stimola e mi appassiona di
                questo settore è la possibilità di dare
                vita alle mie idee e di applicarle alla
                vita di tutti i giorni.
                Seguire da vicino e partecipare allo
                sviluppo di questa tecnologia è per
                me fonte di stimolo e non vedo l’ora
                di entrare nel mondo del lavoro per
                apprendere nuove conoscenze e
                fornire il mio contributo in questo
                ambito.</p>
        </nav>
    
        <a href="#second-pannel">
            <div class="arrow">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </a>
    </div>

    <div id="second-pannel">
        <a href="#first-pannel">
            <div class="arrow-down" >
                <span></span>
                <span></span>
                <span></span>
            </div>
        </a>

        
        <h2>My instruction</h2>
        <h2>My background</h2>
        <img id="its-logo" src={its_logo} alt="A logo of the techinal istitute where a studied">
    </div>
</section>


<style>
    * {
        scroll-behavior: smooth;
    }

    #its-logo {
        width: 10vw;
        height: auto;
        /* height: 10vw; */
    }

    #first-pannel{
        width: 100vw;
        height: 100vh;
        position: relative;
    }

    #foto {
        height: 75vh;
        position: absolute;
        bottom: 0;
        opacity: 0.8;
        left: 10vw;
        overflow: hidden;
    }

    img {
        height: 85vh;
        opacity: 0.8;
    }

    nav {
        position: absolute;
        left: 50vw;
        top: 50vh;
        transform: translateY(-50%);
    }

    h1 {
        font-size: 50px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: #d00000;
        display: inline-block;
    }

    .dark-text {
        color: #6a040f;
    }

    h1 .dark-text {
        font-size: 70px;
    }

    p {
        font-size: 24px;
        color: #ddd;
        width: 40vw;
        margin-top: 20px;
    }

    .arrow-down {
        position: absolute;
        bottom: 4vh;
        left: 50%;
        transform: translateX(-50%) rotate(180deg);
        /* transform: rotate(180deg) !important; */
        cursor: pointer;
    }

    .arrow {
        position: absolute;
        bottom:7vh;
        left: 50%;
        transform: translateX(-50%);
        /* transform: rotate(0deg); */
        cursor: pointer;
    }

    .arrow span, .arrow-down span {
        display: block;
        width: 1.5vw;
        height: 1.5vw;
        transform: rotate(45deg);
        margin: -10px;
        animation: animate 3s infinite;
    }

    .arrow span {
        border-bottom: 5px solid #d00000;
        border-right: 5px solid #6a040f;
    }

    .arrow-down span {
        border-bottom: 5px solid #222;
        border-right: 5px solid #111;
    }

    .arrow-down span:nth-child(2), .arrow span:nth-child(2) {
        animation-delay: -0.2s;
    }

    .arrow-down span:nth-child(3), .arrow span:nth-child(3) {
        animation-delay: -0.4s;
    }

    @keyframes animate {
        0% {
            opacity: 0;
            transform: rotate(45deg) translate(-20px, -20px);
        }
        50% {
            opacity: 1;
        }
        100% {
            opacity: 0;
            transform: rotate(45deg) translate(20px, 20px);
        }
    }

    #second-pannel {
        width: 100vw;
        height: 100vh;
        background: #6a040f;
        position: relative;
    }


</style>