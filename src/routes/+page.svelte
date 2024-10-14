<script>
    import selfie from "$lib/file1.png"
    // import its_logo from "$lib/its_logo.png"
    import its_logo from "$lib/its_logo_black.png"
    // import its_corso from "$lib/its_corso.png"
    // import its_corso from "$lib/its_corso_white.png"
    import contour from "$lib/contour_yellow.png"
</script>

<section>
    <div id="first-pannel">
        <div id="foto">
            <img id="selfie" src={selfie} alt="A photo of myself">
        </div>
        <img id="contour" src={contour} alt="">
    
        <nav id="first-pannel-text">
            <h1>Hi, i'm <h1 class="dark-text">Flavio Manna</h1></h1>
            <p class="text">I am a young student in the field of Machine Learning. <br/> What motivates and excites me about is the opportunity to bring my ideas to life and apply them to everyday life. <br><br> Closely following and participating in the development of this technology is a source of stimulation for me, and I look forward to being able to apply these innovations to find new opportunities to help people which have more problems interacting with evety day life and make a truly useful contribution to society.</p>
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

        <div id="studies">
            <h2>Studies</h2>
            <!-- <img id="its-corso" src={its_corso} alt=""> -->
            <h3>Artificial Intelligence & Machine Learning Specialist course at ITS Angelo Rizzoli</h3>
            <p>The course prepares experienced Machine Learning Technicians with in-depth knowledge of leading artificial intelligence-oriented software and programming languages. <br><br> 
                The training is scheduled to last 2 years. It is organized into 1,000 hours of training each year, with a total of 2,000 hours divided as follows: 1,160 hours of classroom and laboratory training; 840 hours of internship/internship.</p>
            <img id="its-logo" src={its_logo} alt="A logo of the techinal istitute where a studied">
        </div>
        
        <div id="background">
            <h2>Background</h2>
        </div>

        <div id="bg"></div>
    </div>
</section>


<style>
    * {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        scroll-behavior: smooth;
    }

    img { 
        user-select: none;
    }

    #first-pannel-text {
        width: fit-content;
        /* background: green; */
        position: absolute;
        top: 50vh;
        left: 50vw;
        transform: translateX(10%) translateY(-200%);
    }
    
    .text {
        position: absolute;
        font-size: 24px;
        line-height: 1.75em;
        color: #eee;
        text-align: center;
        text-align: start;
        left: 3px;
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
        /* opacity: 0.8; */
        left: 10vw;
        overflow: hidden;
        z-index: 0;
    }

    #foto img {
        height: 85vh;
        width: auto;
        /* opacity: 1; */
    }
    
    #contour {
        position: absolute;
        height: 85vh;
        bottom: -10vh;
        left: 8.5vw;
        z-index: -1;
    }
    
    #selfie {
        z-index: 3;
        position: relative;
        /* top: 10px; */
    }

    #first-pannel-text h1 {
        font-size: 50px;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        display: inline-block;
        /* color: #6a040f; */
        color: #fdc43f;
    }
    
    .dark-text {
        /* color: #980000 !important; */
        /* color: #fecf3e !important; */
        color: #ffda3d !important;
    }

    #first-pannel-text h1 .dark-text {
        font-size: 80px;
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
        border-bottom: 5px solid #fdc43f;
        border-right: 5px solid #fdbe39;
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
        height: 85vh;
        padding-top: 15vh;
        /* background: #6a040f; */
        /* background: #fdbe39; */
        background: #fdb833;
        position: relative;
        display: flex;
        overflow: hidden;
        z-index: 0;
    }

    #second-pannel h2 {
        color: #000;
        /* color: #000; */
        text-transform: uppercase;
        font-size: 70px;
    }


    /* #its-corso {
        width: 10vw;
        height: auto;
    } */

    #its-logo {
        width: 20vw;
        height: auto;
        position: relative;
        top: 7.5vh;
        left: 49%;
        transform: translateX(-50%);
        opacity: 0.8;
        /* height: 10vw; */
    }

    #studies {
        width: 40vw;
        height: 100%;
        margin: 0 5vw 0 5vw;
    }

    #second-pannel p {
        color: #111;
        font-size: 24px;
        margin-top: 20px;
        font-weight: 500;
    }

    #second-pannel h3 {
        margin-top: 10px;
        color: #222;
        font-size: 34px;
    }

    #bg {
        width: 50vw;
        height: 200vh;
        position: absolute;
        top: -25%;
        left: 55%;
        transform: rotate(45deg);
        z-index: -1;
        background: green;
        background: #fdbe39;
    }


</style>