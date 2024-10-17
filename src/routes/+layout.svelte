
<script>
    import { page } from '$app/stores';
    import { afterUpdate } from 'svelte';
    // Set the current URL
    let current_url = $page.url.pathname.split('/').filter(Boolean).pop() || '/';

    // Set it as soon as pages update
    afterUpdate(() => {
        current_url = $page.url.pathname.split('/').filter(Boolean).pop() || '/';
    });
    
    let currentPath = current_url
    
    let about_me_class = ''
    let projects_class = ''
    let contacts_class = ''
    
    if (currentPath == '/') {
        about_me_class = 'active'
    } else if (currentPath == 'projects') {
        projects_class = 'active'
    } else if (currentPath == 'contacts') {
        contacts_class = 'active'
    }


</script>

<nav>
    <!-- <a href="/">{currentPath}, {about_me_class}, {projects_class}, {contacts_class}</a> -->
    <a href="/" class={about_me_class} on:click={() => {about_me_class='active'; projects_class=''; contacts_class=''}}>About Me</a>
    <a href="/projects" class={projects_class} on:click={() => {projects_class='active'; about_me_class=''; contacts_class=''}}>My Projects</a>
    <a href="/contacts" class={contacts_class} on:click={() => {contacts_class='active'; projects_class=''; about_me_class=''}}>Get in contact</a>
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
        font-weight: 700 !important;
        font-size: 26px;
        padding: 20px 40px;
        border-radius: 5px;
        transition: 0.33s;
        background: #181818;
        box-shadow:  2.5px 2.5px 10px 0px #11111155;

    }

    a:hover, .active {
        /* background: rgb(122, 210, 14); */
        /* background: #980000; */
        /* background: #6a040f; */
        background: #fdbe39;
        color: #222;
        padding: 20px 42px;
        font-weight: 700 !important;
    }

    nav > a:nth-child(2) {
        margin: 0 15px;
        /* margin: 0; */
    }


    @media only screen and (max-width: 1500px) {
        nav {
            top: 30px !important;
        }

        a {
            /* background-color: green !important; */
            padding: 10px 20px !important;
            font-size: 18px !important;
        }

        a:hover, .active {
            padding: 10px 22px !important;
        }

        nav > a:nth-child(2) {
            margin: 0 10px !important;
        }
    }

    

    @media only screen and (max-width: 600px) {
        a {
            padding: 10px !important;
            font-size: 14px !important;
        }

        a:hover, .active {
            padding: 10px 12px !important;
        }

        nav {
            top: 15px !important;
        }
    }

  
</style>