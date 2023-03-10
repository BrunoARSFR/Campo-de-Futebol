# Campo-de-Futebol
Esse projeto foi criado com objetivo de praticar meus conhecimentos em HTML, CSS e JavaScript. 

----------HTML----------- 

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Campo de futebol</title>

    <link rel="stylesheet" href="style.css">

</head>
<body>
<main >
    <div class="logo invisivel">
        <div class="selecao"><h2>Seleção</h2></div>
        <div class="brasileira">Brasileira</div>
    </div>
    <div class="campo" >
        <div class="hover"><h1>Hover Me</h1></div>
        <div class="direita">
            <div class="area">
                <div class="penalti"></div>
            </div>
            <div class="pequenaArea"></div>
            <div class="meiaLua"></div>
        </div>
        <div class="esquerda">
            <div class="area ">
                <div class="penalti"></div>
            </div>
            <div class="pequenaArea"></div>
            <div class="meiaLua"></div>
        </div>
        <div class="centro"></div>
        <div class="circulo"></div>
        <div class="pontoCentro"></div>

        <div class="jogadores invisivel" id="jogadores"  readonly>
            <div class="goleiro">
                <div id="alisson"><p>Alisson</p><img src="./src/jogadores/Alisson.jfif" alt="Alisson"></div>
            </div>
            <div class="zagueiros">
                <div id="militao"><P>Eder Militão</P><img src="./src/jogadores/militão.png" alt="Militão"></div>
                <div id="tiago"><p>Tiago Silva</p><img src="./src/jogadores/tiago silva.jfif" alt="Tiago"></div>
                <div id="marquinhos"><p>Marquinhos</p><img src="./src/jogadores/marquinhos.jfif" alt="Marquinhos"></div>
                <div id="danilo"><p>Danilo</p><img src="./src/jogadores/danilo.jfif" alt="Danilo"></div>
            </div>
            <div class="meioCampo">
                <div id="neymar"><p>Neymar jr.</p><img src="./src/jogadores/neymar.jfif" alt="Neymar"></div>
                <div id="casemiro"><p>Casemiro</p><img src="./src/jogadores/casemiro.jfif" alt="Casemiro"></div>
                <div id="paqueta"><p>Paquetá</p><img src="./src/jogadores/paqueta.jfif" alt="Paqueta"></div>
    
            </div>
            <div class="atacante">
                <div id="vinijr"><p>Vini Jr</p><img src="./src/jogadores/vini jr.png" alt="Vinicius jr"></div>
                <div id="richarlison"><p>Richarlison</p><img src="./src/jogadores/richarlisson.jfif" alt=Richarlison"></div>
                <div id="rafinha"><p>Raphinha</p><img src="./src/jogadores/rafinha.png" alt="Rafinha"></div>
            </div>
        </div>
    </div>
    <div class="reservas invisivel">
        <ul class="nome">
            <h3 class="titulo">Reservas</h3>
            <div>Alex Sandro</div>
            <div>Fred</div>
            <div>Weverton</div>
            <div>Daniel Alves</div>
            <div>Fabinho</div>
            <div>Bruno Guimarães</div>
            <div>Antony</div>
            <div>Rodrygo</div>
            <div>Éverton Ribeiro</div>
            <div>Ederson</div>
            <div>Bremer</div>
            <div>Pedro</div>
            <div>Gabriel Martinelli</div>
        </ul>
        <ul class="numero">
            <h3 class="titulo">Número</h3>
            <div>6</div>
            <div>8</div>
            <div>12</div>
            <div>13</div>
            <div>15</div>
            <div>17</div>
            <div>19</div>
            <div>21</div>
            <div>22</div>
            <div>23</div>
            <div>24</div>
            <div>25</div>
            <div>26</div>
        </ul>
    </div>
</main>
</body>
</html>

---------CSS-------

