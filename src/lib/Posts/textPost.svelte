<script>

    export let profilename;
    export let content;
    export let likes;
    

    function likeAdding(){
        likes++;
        
    }

</script>

<div class="titleBox">
    <div class="titleprofile">
        <div class="titleprofilepicture"></div>
        <div class="titleprofilename">{profilename}</div>
    </div>
    <div class="content">{content}</div>
    <div class="actions">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="likes" on:click={likeAdding}>{likes}</div>
        <div class="comments">c</div>
    </div>
</div>

<style>
.titleBox{
    width: 100%;
    min-height: 200px;
    padding: 20px 20px;
    margin-top:30px;
    border-radius: 10px;
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.2);
}
.titleprofile{
    max-width: 300px;
    min-width: 200px;
    height: 60px;
    background-color: rgba(80, 80, 80, 0.479);;
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
    min-width: 50px;
    min-height: 50px;
    border-radius: 5px;
    background-image: url("../../assets/imgs/asd9.jpg");
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

.actions{
    position:absolute;
    width: 120px;
    height: 50px;
    margin-top: -160px;
    margin-left: 600px;
    display: flex;
    justify-content: space-between;
    border-radius: 10px;
}

.likes{
    font-size: 13px;
    width: 60%;
    height: 90%;
    transition: all .5s;
    border-radius: 10px;
    background-color: #3a3a3a65;
    display: flex;
    align-items: center;
    justify-content: center;
}
.likes:hover{
    cursor: pointer;
    background-color: #2525251a;
    transform: scale(0.9);
    border: none;
}

.comments{
    font-size: 13px;
    width: 30%;
    height: 90%;
    transition: all .5s;
    border-radius: 10px;
    background-color: #3a3a3a65;
    display: flex;
    align-items: center;
    justify-content: center;
}
.comments:hover{
    cursor: pointer;
    background-color: #2525251a;
    transform: scale(0.9);
    border: none;
}
.titleBox:nth-child(1){
    background-color: #0c97ce;
}

.titleBox:nth-child(1) .content{
    box-shadow: inset 10px 10px 50px #0a80af,
            inset -10px -10px 50px #0eaeed;
}
.titleBox:nth-child(4){
    background-color: #383F51;
}

.titleBox:nth-child(4) .content{
    box-shadow: inset 20px 20px 60px #2b313e,
            inset -20px -20px 60px #454d64;
}
.titleBox:nth-child(5){
    background-color: #D84A05;
}

.titleBox:nth-child(5) .content{
    box-shadow: inset 20px 20px 60px #842d03,
            inset -20px -20px 60px #ff6707;
}
@media (max-width:420px){
    
    .titleprofile{
        width: 200px;
        transform: scale(0.8);
        margin-left: -20px;
        padding: 0 5px;
    }
    .titleprofile:hover{
        transform: scale(0.85);
    }
    
   .actions{
    margin-left: 200px;
    margin-top: -160px;
   }
}
@media (min-width:860px){
    .actions{
    margin-left: 200px;
    margin-top: -160px;
   }
}
@media (min-width:1200px){
    .actions{
    margin-left:350px;
    margin-top: -160px;
   }
}
@media (min-width:1600px){
    .actions{
    margin-left: 570px;
    margin-top: -160px;
   }
}
@media (min-width:1920px){
    .actions{
    margin-left: 690px;
    margin-top: -160px;
   }
}
</style>