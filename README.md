# Cube-to-pentagon-transformation.
......html........
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
</head>
<body> 
    <div id="cube"></div>
</body>
</html>
.......css.........
html {
  height: 150vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: auto;
  background-color: #191970;
}
body {
  width: 150%;
  z-index: 2;
  overflow: hidden;
  height: 350px;
  background-color: #ffb6c1;
}
#cube{
  width:300px;
  height:400px;
  position:relative;
  left:50%;
  top:0;
  margin-left:-150px;
  background-image: linear-gradient(30deg, #ffffe0 30%, rgba(170,170,170,0) 30.1%), linear-gradient(-30deg, #ffffe0 30%, rgba(170,170,170,0) 30.1%);
  transform-style: preserve-3d;
} 
#cube:before,
#cube:after{
  display:block;
  content:'';
  position:absolute;
}
#cube::before{
  width:200px;
  height:280px;
  left:50px;
  top:-8px;
  background-repeat: no-repeat;
  background-repeat: no-repeat;
  background-image: linear-gradient(30deg, transparent 26%, #98fb98 26.3%, #98fb98 74%, transparent 74.3%), linear-gradient(150deg, transparent 26%, #00fa9a 26.3%, #00fa9a 74%, transparent 74.3%), linear-gradient(150deg, transparent 26%, #eee 26.3%, #eee 73%, transparent 73%), linear-gradient(30deg, transparent 27%, #eee 27%, #eee 74%, transparent 74.3%), radial-gradient(circle at center, #eee 20%, transparent 20%);
  background-size: 50% 60%;
  background-position: 0 100%, 100% 100%, 0 48.5%, 100% 48.5%, 50% 60%;
  -webkit-animation: cube-drop 6000ms infinite alternate linear;
          animation: cube-drop 6000ms infinite alternate linear;
  z-index: -1;
}
#cube:after{
  width:113px;
  height:100px;
  left:92px;
  top:164px;
  -webkit-animation:cube-shadow 6000ms infinite alternate linear;
          animation:cube-shadow 6000ms infinite alternate linear;
  z-index: 0;
}

@-webkit-keyframes cube-drop{
  20%{
    transform:translateY(0) translateZ(-1px);
  }
  80%, 100%{
    transform:translateY(153px) translateZ(-1px);
  }
}
@keyframes cube-drop{
  20%{
    transform:translateY(0) translateZ(-1px);
  }
  80%, 100%{
    transform:translateY(153px) translateZ(-1px);
  }
}
@-webkit-keyframes cube-shadow{
  0%,20%{
    transform:translateY(0) rotate(-30deg) skew(30deg);
    box-shadow: -50px 45px 10px -10px rgba(0,0,0,0.3);
  } 
  37%{ 
    box-shadow: -2px 2px 2px rgba(0,0,0,0.3);
  }
  37%,100%{
    transform:translateY(42px) rotate(-30deg) skew(30deg); 
  }
  39%,100%{ 
    box-shadow: -2px 2px 1px rgba(0,0,0,0.3);
  }
}
@keyframes cube-shadow{
  0%,20%{
    transform:translateY(0) rotate(-30deg) skew(30deg);
    box-shadow: -50px 45px 10px -10px rgba(0,0,0,0.3);
  } 
  37%{ 
    box-shadow: -2px 2px 2px rgba(0,0,0,0.3);
  }
  37%,100%{
    transform:translateY(42px) rotate(-30deg) skew(30deg); 
  }
  39%,100%{ 
    box-shadow: -2px 2px 1px rgba(0,0,0,0.3);
  }
}
  
