<script>
    import IMG1 from './img/4.jpg';
    import IMG2 from './img/1.jpg';
    import IMG3 from './img/2.jpg';
    import IMG4 from './img/8.jpg';
    import IMG5 from './img/storyvid.mp4';
    import color from './Story/colorChange.svelte'
    import Posts from './Posts.svelte';
  import ColorChange from './Story/colorChange.svelte';
    
  
    function close(){
        let click = document.querySelector(".storiesPlay");
        // @ts-ignore
        click.style.visibility = "collapse";
        
    }
    
    document.addEventListener("DOMContentLoaded",()=>{
    let imgsrcArray = document.querySelectorAll(".stories");
    console.log(imgsrcArray.length)

    imgsrcArray.forEach(item =>{
        item.addEventListener("click",(event)=>{
            
            // @ts-ignore
        document.querySelector(".imgsrc").src = event.target.getAttribute("data-imgsrc");
        
        let click = document.querySelector(".storiesPlay");
        // @ts-ignore
        click.style.visibility = "visible" ;
        })
    })
})
    function createStory(){
        let creates = document.querySelector('.createCard');
        // @ts-ignore
        creates.style.visibility="visible";
    }
    let cmessage;
    function cclose(){
        let creates = document.querySelector('.createCard');
        // @ts-ignore
        creates.style.visibility="collapse";
    }
</script>

<div class="cont">
<div class="storybox">

    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="create" on:click={createStory}>
        +
    </div>
<div class="child">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="stories" data-imgsrc={IMG1}></div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="stories" data-imgsrc={IMG2}></div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="stories" data-imgsrc={IMG3}></div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="stories" data-imgsrc={IMG4}></div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="stories" data-imgsrc={IMG1}></div>
</div>
</div>
</div>
<div class="cont">
    <div class="storiesPlay">
        <div class="card">
            <img src="" class="imgsrc" alt="">
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="close" on:click={close}>
            x
        </div>
    </div>
</div>
<div class="cont">
    <div class="createCard">
        <div class="scard">
            <div class="choose">
                <div class="text">Text</div>
                <div class="img">Image</div>
            </div>
            <div class="inputs">
                <div class="colors">
                    <ColorChange/>
                </div>
            </div>
            <div class="preview">
                <div class="titleBox">
                    <div class="titleprofile">
                        <div class="titleprofilepicture"></div>
                        <div class="titleprofilename">Kyd</div>
                    </div>
                    <div class="content" contenteditable="true" bind:innerHTML={cmessage}>Ide írj</div>
                    
                </div>
            </div>
            <button class="cret" >Create</button>
            <!-- svelte-ignore a11y-click-events-have-key-events -->
            <div class="closec" on:click={cclose}>Close</div>
        </div>
    </div>
</div>

<style>
    .closec{
        margin-top: 20px;
        color: black;
        
    }
    .closec:hover{
        cursor: pointer;
        
    }

.storybox{
    margin-top: 20px;
    width: 47%;
    min-width: 400px;
    height: 70px;
    display: flex;
    align-items: center;
    margin-left:410px;
    position: fixed;
    padding: 20px 20px;
    background-color: rgba(22, 22, 22, 0.473);
    backdrop-filter: blur( 10.5px );
    -webkit-backdrop-filter: blur(10.5px);
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.15);
    border-radius: 10px;
    overflow-x: scroll;
    overflow-y: hidden;
    z-index: 99;
}
.storybox::-webkit-scrollbar{
    height: 5px;
    border-radius: 20px;
}
.storybox::-webkit-scrollbar-track {
  background-color: rgba(169, 169, 169, 0.26);
  border-radius: 20px;
}
.storybox::-webkit-scrollbar-thumb {
  background-color: rgba(128, 128, 128, 0.5);
  border-radius: 20px;
  max-height: 200px;
}

.create{
    min-width: 50px;
    height: 50px;
    border-radius: 10px;
    border: 2px solid #0CCE6B;
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 20px;
    font-family: monospace;
    margin-right: 30px;

    transition: all .5s;
}
.create:hover{
    transform: rotateZ(180deg);
    cursor: pointer;
   
}
.stories{
    width: 50px;
    height: 50px;
    border-radius: 10px;
   
    margin-right: 20px;
    transition: all .5s;
    border: 2px solid #EF2D56;
    
}

