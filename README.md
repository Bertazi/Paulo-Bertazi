<!DOCTYPE html>
<html>
    <head>
        <title>Calculadora</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            *{
                margin: 0;
                padding: 0;
            }
            .fundo{
                background-image: linear-gradient(45deg, #008DC6, #00B6FF);
                height: 100vh;
                color: white;
                font-family: Helvetica;
                text-align: center
            }
            .CALCULADORA{
                position: absolute;
                background-color: rgba(0,0,0,0.5);
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                border-radius: 30px;
                padding: 10px;                             
            }
            .botao{
                width: 50px;
                height: 50px;
                font-size: 25px;
                margin: 2px;
                border-radius: 20px;
                cursor: pointer;
                background-color: rgb(31,31,31);
                border: none;
                color: #fff
            }
            .botao:hover{
                background-color: black;                
            }
            #resultado{
                background-color: white;
                width: 197px;
                height: 30px;
                margin: 5px;
                color: black;
                text-align: right;
                padding: 10px;
                border-radius: 10px;
                font-size: 28px;
            }
        </style>    
    </head>
    <body>
        <div class="fundo">
            <h1>Paulo Bertazi</h1>
            <div class="CALCULADORA">
                <h2>SUPER CASSIO</h2>
                <P id="resultado"></P>
                <table>
                    <tr>
                        <td><button class="botao" onclick="clean()">C</button></td>
                        <td><button class="botao" onclick="back()"><</button></td>
                        <td><button class="botao" onclick="insert('/')">/</button></td>
                        <td><button class="botao" onclick="insert('*')">X</button></td>
                    </tr>
                    <tr>
                        <td><button class="botao" onclick="insert('7')">7</button></td>
                        <td><button class="botao" onclick="insert('8')">8</button></td>
                        <td><button class="botao" onclick="insert('9')">9</button></td>
                        <td><button class="botao" onclick="insert('-')">-</button></td>
                    </tr>
                    <tr>
                        <td><button class="botao" onclick="insert('4')">4</button></td>
                        <td><button class="botao" onclick="insert('5')">5</button></td>
                        <td><button class="botao" onclick="insert('6')">6</button></td>
                        <td><button class="botao" onclick="insert('+')">+</button></td>
                    </tr>
                    <tr>
                        <td><button class="botao" onclick="insert('1')">1</button></td>
                        <td><button class="botao" onclick="insert('2')">2</button></td>
                        <td><button class="botao" onclick="insert('3')">3</button></td>
                        <td rowspan="2"><button class="botao" style="height: 106px;"  onclick="calcular()">=</button></td>
                    </tr>
                    <tr>
                        <td colspan="2"><button class="botao" onclick="insert('0')" style="width: 106px;">0</button></td>
                        <td><button class="botao" onclick="insert('.')">.</button></td>
                    </tr>
                </table>
           
        </div>
            <script>
                function insert(num)
                {
                   var numero = document.getElementById('resultado').innerHTML;
                   document.getElementById('resultado').innerHTML = numero + num;
                }
                function clean()
                {
                    document.getElementById('resultado').innerHTML = ""
                }
                function back()
                {
                    var resultado = document.getElementById('resultado').innerHTML;
                    document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1);
                }
                function calcular()
                {
                    var resultado = document.getElementById('resultado').innerHTML;
                    if(resultado);
                    {
                        document.getElementById('resultado').innerHTML = eval(resultado);
                    }
                }
            </script>    
    </body>
</html>
