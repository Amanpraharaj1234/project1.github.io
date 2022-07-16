<html>
<head>
    <style type="text/css">
    	body {
   padding:200px;
  background:skyblue; 

}

.content {
 display: flex;
  align-items: center;
  justify-content: center;
  padding:300px;
}
.sun {
  display:inline-block;
  border-radius:50%;
  height:200px;
  width:200px;
  background:orange;
  box-shadow: 0 0 10px orange,
                0 0 60px orange,
                0 0 200px yellow,
                inset 0 0 80px yellow;
  z-index:12;
  align:center;
  z-index:-99;
}

.cloud {
  display:inline-block;
  background:white;
  width:120px;
  height:120px; 
  border-radius:50%;
  position:relative;
  top:-30px;
  -webkit-filter: blur(6px);
  z-index:11;
  left:-50px;
  animation: 15000ms cloudAnimation linear infinite;
  opacity:0.76;
}
.cloud:before {
  content:"";
  display:inline-block;
  background:white;
  width:100px;
  height:100px; 
  -webkit-filter: blur(3px);
  position:relative;
  border-radius:50%;
  top:-30px;
  left:60px;
}
.cloud:after {
  content:"";
  display:inline-block;
  background:white;
  width:200px;
  height:100px; 
  -webkit-filter: blur(3px);
  position:relative;
  border-radius:50%;
  top:-80px;
  left:70px;
}

.cloud:first-child {zoom:1.5}

@keyframes cloudAnimation {
  0%{
    transform: translate(-100px,0);
  }
  100% {
    transform: translate(600px,0);
  }
}
 </style>
</head>
<body>
	<div class="content">
<div class="cloud"></div>
<div class="sun"></div><br>
<div class="cloud x"></div><br>
 </div>
</body>
</html>