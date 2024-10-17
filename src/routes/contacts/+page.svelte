<script>
    import cv_url from '$lib/cv.pdf'
</script>

<section>
   <div id="contacts">

        <div>
            <h3>Email:</h3>
            <a href="mailto: flama2204@gmail.com">flama2204@gmail.com</a>
        </div>

        <div>
            <h3>LinkedIn:</h3>
            <a href="https://www.linkedin.com/in/flavio-manna-a823a52a3/">Flavio Manna</a>
        </div>

        <div>
            <h3>Github:</h3>
            <a href="https://github.com/Hypnos999/">Hypnos999</a>
        </div>
   </div>

   <div id="info">
        <div>
            <h3>Curriculum</h3>
            <a href={cv_url}>click on the text to see my CV</a>
        </div>
   </div>

   <h4 id="disclaimer">Click on the text to be redirected!</h4>
</section>


<style>

    #contacts {
        position: relative;
        left: 50%;
        transform: translateX(-50%);
        width: fit-content;
        height: 95vh;
        margin-top: 0vh;
        display: flex;
        align-items: center;
    }

    #contacts > div:nth-child(2) {
        margin: 0 10vw;
        width: min-content;
    }

    h3 {
        color: #ffda3d;
        font-size: 70px;
    }

    a {
        color: #ccc;
        font-size: 34px;
        text-underline-offset: 12.5px;
        text-decoration: underline;
        text-decoration-color: #151515;
        transition: 0.5s;
        position: relative;
        left: 2px;
    }
    
    a:hover {
        text-decoration-color: #fdc43f;
    }

    #info {
        display: none;
        height: 0;
        width: 0;
    }

    #disclaimer {
        position: absolute;
        bottom: 7.5vh;
        font-size: 30px;
        font-weight: 600 !important;
        color: #fdc43f;
        left: 50%;
        transform: translateX(-50%);
    }

    @media only screen and (max-width: 1500px) {
        h3 {
            font-size: 50px !important;
        }

        a {
            font-size: 24px !important;
        }

        #disclaimer {
            font-size: 20px !important;
        }
    }

    @media only screen and (max-width: 1100px) {
        h3 {
            font-size: 40px !important;
        }

        a {
            font-size: 18px !important;
        }

        #disclaimer {
            font-size: 14px !important;
        }
    }
</style>