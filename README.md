# bootsrap-two-column


```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    <style>
        h1{
            padding-top: 50px;
        }
        p{
            font-size: large;
            padding-top: 30px;
        }
        hr{
            height: 1.75px;
            background-color: black;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="row" style="margin-top: 200px;">
            <div class="col-md-6" style="background-color: rgb(97, 211, 231); height: 50vh; text-align: center;">
                <h1>HTML</h1>
                <hr>
                <p>
                    HTML (HyperText Markup Language) is the most basic building block of the Web. It defines the meaning and structure of web content. ... HTML uses "markup" to annotate text, images, and other content for display in a Web browser.
                </p>
            </div>
            <div class="col-md-6 "  style="background-color: rgb(240, 110, 106); height: 50vh; text-align: center;">
                <h1>CSS</h1>
                <hr>
                <p>
                    Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML.[1] CSS is a cornerstone technology of the World Wide Web, alongside HTML and JavaScript.[2]
                </p>
            </div>
        </div>
    </div>
</body>
</html>
```



```
<script type="text/javascript">
  var drawing = false;
  var ctx;

  window.onload=function(){
    document.getElementById('btnClear').addEventListener('click',function(){
      ctx.clearRect(0,0,ctx.canvas.width,ctx.canvas.height);
    },false);

      ctx.strokeStyle="#000";
      ctx.lineJoin="round";
      ctx.lineWidth=5;

    }
    function myClickEvent(e) {
    var message;
    ctx.beginPath();
    if (shape == 0){
        ctx.arc(e.offsetX, e.offsetY, 50, 0, 2 * Math.PI);
           
    }else if (shape==1){
        ctx.rect(e.offsetX, e.offsetY, 100, 100);
        
    }else if (shape == 2){
        ctx.strokeRect(e.offsetX,e.offsetY,150,100);
    
    }else if (shape == 3){
      ctx.moveTo(e.offsetX, e.offsetY);
          ctx.lineTo(e.offsetX-(100/2),e.offsetY-(100*0.86602));
          ctx.lineTo(e.offsetX+(100/2),e.offsetY-(100*0.86602));
          ctx.lineTo(e.offsetX,e.offsetY)
    }
    else if (shape == 4){
      ctx.moveTo(e.offsetX, e.offsetY);
      ctx.lineTo(e.offsetX+(100/2),e.offsetY+(100*0.86602));
      
      
    }

  ctx.stroke();
  }



function circleclicked() {
    shape=0;
}
function squareclicked() {
    shape=1;
}
</script>
<body>
    <div class="container">
        <div class="content">
            <h1>Drawing application</h1>
            <canvas 
            id="myCanvas"
            width="1315"
            height="600"
            style="border:1px solid #000000"></canvas>
            <div class="toolbar">
                <input type="button" id="circle" value="Circle"/>
                <input type="button" id="square" value="Square"/>
                <button id="btnClear">Clear</button><br>
    </div>
    </div>
    </div>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
shape=0;

c.addEventListener("click",myClickEvent);
document
.getElementById("circle")
.addEventListener("click",circleclicked);
document
.getElementById("square")
.addEventListener("click",squareclicked);
</script>
</body>
```
