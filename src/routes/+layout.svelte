

<nav>
    <a href="/">About Me</a>
    <a href="/projects">My Projects</a>
    <a href="/contacts">Get in contact</a>
</nav>


<slot>
</slot>

<style>
    
nav {
        width: max-content;
        position: fixed;
        position: absolute;
        top: 60px;
        left: 50%;
        transform: translateX(-50%);
        padding: 20px 0;
        border-radius: 5px;
        z-index: 999;
    }

    a {
        /* color: rgba(0, 0, 0, 0.712); */
        /* background: #151515; */
        /* text-transform: uppercase; */
        /* font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif; */
        /* font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif; */
        /* font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; */
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        text-decoration: none;
        color: #bbb;
        font-weight: 700;
        font-size: 26px;
        padding: 20px 40px;
        border-radius: 5px;
        transition: 0.33s;
        background: #181818;
        box-shadow:  2.5px 2.5px 10px 0px #11111155;

    }

    a:hover {
        /* background: rgb(122, 210, 14); */
        /* background: #980000; */
        /* background: #6a040f; */
        background: #fdbe39;
        color: #222;
        padding: 20px 42px;
    }

    nav > a:nth-child(2) {
        margin: 0 15px;
        /* margin: 0; */
    }

</style>