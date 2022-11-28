<script>

</script>
<div class="container">
    <div class="kozep">
<div class="icon">IMPORT</div>
</div>
<p class="active">Home</p>
<p>Search</p>
<p>Explore</p>
<p>Messages</p>
<p>Notifications</p>
<p>Create</p>

<div class="more"></div>

</div>
<style>
.container{
    position: fixed;
    top: 0;
    background-color: transparent;
    
    border-right: 2px solid gray;
    width: 400px;
    color: #DCED31;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    justify-content: center;
    padding: 0 40px;
    transition: all .5s;
}
.container:hover{
    box-shadow: 20px 20px 20px rgba(0,0,0,0.25);
    border-color: #242424;
    
}
.kozep{
    display: flex;
    justify-content: center;
}
p{
    color: black;
    padding: 20px 10px;
    font-size: 25px;
    transition: all .5s;
    border-radius: 10px;
    
}
p:hover{
    padding: 20px 30px;
    cursor: pointer;
    transform: translateX(20px);
    color: #EF2D56;
    background-color: rgba(26, 26, 26, 0.178);
}
.icon{
    position: absolute;
    top: 0;
    margin: 20px 20px;
    font-size: 30px;
    text-align: center;
    transition: all .5s;
    color: black;
    
}
.icon:hover{
    cursor: pointer;
    color: transparent;
    -webkit-text-stroke: 1px #242424;
    
}
.active{
    
    color: #EF2D56;
   
}
@media (max-width:1800px){
    .container{
        display: none;
    }
}
</style>