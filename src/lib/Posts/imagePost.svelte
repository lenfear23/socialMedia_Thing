<script>
    export let profilename;
    export let likes;
    export let imgsrc;

    console.log(imgsrc)
    
    
    

    function likeAdding(){
        likes++;
    }


</script>

<div class="postbox" on:dblclick={likeAdding}>
    
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
    background: rgb(251,8,0);
    background: linear-gradient(142deg, rgba(251,8,0,1) 0%, rgba(255,111,0,0.989233193277311) 100%);
    background-position: center;
}

.profilepicture{
    min-width: 70px;
    height: 70px;
    border-radius: 10px;
    border: 2px solid #0CCE6B;
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.15);
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
    padding: 20px 20px;
    border-radius: 10px;
    background-color: #1f1f1f94;
    transition: all .5s;
    width: 300px;
}
.postinfo:hover{
    cursor: pointer;
    background-color: #1f1f1f94;
    transform: scale(1.05);
}

.profilename{
    margin-left: 20px;
    color: #fdfdfd;
    font-size: 20px;
}

.postlikes{
    width: 120px;
    height: 80px;
    margin-top: 450px;
    margin-left: 620px;
    background-color: #1f1f1f94;
    border-radius: 10px;
    transition: all .5s;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #0CCE6B;
}
.postlikes:hover{
    cursor: pointer;
    background-color: #1f1f1f94;
    transform: scale(1.1);
}
@media (max-width:600px){
    .postlikes{
        transform: scale(0.8);
        margin-top: 530px;
        margin-left: 220px;
    }
}
@media (max-width:420px){
    .postlikes{
        transform: scale(0.7);
        height: 70px;
        margin-top: 530px;
        margin-left: 220px;
    }
    .postlikes:hover{
        transform: scale(0.75);
    }
    .postinfo{
        max-width: 300px;
        transform: scale(0.6);
        padding: 10px 10px;
        margin-left: -40px;
    }
    .postinfo:hover{
        transform: scale(0.65);
    }
    .postbox{
        padding: 10px 0;
    }
   
}

</style>