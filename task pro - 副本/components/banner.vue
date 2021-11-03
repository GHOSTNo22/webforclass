<template>
	<div id="banner" class="w1" top:50px>
	    <a id="ba" href="catalog/catalog.html"><img id="img" src="./img/banner/img1.jpg" width=500px height=300px></a>
		
		</span>
	    <ul >
	        <li class="numb"><a href="catalog/catalog.html">1</a></li>
	        <li class="numb"><a href="catalog/cata2.html">2</a></li>
	        <li class="numb"><a href="catalog/cata3.html">3</a></li>
	        <li class="numb"><a href="catalog/cata4.html">4</a></li>
	    </ul>
	</div>
</template>

<script>
	module.exports={
		data:function() {
		  return {
			  urls:[
					require('./img/banner/img1.jpg'),
					require('./img/banner/img2.jpg'),
					require('./img/banner/img3.jpg'),
					require('./img/banner/img4.jpg')
				]
			}
	  }
	}
	methods:{
	var urls=new Array("./img/banner/img1.jpg","./img/banner/img2.jpg","./img/banner/img3.jpg","./img/banner/img4.jpg");
	  var lis=document.getElementById("banner").getElementsByTagName("li");
	  var Img=document.getElementById("img");	
	var address=document.getElementById("ba");
	var urlnet=new Array("catalog/img/catalog.html","catalog/img/cata1.html","catalog/img/cata3.html","catalog/img/cata4.html");
	  var len=lis.length;
	  for(var i=0;i<len;i++){
	      lis[i].onmouseover=function (){
	          for(var j=0;j<len;j++){
	              if(this==lis[j]){
	                  lis[j].className="numb_get";
	                  Img.src=urls[j];
	              }
	          }
	      }
	      lis[i].onmouseout=function () {
	          for(var j=0;j<len;j++){
	              if(this==lis[j]){
	                  lis[j].className="numb";
	              }
	          }
	      }
		address.onmouseover=function(){
			for(var m=0;m<len;m++){
				if(Img.src==urls[m]){
					address.href=urlnet[m];
				}
			}
		}
	 }
	}
</script>

<style scoped>
	#banner{
	       top: 500px;
	   left:500px;
	   position: static;
	   padding-bottom: 40px;
	   padding-left: 170px;
	   padding-top: 50px;
	    }
	    #banner ul{
	        left: 520px;
	        top: 440px;
	    }
	    #banner li{
	        width: 30px;
	        height: 30px;
	        text-align: center;
	        line-height: 30px;
	        font-size: 20px;
	        list-style: none;
	        float: left;
	        margin: 0px 10px;
		opacity: 0.5;
	    }
	    .numb_get{
	        border: 1px solid blue;
	        color: blue;
	        background: #fff;
		opacity: 0.5;
	    }
	    .numb{
		border: 1px solid blue;
	        color: #fff;
	        background: blue;
		opacity: 0.5;
		
	}
</style>