.stories:hover{
    transform: scale(1.2);
    cursor: pointer;
}
.child{
    display: flex;
    
}
.stories:nth-child(1){
    background-image: url(../assets/imgs/asd19.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.stories:nth-child(2){
    background-image: url(../assets/imgs/asd2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.stories:nth-child(3){
    background-image: url(../assets/imgs/asd6.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.stories:nth-child(4){
    background-image: url(../assets/imgs/asd9.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.stories:nth-child(5){
    background-image: url(../assets/imgs/asd7.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.storiesPlay{
    position: fixed;
    width: 100%;
    min-height: 100vh;
    max-height: 100vh;
    background-color: rgba(2, 2, 2, 0.918);
    z-index: 99;
    display: flex;
    justify-content: center;
    align-items: center;
    visibility: collapse;
    backdrop-filter: blur( 10.5px );
    -webkit-backdrop-filter: blur( 10.5px );
    
    padding: 20px 20px;

}
.card{
    min-width: 500px;
    height: 100vh;
    max-width: 700px;
    
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
    border-radius: 10px;
}
.close{
    position: absolute;
    top: 0;
    right: 0;
    font-size: 30px;
    padding: 40px 40px 0 0;
}
.close:hover{
    cursor: pointer;
    
}
img{
    width: 100%;
    height: 100%;
    border-radius: 10px;
}

.createCard{
    position: fixed;
    width: 100%;
    min-height: 50vh;
    max-height: 100vh;
    background-color: rgba(2, 2, 2, 0.918);
    z-index: 99;
    display: flex;
    justify-content: center;
    align-items: center;
    visibility: collapse;
    backdrop-filter: blur( 10.5px );
    -webkit-backdrop-filter: blur( 10.5px );
    padding: 20px 20px 20px 20px; 
}
.scard{
    min-width: 500px;
    height: 100vh;
    max-width: 700px;
    border-radius: 10px;
    background-color: white;
    padding: 20px 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.cret{
    background-color: black;
    color: white;
    outline: none;
    border: none;
    border-radius: 10px;
    width: 200px;
    height: 35px;
}
.cret:hover{
    cursor: pointer;
}
.choose{
    display: flex;
    height: 50px;
}
.text{
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    margin-right: 20px;
    border-bottom: 1px solid black;
}
.text:hover{
    opacity: 0.6;
}
.img{
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    margin-left: 20px;
}
.img:hover{
    opacity: 0.6;
}
.inputs{
    width: 100%;
    height: 200px;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 20px 20px;
}
input{
    width: 50%;
    background-color: transparent;
    outline: none;
    height: 40px;
    border: 2px solid black;
    border-radius: 10px;
    padding: 10px;
    color: black;
}
.colors{
    margin-top: 50px;
}

.preview{
    width: 100%;
    min-height: 200px;
    padding: 20px 20px;
    display: flex;
    justify-content: center;
}
.titleBox{
    width: 95%;
    
    padding: 20px 20px;
    margin-top:30px;
    border-radius: 10px;
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.15);
}
.titleprofile{
    max-width: 300px;
    min-width: 200px;
    height: 60px;
    background-color: rgba(128, 128, 128, 0.075);
    padding: 10px 10px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    transition: all .5s;
}
.titleprofile:hover{
    transform: scale(1.02);
    cursor: pointer;
}

.titleprofilepicture{
    width: 50px;
    height: 50px;
    border-radius: 5px;
    background-image: url("../assets/imgs/asd2.jpg");
    background-repeat: no-repeat;
    background-size: cover;
}

.titleprofilename{
    margin-left: 15px;
}

.content{
    width: 100%;
    height: 100px;
    border-radius: 10px;
    margin-top: 5px;
    font-size: 15px;
    padding: 20px 20px;
}



.titleBox:nth-child(1){
    background-color: #0c97ce;
}

.titleBox:nth-child(1) .content{
    box-shadow: inset 10px 10px 50px #0a80af,
            inset -10px -10px 50px #0eaeed;
}
@media (max-width:1800px){
    .storybox{
        margin-left: 0;
        
    }
    .cont{
        display: flex;
        justify-content: center;
    }
}
@media (max-width:420px){
    .storiesPlay{
        padding: 10px 10px;
    }
}
</style>