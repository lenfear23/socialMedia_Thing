<script>
   
   import App from "../App.svelte";
import Test from "../assets/Datas/posts.json";
    import TextPost from "../lib/Posts/textPost.svelte";
    import ImagePost from "./Posts/imagePost.svelte";
   import img1 from "./img/1.jpg";


    
</script>
<div class="cont">
    <div class="postsContainer">

        <TextPost profilename={"Lenfear23"} content={"Lorem ipsum dolor"} likes={"1000"}/>
        <ImagePost profilename={"Lenfear23"} likes={"106"} imgsrc={img1}/>
        <ImagePost profilename={"Lenfear23"} likes={"5670"} imgsrc={img1}/>
        <TextPost profilename={"Lenfear23"} content={"Lorem ipsum dolor"} likes={"0"}/>
        <TextPost profilename={"Lenfear23"} content={"Lorem ipsum dolor"} likes={"9999"}/>

</div>
</div>

<style>
.postsContainer{
    position:absolute;
    margin-top: 100px;
    width: 47%;
    min-width: 400px;
    margin-left:410px;
    background-color: transparent;
    padding: 20px 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
   
}
.postsContainer::-webkit-scrollbar{
    width: 5px;
    border-radius: 20px;
}
.postsContainer::-webkit-scrollbar-track {
  background-color: rgba(169, 169, 169, 0.26);
  border-radius: 20px;
}
.postsContainer::-webkit-scrollbar-thumb {
  background-color: rgba(128, 128, 128, 0.5);
  border-radius: 20px;
  max-height: 200px;
}







@media (max-width:1800px){
    .postsContainer{
        margin-left: 0;
        justify-content: center;
    }
   
    .cont{
        display: flex;
        justify-content: center;
    }
}
@media (max-width:1400px){
    .postsContainer{
        margin-left: 0;
        justify-content: center;
    }
}


@media(max-height:900px){
    .postsContainer{
        
        margin-top: 80px;
       
    } 
}
</style>