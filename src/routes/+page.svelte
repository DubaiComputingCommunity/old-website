<script>
import Buttons from "../components/buttons.svelte";
import Nav from "../components/nav.svelte";

</script>

<div class="body">
  <Nav/>
  <div class="side_view">
    <h1>Dubai <br/>Computing Community</h1>
    <span></span>
    <p>
        As Computer Science exapnds across the UAE, we aim to foster a community where<br/>
        programmers can connect, collaborate, and innovate regardless of age and skillset.
    </p>
    

    <span class="Mobile_p">
        As Computer Science exapnds across the UAE, we aim to foster a community where<br/>
        programmers can connect, collaborate, and innovate regardless of age and skillset.
    </span>
    <div class="btn_ctn">
        <span>
            <Buttons title="Join our Community"/>
        </span>
        <span>
            <Buttons title="See more about us"/>
        </span>
    </div>
  </div>
  <div>
      <img src="/blob.svg" alt="blobl" class="blob">
      <img src="/discord.svg" alt="discord" class="dsc"/>
  </div>
</div>


<style>

    .body{
        height: 100vh;
    }

    .Mobile_p{
        display: none;
    }

    .btn_ctn{
        margin-top: 5%;
        display: flex;
        flex-direction: row;
    }

    .btn_ctn span{
        margin-right: 5%;
    }

    .side_view{
        margin-top: 5%;
        margin-left: 5%;
    }


    .side_view h1{
        font-size: 4rem;
        font-family: var(--font_M);
        font-weight:bolder;
        margin-bottom: 1%;
    }

    .side_view p{
        font-size: 20px;
        color: grey;
        font-family: var(--font_M);
    }

 .blob{
    position: absolute;
    right: -50%;
    top: -100%;
    width: 100rem;
    z-index: -1;
 }

 .dsc{
    width: 600px;
    height: 400px;
    position: absolute;
    right: 5%;
    top:15%;
 }

 
 @media only screen and (max-width: 600px) {
    .side_view p, .dsc{
        display: none;
    }

    .blob{
        right: -50%;
        left: -100%;
        width: 45rem;
        height: 120rem;
    }


    .side_view h1{
        margin-top: 10%;
        color: #25E5A7;
        font-size: 2.5rem;
        font-style:italic;
        font-weight: bolder;
        line-height: 6rem;
        display: inline-block;
        max-width: min-content;
    }

    .side_view h1 br{
        display: none;
    }


    .Mobile_p{
        display: flex;
        position: absolute;
        top: 85vh;
        text-align: left;
        line-height: 5vh;
        font-family: var(--font_M);
        color: rgb(43, 43, 43);
    }

    .btn_ctn{
        position: absolute;
        top: 105vh;
        flex-direction: column;
    }


 }

</style>