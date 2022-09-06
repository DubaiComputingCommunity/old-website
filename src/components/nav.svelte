<script>
      import { browser } from '$app/environment';
    let is_Nav_M_Ctn_Open = false;

    const HandleBurgerClick = () => {
        if(browser)
        {
            const Nav_M_Ctn = document.getElementById("Nav_M_Ctn");
            if(is_Nav_M_Ctn_Open)
            {
                is_Nav_M_Ctn_Open = false;
                Nav_M_Ctn?.style.setProperty("display", "none")
            }else{
                is_Nav_M_Ctn_Open = true;
                Nav_M_Ctn?.style.setProperty("display", "flex")
            }            
        }

    }
</script>

<div class="nav">
    <div class="logo">
        <img src="/logo.png" alt="logo" class="logo-img"/>
        <h1>DCC</h1>
    </div>

    <div class="ALink_M">
        <img src="/menu-outlined.svg" alt="Menu_icon" class="Icon_menu" on:click={() => HandleBurgerClick()}/>
        <div class="Pop_Ctn" id="Nav_M_Ctn">
            <a href="/">Home</a>
            <a href="/">Social</a>
            <a href="/">Event</a>
            <a href="/">Team</a>
            <a href="/">Contact</a>
        </div>
    </div>

    <div class="Alinks">
        <a href="/">Home</a>
        <a href="/">Social</a>
        <a href="/">Event</a>
        <a href="/">Team</a>
        <a href="/">Contact</a>
    </div>
</div>

<style>

    .ALink_M{
        margin-right: 5%;
        display: none;        
    }

    .Icon_menu{
        width: 35px;
        height: 35px;
        cursor: pointer;
    }


    .Pop_Ctn{
        position: absolute;
        width: 45vw;
        height: 65vh;
        display: flex;
        flex-direction: column;
        background-color: white;
        align-items: center;
        bottom: 25%;
        left: 55%;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        border-top-left-radius: 10px;
        z-index: 12;
        transition: all 1s ease-in;
        display: none;
    }

    .Pop_Ctn a{
        padding-bottom: 10%;
        padding-top:10%;
        font-size: x-large;
        text-decoration: none;
        font-family: var(--font_M);
        color: black;
    }

    .Pop_Ctn a:hover{
        border: none;
        outline: none;
        color: grey;
        transition: all 0.5s ease-in-out;
    }

    .Alinks{
        display: flex;
        flex-direction: row;
        margin-right: 18%;
    }

    .Alinks a{
        margin-left: 15%;
        font-size: x-large;
        text-decoration: none;
        color: white;
        font-family: var(--font_M);
        font-weight: 400;
    }


    .Alinks a:hover {
        border: none;
        outline: none;
        color: black;
        transition: all 0.5s ease-in-out;
    }

    .logo-img{
        width: 70px;
        height: 70px;
    }

    .logo{
        margin-left: 2%;
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .logo h1{
        margin-left: 10px;
        font-family: var(--font_M);
        color: rgb(88, 88, 88);
    }

    .nav{
        display: flex;
        justify-content: space-between;
        height: 80px;
        align-items: center;
        width: 100vw;
        background: transparent;
        box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
    }


    @media only screen and (max-width: 600px) {
        .Alinks{
            display: none;
        }
        .ALink_M{
            display: flex;
        }

        .nav{
            background-color: white;
        }
    }
</style>