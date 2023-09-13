<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tetris</title>

    <style>
        body{
            margin: 0;
            padding: 0;
            background: rgb(152, 152, 152);
        }

        .container-canvas{
            display: flex;
            flex-direction: column; 
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            padding: 0;
        }

        canvas{
            background: rgb(12, 12, 12);
            border: solid 4px purple;
        }

        h3{
            color: purple;
        }
    </style>
</head>


<body>
    <div class="container-canvas">
    <div>
        <h3>"a" Movimiento izquierda<br>
            "d" Movimiento derecha<br>
            "w" Rotar pieza<br>
            "s" Baja con velocidad</h3>
    </div>
        <canvas id="myCanvas" width="200" height="400"></canvas>
    </div>

    <script>
        var canvas = document.getElementById("myCanvas");
        var ctx = canvas.getContext("2d");
        var jugar = false;
        var filas = 20;
        var columnas = 10;
        var bloques = 20;
        var speed = 400;
        var numRandom;
        var elemento;
        var nombreElemento = '';
        var elementoPlayer = '';
        var score = 0;
        var segundos = 0;
        var minutos = 0;
        var horas = 0;
        var fondoMenu = new Image();
        var tetrisTheme = new Audio();
        var rotar = new Audio();
        var fila = new Audio();
        var fuego = new Audio();
        var agua = new Audio();
        var planta = new Audio();

        window.requestAnimationFrame = (function () {
            return window.requestAnimationFrame ||
                window.webkitRequestAnimationFrame ||
                window.mozRequestAnimationFrame ||
                function (callback) {
                    window.setTimeout(callback, 17);
                };
            }());

        function cuadrado(x,y,elemento){
            ctx.fillStyle = elemento;
            ctx.fillRect(x * bloques,y * bloques,bloques, bloques);
            ctx.strokeStyle = "black";
            ctx.strokeRect(x * bloques,y * bloques,bloques, bloques);
        }

        var mapa = [];
        for (let i = 0; i<filas; i++){
            mapa[i] = Array(columnas).fill("black");
        }

        function dibujarMapa(){
            for (let fila = 0; fila<filas; fila++){
                for (let column = 0; column<columnas; column++){
                    cuadrado(column,fila,mapa[fila][column]);
                }
            }
        }

        var piezas={
            i: [[1], [1], [1], [1]],
            j: [[1, 0, 0], [1, 1, 1]],
            l: [[0, 0, 1], [1, 1, 1]],
            o: [[1, 1], [1, 1]],
            s: [[0, 1, 1], [1, 1, 0]],
            t: [[0, 1, 0], [1, 1, 1]],
            z: [[1, 1, 0], [0, 1, 1]]
        };

        function generarElemento(){
            numRandom = getRandomInt(3);

            if(numRandom === 1){
                elemento = 'rgb(242, 57, 35)';
                nombreElemento = 'fuego';
            }

            if(numRandom === 2){
                elemento = 'rgb(77, 120, 254)';
                nombreElemento = 'agua';
            }

            if(numRandom === 3){
                elemento = 'rgb(48, 200, 20)';
                nombreElemento = 'planta';
            }
        }
        generarElemento()

        function piezaRandom(){
            var allPiezas = Object.keys(piezas);
            var rdmPieza = allPiezas[getRandomInt(allPiezas.length) - 1];
            return piezas[rdmPieza];
        }

        var piezaActual = piezaRandom();
        var actualX = 4;
        var actualY = 0;
        function dibujarPieza(){
            for (let i = 0; i<piezaActual.length; i++){
                for (let j = 0; j<piezaActual[i].length; j++){
                    if(piezaActual[i][j]){
                        cuadrado(actualX + j, actualY + i, elemento);
                    }
                }
            }
        }

        function moveDown(){
        actualY++;
            if(seTocan()){
                actualY--;
                juntarPiezas();
                piezaActual = piezaRandom();
                actualX = 4;
                actualY = 0;
            }
        }

        var mapaX;
        var mapaY;
        function seTocan(){
            for (let i = 0; i<piezaActual.length; i++){
                for (let j = 0; j<piezaActual[i].length; j++){
                    if(piezaActual[i][j]){
                        mapaX = actualX + j;
                        mapaY = actualY + i;
                        if(mapaY >= filas || mapaX < 0 || mapaX >= columnas || mapaY >= 0 && mapaY < filas && mapa[mapaY][mapaX] !== "black"){
                            console.log(mapaY)
                            return true;
                        }
                    }
                }
            }
        }

        function juntarPiezas(){
            for (let i = 0; i<piezaActual.length; i++){
                for (let j = 0; j<piezaActual[i].length; j++){
                    if(piezaActual[i][j]){
                        var mapaX = actualX + j;
                        var mapaY = actualY + i;
                        if(mapaY >= 0 && mapaY < filas){
                            mapa[mapaY][mapaX] = elemento;
                        }
                    }
                }
            }
            clear();
            generarElemento()
        }

        fuego.src = "sounds/fuego.mp3";
        agua.src = "sounds/agua.mp3";
        planta.src = "sounds/planta.mp3";
        fila.src = "sounds/fila.mp3";

        function clear(){
            for (let i = filas - 1; i >= 0; ){
                if(mapa[i].every((cell) => cell === elemento && nombreElemento === elementoPlayer)){
                    if(elementoPlayer === "fuego"){
                        fuego.play();
                    }
                    else if(elementoPlayer === "agua"){
                        agua.play();
                    }
                    else if(elementoPlayer === "planta"){
                        planta.play();
                    }

                    for (let j = i; j > 0; j--){
                        mapa[j] = [...mapa[j - 1]];
                    }
                    mapa[0] = Array(columnas).fill("black");
                    score += 100;
                    console.log(score);

                }else if(mapa[i].every((cell) => cell !== "black")){
                    if(mapa[i].every((cell) => cell === "rgb(242, 57, 35)")){
                        fuego.play();
                    }
                    else if(mapa[i].every((cell) => cell === "rgb(77, 120, 254)")){
                        agua.play();
                    }
                    else if(mapa[i].every((cell) => cell === "rgb(48, 200, 20)")){
                        planta.play();
                    }else{
                        fila.play();
                    }

                    for (let j = i; j > 0; j--){
                        mapa[j] = [...mapa[j - 1]];
                    }
                    mapa[0] = Array(columnas).fill("black");
                    score += 10;
                    console.log(score);
                }else{
                    i--;
                }
            }
        }

        function update(){
            if(elementoPlayer === ""){
                fondoMenu.src = "images/fondoMenu.png";
                ctx.drawImage(fondoMenu, 0, 0, 200, 400);

                ctx.fillStyle = "white";
                ctx.font = "12px Arial";
                ctx.fillText("Instrucciones", 65, 40);

                ctx.fillText("-Selecciona uno de los 3 elementos.", 5, 60);
                ctx.fillText("-La filas formadas de tu elemento", 10, 80);
                ctx.fillText("tendran un valor de 100 puntos.", 10, 95);
                ctx.fillText("-Las filas formadas por cualquier", 10, 115);
                ctx.fillText("otra convinación de elementos", 10, 130);
                ctx.fillText("tendran un valor de 10 puntos.", 10, 145);

                ctx.fillStyle = "rgb(242, 57, 35)";
                ctx.fillText("<Oprime 1> para el elemento fuego", 5, 190);
                ctx.fillRect(90,200, 20, 20);
                ctx.strokeRect(90,200, 20, 20);

                ctx.fillStyle = "rgb(77, 120, 254)";
                ctx.fillText("<Oprime 2> para el elemento agua", 5, 250);
                ctx.fillRect(90,260, 20, 20);
                ctx.strokeRect(90,260, 20, 20);

                ctx.fillStyle = "rgb(48, 200, 20)";
                ctx.fillText("<Oprime 3> para el elemento planta", 5, 310);
                ctx.fillRect(90,320, 20, 20);
                ctx.strokeRect(90,320, 20, 20);
            }else{
                ctx.clearRect(0, 0, 200, 400);

                dibujarMapa();
                dibujarPieza();
                moveDown();

                ctx.fillStyle = "white";
                ctx.font = "12px Arial";
                ctx.fillText("Puntaje: " + score, 10, 15);

                ctx.fillText("Elemento: " + elementoPlayer, 60, 35);

                actualizarContador();
                ctx.fillText("Tiempo: " + horas + ":" + minutos + ":" + segundos, 110, 15);
                if(minutos === 3){
                    speed = 300;
                }
                if(minutos === 6){
                    speed = 200;
                }
                if(minutos === 9){
                    speed = 100;
                }
                
            }
            
            if(mapaY < 2){
                ctx.drawImage(fondoMenu, 0, 0, 200, 400);
                ctx.font = "22px Arial";
                ctx.fillText("Juego Terminado", 15, 150);
                ctx.fillText("Puntaje: " + score, 40, 220);

                tetrisTheme.pause();
                jugar = false;
            }

            setTimeout(() =>{
                requestAnimationFrame(update);
            }, speed);
        }

        function rotarPieza(){
            var piezaAntes = piezaActual.slice();
            piezaActual = piezaActual[0].map((_, column) => piezaActual.map((fila) => fila[column]));
            piezaActual.forEach((row) => row.reverse());

            if(seTocan()){
                piezaActual = piezaAntes;
            }
        }

        function actualizarContador() {
            segundos++;
            if(segundos === 60){
                segundos = 0;
                minutos++;
                if(minutos === 60){
                    minutos = 0;
                    horas++;
                }
            }
        }

        tetrisTheme.src = "sounds/tetrisTheme.mp3";
        rotar.src = "sounds/rotar.mp3";

        document.addEventListener("keydown", (e) =>{
            if(e.keyCode===65){
                if(jugar){
                    actualX--;
                    if(seTocan()){
                        actualX++;
                    }
                }
            }
            
            if(e.keyCode===68){
                if(jugar){
                    actualX++;
                    if(seTocan()){
                        actualX--;
                    }
                }
            }
            
            if(e.keyCode===83){
                if(jugar){
                    moveDown(); 
                }
                
            }

            if(e.keyCode === 87){
                if(jugar){
                    rotar.play();
                    rotarPieza();
                }
            }

            if(e.keyCode === 49){
                if(!jugar){
                    elementoPlayer = 'fuego';
                    jugar = true;
                    tetrisTheme.play();
                    tetrisTheme.loop = true;
                }
            }

            if(e.keyCode === 50){
                if(!jugar){
                    elementoPlayer = 'agua';
                    jugar = true;
                    tetrisTheme.play();
                    tetrisTheme.loop = true;
                }
            }

            if(e.keyCode === 51){
                if(!jugar){
                    elementoPlayer = 'planta';
                    jugar = true;
                    tetrisTheme.play();
                    tetrisTheme.loop = true;
                }
            }
        });

        function getRandomInt(max) {
            return Math.floor(Math.random() * max) + 1;
        }

        update();
    </script>
</body>
</html>