*{
    margin: 0px;
    padding: 0px;
}
body{
    width: 100vw;
    height: 100vh;
    background-color: #1c1c1c;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
}
main{
    display: flex;
    align-items : center;
    justify-content: center;
    width: 100vw;
    height: 100vh;
    position: relative;
    flex-wrap: wrap;
}
.logo{
    position: absolute;
    left: 3rem;
    top: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.logo .selecao,
.logo .brasileira{
    width: 14rem;
    height: 5rem;  
}
.selecao{
    font-size: 3rem;
    color: yellow;
}
.brasileira{
    font-size: 3.5rem;
    color: green;
}
.campo{
    width:35rem;
    height: 25rem;
    background-color: green;
    border: 4px solid aliceblue;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    transition: 1s;
    opacity: 1;

}
.centro{
    z-index: 4;
    position: relative;
    height: 100%;
    width: 4px;
    background-color:white;
    
    display: flex;
    justify-content: center;
    align-items: center;
    
}

.circulo{
    height:100px;
    width: 100px;
    z-index: 3;
    position:absolute;
    border: 4px solid aliceblue;
    border-radius: 50%;
}
.pontoCentro, .penalti{
    height: 5px;
    width: 5px;
    position:absolute;
    border: 4px solid aliceblue;
    border-radius:50%;
    background-color: aliceblue;
    z-index: 1;
}

.direita, 
.esquerda{
    width:50% ;
    height: 100%;
    position: absolute;
    display: flex;
    align-items: center;
    
}
.direita{
    right: 0;
}
.esquerda{
    left: 0;
}
.pequenaArea{
    height: 100px;
    width: 50px;
    position: absolute;
    border: 4px solid aliceblue;
    z-index: 3;
}
.direita .pequenaArea, .direita .area{
    right: 0;
}
.area{
    height: 200px;
    width: 100px;
    position: absolute;
    border: 4px solid aliceblue; 
    background-color: green;
    z-index: 1;   
    display: flex;
    align-items: center;   
}
.direita .area,
.direita .pequenaArea{
    border-right: 0;
}
.esquerda .area,
.esquerda .pequenaArea{
    border-left: 0;
}
.direita .penalti{
    left: 10px;
}
.esquerda .penalti{
    right: 10px;
}

.meiaLua{
    content: "";
    color: #1c1c1c;
    border: 4px solid aliceblue;
    border-radius: 50%;
    height: 100px;
    width: 100px;
    position: absolute;
    right: 40px;
    z-index: 0;
}
.esquerda .meiaLua{
    left: 40px;
}
main:hover .campo{
    transition: 1s;
    rotate: 90deg;
    
}
.hover{
    font-size: 2.5rem;
    position: absolute;
    z-index: 7;
    opacity: 1;
    bottom: 5px;
    color: yellow;
    -webkit-text-stroke-width: 1.5px;
    -webkit-text-stroke-color: #1c1c1c;
    transition: 1s;
}
main:hover .hover{
    opacity: 0;
    transition: 1s;
}

main:hover .invisivel{
    z-index: 5;
    transition: 1s 1s;
    opacity: 1;
    
}
.jogadores img{
    border: 4px solid yellow;
    width: 50px;
    border-radius: 50%;
    z-index: 5;
}
.jogadores{
    z-index: 5;
    width:25rem;
    height: 35rem;
    display: flex;
    flex-direction: column-reverse;
    rotate: -90deg;
    transition: 1s;
    position: absolute;
}

.goleiro{
    display: flex;
    justify-content: center;
    margin-top: 10px;
}
.zagueiros{
    display: flex;
    justify-content: center;
    gap: 2em;
}
#militao, #danilo{
    font-size: 14px;
}
#tiago, #marquinhos{
    margin-top: 35px;
}
.meioCampo{
    display: flex;
    justify-content: center;
}
#neymar{
    margin: 0px 0px 150px 0px;
}
#casemiro{
    margin: 150px 10px 0px 0px;
}
#paqueta{
    margin: 50px 0px 0px 0px;   
}
.atacante{
    display: flex;
    justify-content: center;
    gap: 100px;
}
#vinijr, #rafinha{
    margin-top: 50px;
}
.goleiro div,
.zagueiros div,
.meioCampo div,
.atacante div{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2px;
    color: aliceblue;
    -webkit-text-stroke-width: 0.2px;
    -webkit-text-stroke-color: black;
}
.invisivel{
    opacity: 0;
}
.reservas{
    position: absolute;
    right: 10%;
    display: flex;
    gap: 5px;
    padding: 15px;
    background-color: green;
    border: 3px white outset;
    z-index: 5;
    
}
.nome div,
.numero div,
.titulo{
    color: aliceblue;
    opacity: 1;
}
.numero div{
    display: flex;
    justify-content: center;
}
