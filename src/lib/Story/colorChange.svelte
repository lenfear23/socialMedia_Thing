<script>
function colorc1(){
        let ttbox = document.querySelector(".titleBox");
        let ttcontent = document.querySelector(".content");
        // @ts-ignore
        ttbox.style.background="#0c97ce";
        // @ts-ignore
        ttcontent.style.boxShadow=`inset 10px 10px 50px #0a80af,
            inset -10px -10px 50px #0eaeed`;
    }
    function colorc2(){
        let ttbox = document.querySelector(".titleBox");
        let ttcontent = document.querySelector(".content");
        // @ts-ignore
        ttbox.style.background="#383F51";
        // @ts-ignore
        ttcontent.style.boxShadow=`inset 20px 20px 60px #2b313e,
            inset -20px -20px 60px #454d64`;
    }
    function colorc3(){
        let ttbox = document.querySelector(".titleBox");
        let ttcontent = document.querySelector(".content");
        // @ts-ignore
        ttbox.style.background="#D84A05";
        // @ts-ignore
        ttcontent.style.boxShadow=`inset 20px 20px 60px #842d03,
            inset -20px -20px 60px #ff6707`;
    }
    function colorc4(){
        let ttbox = document.querySelector(".titleBox");
        let ttcontent = document.querySelector(".content");
        // @ts-ignore
        ttbox.style.background="#70A37F";
        // @ts-ignore
        ttcontent.style.boxShadow=`inset 20px 20px 60px #567e62,
            inset -20px -20px 60px #8ac89c`;
    }
    function colorc5(){
        let ttbox = document.querySelector(".titleBox");
        let ttcontent = document.querySelector(".content");
        // @ts-ignore
        ttbox.style.background="#4C3957";
        // @ts-ignore
        ttcontent.style.boxShadow=`inset 20px 20px 60px #3b2c43,
            inset -20px -20px 60px #5d466b`;
    }
    function colorc6(){
        let ttbox = document.querySelector(".titleBox");
        // @ts-ignore
        let ttcontent = document.querySelector(".content").style;
        // @ts-ignore
        ttbox.style.background="#343a40";
        ttcontent.style.boxShadow=`inset 20px 20px 60px #2c3136,
            inset -20px -20px 60px #3c434a`;
    }
</script>
    <button class="color1" on:click={colorc1}></button>
    <button class="color2" on:click={colorc2}></button>
    <button class="color3" on:click={colorc3}></button>
    <button class="color4" on:click={colorc4}></button>
    <button class="color5" on:click={colorc5}></button>
    <button class="color6" on:click={colorc6}></button>

<style>
button{
    width: 35px;
    height: 35px;
    outline: none;
    border: none;
    border-radius: 5px;
}
button:hover{
    cursor: pointer;
}
.color1{
    background-color: #0c97ce;
}
.color2{
    background-color: #383F51;
}
.color3{
    background-color: #D84A05;
}
.color4{
    background-color: #70A37F;
}
.color5{
    background-color: #4C3957;
}
.color6{
    background-color: #343a40;
}
</style>