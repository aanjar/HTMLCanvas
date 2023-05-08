# HTMLCanvas

https://aanjar.github.io/HTMLCanvas/

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Canvas</title>
</head>
<body>
    <canvas id="canv" width="400" height="320" style="background-color: green;"></canvas>
    <script type="text/javascript">
        var canv = document.getElementById("canv");
        var c = canv.getContext("2d");
        let x = 10;
        let cepat = 4;
        function draw() {
            window.requestAnimationFrame(draw);
            c.clearRect(0,0, 400, 320)
            c.fillStyle = "white";
            c.beginPath();
            c.arc(x, 50, 10, 0, 2*Math.PI);
            c.fill();
            
            if (x + 10 > 400 || x - 10 < 0) {
                cepat = -cepat;
            }

            x += cepat;
        }
        draw();
    </script>
</body>
