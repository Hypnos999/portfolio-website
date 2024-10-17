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
            <div>
                <h1>Hello, i'm </h1>
                <h1 class="dark-text">Flavio Manna</h1>
            </div>
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
            <!-- <h3>Artificial Intelligence & Machine Learning Specialist course at ITS Angelo Rizzoli</h3> -->
            <h3>Artificial Intelligence & Machine Learning Specialist course</h3>
            <p>The training course is provided by the ITS Angelo Rizzoli foundation, one of the most renowned institutes in my region. prepares experienced Machine Learning Technicians with in-depth knowledge of leading artificial intelligence-oriented software and programming languages. <br><br> 
                The training is scheduled to last 2 years. It is organized into 1,000 hours of training each year, with a total of 2,000 hours divided as follows: 1,160 hours of classroom and laboratory training; 840 hours of internship/internship.</p>
            <img id="its-logo" src={its_logo} alt="A logo of the techinal istitute where a studied">
        </div>
        
        <div id="background">
            <h2>Background</h2>
            <h3>Why i started programming?</h3>
            <p>
                Before taking the deep learning course, I graduated from a high school in economics, but I soon learned that working in this field was uninspiring for me and I would soon find myself in a sterile work environment with no ambition.
                <br>
                <br>
                Instead, in the world of computer science I found an alternative that would serve as fuel for my desire to know and learn new knowledge, but above all, the big difference lies in the possibility of being able to apply one's work in everyday life. 
                <br>
                <br>
                That's why I started self-taught programming, always setting myself new challenges to take on in order to gain more experience. In fact, I would very much like one day to be able to work in the social field to help people who have the most difficulty interacting with society or who for other reasons related to it face excessive difficulties in their lives
            </p>
        </div>

        <div id="bg"></div>
    </div>
</section>


