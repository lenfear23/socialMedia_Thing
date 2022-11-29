<script>

document.addEventListener('DOMContentLoaded',()=>{
    let kepek = document.querySelectorAll(".imgBox");
    let filterimg ;
    // @ts-ignore
    document.querySelector(".imgBox").addEventListener('mousemove',()=>{
        filterimg = document.querySelector(".imgBox");
        
    })
})

</script>

<div class="container">
<div class="allcont">
<div class="profileBox">
    <div class="profileData">
        <div class="profileImg"></div>
        <div class="profileName">Lenfear23</div>
        <div class="profileTag">@lenfear23</div>
    </div>
    <div class="profileInfo">
        <div class="followers">
            <h3>Followers</h3>
            <span>35k</span>
        </div>
        <div class="likes">
            <h3>Likes</h3>
            <span>540k</span>
        </div>
    </div>
    <div class="imgs">
      
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
        <div class="imgBox">
        </div>
  
    </div>
    
</div>

</div>

</div>


<style>
.container{
    
    width: 600px;
    min-height: 100vh;
    background-color: transparent;
    float: right;
    display: flex;
    justify-content: center;
    align-items: center;
    
    transition: all .5s;
}

.allcont{
    background-color: white;
    position: fixed;
    border-radius: 20px;
}

.profileBox{
    width: 550px;
    height: 900px;
    
    border-radius: 20px;
    padding: 20px 20px;
}
.profileData{
    width: 100%;
    height: 60px;
    background-color: #EF2D56;
    border-radius: 10px;
    transition: all .3s;
    display: flex;
    align-items: center;
    box-shadow: 20px 20px 20px rgba(0,0,0,0.15);
}
.profileData:hover{
    transform: scale(1.03);
    cursor: pointer;
    box-shadow: 20px 20px 20px rgba(0,0,0,0.25);
}
.profileImg{
    width: 50px;
    height: 50px;
    border-radius: 50%;
    margin-left: 20px;
    background-image: url(../assets/imgs/asd.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.profileName{
    color: white;
    margin-left: 20px;
}
.profileTag{
    color: gray;
    font-size: 13px;
    margin-left: 180px;
}
.profileInfo{
    width: 100%;
    height: 100px;
    background-color: white;
    border-radius: 10px;
    margin-top: 10px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    color: black;
    transition: all .3s;
    box-shadow: 5px 5px 5px 5px rgba(0,0,0,0.15);
}
.followers{
    width: 200px;
    height: 70px;
    background-color: #DCED31;
    border-radius: 10px;
    box-shadow: 20px 20px 20px rgba(0,0,0,0.15);
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    transition: all .5s;
}
.followers:hover{
    cursor: pointer;
    transform: scale(1.05);
    box-shadow: 20px 20px 20px rgba(0,0,0,0.25);
}
.likes{
    width: 200px;
    height: 70px;
    background-color: #0CCE6B;
    border-radius: 10px;
    box-shadow: 20px 20px 20px rgba(0,0,0,0.15);
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    transition: all .5s;
}

.likes:hover{
    cursor: pointer;
    transform: scale(1.05);
    box-shadow: 20px 20px 20px rgba(0,0,0,0.25);
}

.imgs{
    margin-top: 10px;
    width: 100%;
    border-radius: 10px;
    max-height: 680px;
    padding: 35px 20px 30px 20px;
    display: flex;
    justify-content: space-around;
    flex-wrap:wrap;
    overflow-y: scroll;
    overflow-x: hidden;
    box-shadow: 20px 20px 20px 20px rgba(0,0,0,0.25);
}
.imgs::-webkit-scrollbar{
    width: 10px;
    border-radius: 20px;
}
.imgs::-webkit-scrollbar-track {
  background-color: rgba(169, 169, 169, 0.26);
  border-radius: 20px;
}
.imgs::-webkit-scrollbar-thumb {
  background-color: rgba(128, 128, 128, 0.5);
  border-radius: 20px;
  max-height: 200px;
}
.imgBox{
    box-shadow: 20px 20px 20px rgba(0,0,0,0.15);
    width: 150px;
    height: 150px;
    border-radius: 5px;
    transition: all .5s;
    border: 2px solid #363537;
    background-repeat: no-repeat;
    background-size: cover;
    margin-top: 5px;
    
}
.imgBox:nth-child(1){
    background-image: url(../assets/imgs/asd.jpg);
}
.imgBox:nth-child(2){
    background-image: url(../assets/imgs/asd2.jpg);
}
.imgBox:nth-child(3){
    background-image: url(../assets/imgs/asd1.jpg);
}
.imgBox:nth-child(4){
    background-image: url(../assets/imgs/asd3.jpg);
}
.imgBox:nth-child(5){
    background-image: url(../assets/imgs/asd4.jpg);
}
.imgBox:nth-child(6){
    background-image: url(../assets/imgs/asd5.jpg);
}
.imgBox:nth-child(7){
    background-image: url(../assets/imgs/asd6.jpg);
}
.imgBox:nth-child(8){
    background-image: url(../assets/imgs/asd7.jpg);
}
.imgBox:nth-child(9){
    background-image: url(../assets/imgs/asd8.jpg);
}
.imgBox:nth-child(10){
    background-image: url(../assets/imgs/asd9.jpg);
}
.imgBox:nth-child(11){
    background-image: url(../assets/imgs/asd10.jpg);
}
.imgBox:nth-child(12){
    background-image: url(../assets/imgs/asd11.jpg);
}
.imgBox:hover{
    transform: scale(1.4);
    cursor: pointer;
    box-shadow: 20px 20px 20px rgba(0,0,0,0.25);
    z-index: 99;
}

.imgBox:hover ~ .imgBox{
    filter: blur(3px);
}

@media (max-width:1500px){
    .container{
        display: none;
    }
}

</style>