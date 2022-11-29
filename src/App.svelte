<script>
  import SideBar from "./lib/SideBar.svelte";
  import Profile from "./lib/Profile.svelte";
  import Story from "./lib/Story.svelte";
  import Posts from "./lib/Posts.svelte";
</script>

<main>
 <SideBar/>
 <Profile/>
 <Story/>
 <Posts />
 <div class="nav">

 </div>
</main>

<style>
  .nav{
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 60px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    background-color: rgba(22, 22, 22, 0.473);
    backdrop-filter: blur( 5.5px );

    visibility: hidden;
  }
  @media (max-width:1800px){
    .nav{
      visibility: visible;
    }
  }
</style>