<style>
    #first-pannel-text {
        width: 35vw;
        /* background: green; */
        position: absolute;
        top: 25vh;
        left: 55vw;

    }
    
    .text {
        position: relative;
        font-size: 24px;
        line-height: 1.75em;
        color: #eee;
        left: 3px;
        width: 100;
    }

    #first-pannel{
        width: 100vw;
        height: 100vh;
        position: relative;
    }

    #first-pannel-text div {
        display: inline-block;
    }

    #foto {
        height: 75vh;
        position: absolute;
        bottom: 0;
        /* opacity: 0.8; */
        left: 7.5vw;
        overflow: hidden;
        z-index: 0;
    }
    
    #foto img {
        height: 85vh;
        width: auto;
        filter: brightness(65%);
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
        /* color: #6a040f; */
        color: #fdc43f;
    }
    
    #first-pannel-text h1.dark-text {
        font-size: 80px;
        margin-left: 0 !important;
    }

    .dark-text {
        /* color: #980000 !important; */
        /* color: #fecf3e !important; */
        color: #ffda3d !important;
        margin-left: 10px;
    }

    .arrow-down {
        position: absolute;
        left: 50%;
        top: 7vh !important;
        transform: translateX(-50%) rotate(180deg);
        /* transform: rotate(180deg) !important; */
        cursor: pointer;
    }

    .arrow {
        position: absolute;
        bottom: 7vh;
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
        /* height: 85vh;
        padding-top: 15vh; */
        height: 100vh;
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

    #its-logo {
        width: 25vw;
        height: auto;
        position: relative;
        top: 6.5vh;
        left: 45%;
        transform: translateX(-50%);
        opacity: 0.9;
        /* height: 10vw; */
    }

    #studies, #background {
        height: fit-content;
        position: relative;
        top: 50%;
        transform: translateY(-50%);
        margin: 0 5vw 0 5vw;
        width: 40vw;
    }

    #second-pannel p {
        color: #111;
        font-size: 26px;
        margin-top: 20px;
        font-weight: 500;
    }

    #second-pannel h3 {
        margin-top: 10px;
        color: #222;
        font-size: 44px;
    }

    #bg {
        width: 50vw;
        height: 200vh;
        position: absolute;
        top: -25%;
        left: 55%;
        transform: rotate(45deg) !important;
        z-index: -1;
        /* background: green; */
        background: #fdbe39;
    }

    #background {
        text-align: right;
    }

    @media only screen and (max-width: 1700px) {
        .text {
            font-size: 20px !important;
        }

        #first-pannel-text {
            top: 55vh !important;
            transform: translateY(-50%);
        }
    }

    @media only screen and (max-width: 1500px) {
        #foto {
            height: 65vh;
            max-height: 500px;
        }
        
        #foto img, #contour {
            height: 75vh !important;
            max-height: 590px;
        }

        #first-pannel-text {
            left: 57.5vw !important;
        }

        h1 {
            font-size: 34px !important;
        }

        #first-pannel-text h1.dark-text {
            font-size: 60px !important;
        }

        .text {
            font-size: 16px !important;
            line-height: 1.4em !important;
            left: 3px;
            top: 5px;
        }

        .arrow {
            bottom: 10vh !important;
        }

        .arrow-down {
            bottom: auto;
            top: 10vh !important;
        }

        h2 {
            font-size: 40px !important;
        }

        #second-pannel {
            padding-top: 10vh !important;
            height: 90vh !important;
        }

        h3 {
            font-size: 24px !important;
        }

        #second-pannel p {
            font-size: 15px;
        }
    }


    @media only screen and (max-width: 1350px) {
        #foto {
            height: 65vh;
        }

        #foto img, #contour {
            height: 75vh !important;
        }
    }

    @media only screen and (max-width: 1100px) {
        #foto {
            left: 50%;
            transform: translateX(-50%);
        }

        #contour {
            left: 52.5%;
            bottom: -7vh;
            transform: translateX(-50%);
        }

        .arrow, .arrow-down {
            display: none !important;
        }

        #first-pannel-text {
            left: 50vw !important;
            transform: translateX(-50%);
            top: 17.5vh !important;
            width: 75vw;
        }

        #second-pannel {
            /* width: 100svw; */
            display: block;
        }

        #second-pannel > * {
            width: 80vw;
            margin: 0 10vw;
            top: 0;
            transform: translateY(0);
        }

        #second-pannel p {
            width: 90%;
        }

        #its-logo {
            position: absolute !important;
            top: -7.5vh !important;
            right: 0 !important;
            left: auto !important;
            transform: translateX(0) !important;
        }

        #background {
            margin-top: 3vh;
        }

        #background p {
            margin-left: 10%;
        }

        #second-pannel h2 {
            font-size: 34px !important;
        }

        #second-pannel h3 {
            margin-top: 0;
        }

        #bg {
            top: -25% !important;
        }

        @media only screen and (max-height: 1000px) {
            #foto {
                height: 39vh !important;
            }

             
            #foto img, #contour {
                height: 45vh !important;
                max-height: 590px;
            }
        }

        @media only screen and (max-height: 750px) {
            #foto {
                height: 29vh !important;
            }

             
            #foto img, #contour {
                height: 35vh !important;
                max-height: 590px;
            }
        }
    }

    @media only screen and (max-width: 700px) {
        #first-pannel-text div {
            display: flex;
            height: max-content;
            align-items: baseline;
        }

        body #first-pannel > #first-pannel-text h1:not(.dark-text) {
            font-size: 20px !important;
        }

        body #first-pannel > #first-pannel-text h1.dark-text {
            font-size: 30px !important;
            margin-left: 7.5px !important;
        }
        
        
        body #first-pannel > #first-pannel-text .text {
            font-size: 18px !important;
        }
    }

    @media only screen and (max-width: 600px) {
        body #first-pannel > #first-pannel-text .text {
            font-size: 14px !important;
            text-align: center;
        }

        body #first-pannel > #first-pannel-text div {
            width: fit-content !important;
            position: relative;
            left: 50% !important;
            transform: translateX(-50%);
        }

        body #first-pannel > #first-pannel-text h1:not(.dark-text) {
            font-size: 16px !important;
        }

        body #first-pannel > #first-pannel-text h1.dark-text {
            font-size: 26px !important;
            margin-left: 7.5px !important;
        }

        #second-pannel h2 {
            font-size: 24px !important;
        }

        #second-pannel {
            height: 97.5vh !important;
            height: 200vh !important;
            height: fit-content !important;
            padding-top: 5vh !important;
            padding-bottom: 0 !important;
        }

        h3 {
            margin-top: 0 !important;
            font-size: 16px !important;
        }

        #second-pannel p {
            margin-top: 7.5px !important;
            font-size: 14px;
        }

        #its-logo {
            display: none;
        }

        #studies, #background {
            height: fit-content !important;
            margin-bottom: 5vh;
        }

        #bg {
            display: none;
        }
    }

</style>