<script>
    export let profilename;
    export let likes;
    export let imgsrc;

    function likeAdding(){
        likes++;
    }


</script>

<div class="postbox" style="{ `background-image: url(${imgsrc})!important;` }" on:dblclick={likeAdding}>
    
    <div class="postinfo">
        <div class="profilepicture"></div>
        <div class="profilename">{profilename}</div>
    </div>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="postlikes" on:click={likeAdding} >
    <div class="postlikeicon" ></div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="postliketext" >{likes}</div>
    </div>
</div>

<style>
.postbox{
    display: block;
    width: 100%;
    min-height: 700px;
    max-height: 800px;
    padding: 20px 20px;
    margin-top:30px;
    border-radius: 10px;
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.15);
    background-position: center;
    background-size:auto;
}

.profilepicture{
    min-width: 70px;
    height: 70px;
    border-radius: 10px;
    border: 2px solid #0CCE6B;
}
.profilepicture:nth-child(1){
    background-image: url(../../assets/imgs/asd19.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.postbox:nth-child(1){
    background-image: url(../../assets/imgs/asd15.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.postinfo{
    display: flex;
    align-items: center;
    padding: 10px 10px;
    border-radius: 10px;
    transition: all .5s;
    background-color: rgba(80, 80, 80, 0.479);
    padding: 10px 10px;
    backdrop-filter: blur( 5px );
    width: 300px;
}
.postinfo:hover{
    cursor: pointer;
    background-color: rgba(80, 80, 80, 0.479);
    transform: scale(1.1);
}

.profilename{
    font-size: 20px;
    margin-left: 20px;
    color: #EF2D56;
}

.postlikes{
    width: 120px;
    height: 80px;
    margin-top: 450px;
    margin-left: 620px;
    background-color: transparent;
    border-radius: 10px;
    transition: all .5s;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #0CCE6B;
}
.postlikes:hover{
    cursor: pointer;
    background-color: rgba(110, 109, 109, 0.178);
    transform: scale(1.1);
}
@media (max-width:420px){
    .postlikes{
        transform: scale(0.8);
        margin-top: 530px;
        margin-left: 220px;
    }
    .postlikes:hover{
        transform: scale(0.85);
    }
    .postinfo{
        transform: scale(0.7);
        padding: 10px 10px;
        margin-left: -30px;
    }
    .postinfo:hover{
        transform: scale(0.75);
    }
    .postbox{
        padding: 10px 0;
    }
   
}

</style>