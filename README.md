<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo Gerenciamento - Versão Mobile</title>
    <style>
        /* Estilos para o cabeçalho */
        .header {
            background-color: #000;
            padding: 20px;
            color: #fff;
            font-family: Arial, sans-serif;
            text-align: center;
        }

        /* Estilos para o corpo */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        /* Estilos para o texto normal */
        p {
            color: #333;
            font-size: 9.6px;
        }

        /* Estilo para o texto no cabeçalho */
        .header span {
            display: block;
        }

        /* Estilo para a contagem de dias */
        #contagemDias {
            display: inline-block;
            font-size: 9.6px;
            margin-left: 20px;
            background-color: #0000ff;
            padding: 4px;
            border: 1.6px solid #0077b3;
            border-radius: 3.2px;
            color: white;
        }

        /* Estilo para o botão */
        .button {
            font-family: "Arial Black", Arial, sans-serif;
            font-size: 7.2px;
            color: orange;
            background-color: transparent;
            border: 1.6px solid orange;
            padding: 4px 8px;
            cursor: pointer;
            display: block;
            margin: 4px auto;
        }

        /* Estilo para a caixa azul */
        .blue-box {
            background-color: #0000ff;
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #0077b3;
            border-radius: 3.2px;
            color: white;
            font-size: 8px;
            margin-top: 8px;
        }

        /* Estilo para a caixa dourada */
        .golden-box {
            background-color: #ffd700;
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #b8860b;
            border-radius: 3.2px;
            color: #333;
            font-size: 8px;
            margin-top: 8px;
        }

        /* Estilo para a caixa laranja fluorescente */
        .orange-fluorescent-box {
            background-color: #FF9900;
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #FF6600;
            border-radius: 3.2px;
            color: white;
            font-size: 8px;
            margin-top: 8px;
            font-weight: bold;
        }

        /* Estilo para a caixa cinza */
        .gray-box {
            background-color: #808080;
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #333;
            border-radius: 3.2px;
            color: white;
            font-size: 8px;
            margin-top: 8px;
        }

        /* Estilo para a caixa população */
        .population-box {
            background-color: #00cc00;
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #007700;
            border-radius: 3.2px;
            color: white;
            font-size: 8px;
            margin-top: 8px;
        }

        /* Estilo para o texto piscante */
        .blinking {
            animation: blinkingText 1s infinite;
        }

        @keyframes blinkingText {
            0% { opacity: 1.0; }
            50% { opacity: 0.0; }
            100% { opacity: 1.0; }
        }

        /* Estilo para o texto branco */
        .white-text {
            color: white;
        }

        /* Estilo para as telas azul, amarela, verde e laranja */
        .colored-box {
            display: inline-block;
            padding: 4px;
            border: 1.6px solid #0077b3;
            border-radius: 3.2px;
            color: white;
            font-size: 8px;
            margin-top: 8px;
            width: 25%;
        }

        /* Estilo para o layout com as quatro telas */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
        }

        /* Estilo para cada célula da grid */
        .grid-item {
            display: flex;
            justify-content: center;
            align-items: center;
        }
    </style>
</head>
<body>
    <div class="header">
        <span class="white-text">Domine o Simulador Banco de Fomento 🏙🌆🌇🌁</span>
    </div>
     <div class="grid-container">
        <!-- Tela Azul: Jogo de Gerenciamento de Empresas -->
        <div class="grid-item blue-box">
            <div class="blinking">
                <button class="button" onclick="toggleJogo()">Iniciar Jogo</button>
            </div>
            <span id="contagemDias"></span>
        </div>
        <!-- Tela Amarela: Dinheiro em Caixa -->
        <div class="grid-item golden-box">
            <h3 style="font-size: 9.6px; margin: 0; color: #fff;">Dinheiro em Caixa</h3>
            <span id="valor" style="font-size: 12.8px; color: #fff;">R$ 1.999.000.000.000</span>
        </div>
        <!-- Tela Verde: População Brasileira -->
     
        <div class="grid-item population-box">
         
            <h3 style="font-size: 9.6px; margin: 0; color: #fff;">População Brasileira</h3>
         
            <span id="populacao" style="font-size: 12.8px; color: #fff;"
             
             </p>
              >214.000.000</span>
        </div>
        <!-- Tela Laranja: Lucros Diários -->
        <div class="grid-item orange-fluorescent-box">
            <p>
                <span id="lucrosText" class="blinking white-text">Lucros Diários: <span id="lucros" style="font-size: 9.6px; background-color: #FF9900; color: #fff;">R$ 0</span></span>
                <button id="somarAoCaixaBtn" class="button white-text blinking" onclick="somarAoCaixa()">Somando ao Caixa</button>
            </p>
        </div>
    </div>

 
    <!-- Tela Palmeiras -->
    <div class="gray-box">
<span id="valor" style="font-size: 15.8px; color: #fff;">Sociedade Esportiva Palmeiras</span>
</p>
<!-- Tela 1.4:Posição Brasileiro-->
        <span style="font-size: 9px; color: #fff;">Campeonato Brasileiro</span><span id="quantidadePPV" style="font-size: 9px; color: #fff;"> 10 Lugar</span>
    <p>

        <!-- Tela 1.1: Comprar Palmeiras -->
        <button class="button white-text" onclick="comprarEmpresaPAL()"> <span id="lucrosText" class="blinking white-text">Clique Aqui para Comprar: <span id= style="font-size: 10.9px; background-color: #FF9900; color: #fff;"></span></span> Palmeiras Por 1,2 Trilhões (Rende 1,1 Milhões por dia) Empregando 1 Mil Colaboradores.</button>

<!-- Tela 1.4: Quantidades de Palmeiras -->
        <span style="font-size: 9px; color: #fff;">Palmeiras </span><span id="quantidadePAL" style="font-size: 9px; color: #fff;">0</span>
    <p>

<!-- Tela 1.2: Investimentos Palmeiras -->
        <button class="button white-text" onclick="comprarInvestimentoPalmeiras()">Clique para Investir em melhoria no elenco Por 500 Milhões (Rende 100 Mil por dia) Empregando 0,1 Mil funcionários.que vai aumentar sua suas chances de vitórias e ganhar o Campeonato Brasileiro, Libertadores e Copa do Brasil </button>
 <span style="font-size:
   8px; color: #fff;">Quantidades de Melhorias no elenco: </span><span id="quantidadePD" style="font-size: 8px; color: #fff;">0</span>

<!-- Tela 1.2.2: Vender Jogadores -->
        <button class="button white-text" onclick="venderPD()">Clique Aqui para vender jogadores não utilizados por 150 Milhões .</button>

        <!-- Tela 1.3: Vender Palmeiras -->
        <button class="button white-text" onclick="venderPAL()">Clique Aqui para Vender Palmeiras pelo mesmo valor.</button>
       

<!-- Tela 1.5: Quantidades Brasileiro -->
        <span style="font-size: 9px; color: #fff;">Quantidades Brasileiros : </span><span id="quantidadePALBRA" style="font-size: 9px; color: #fff;"> 0</span>
    </p>
  
    
   <!-- Tela 1.6: Quantidades Libertadores -->
        <span style="font-size: 9px; color: #fff;">Quantidades Libertadores : </span><span id="quantidadePLIB" style="font-size: 9px; color: #fff;"> 0</span>
    
    </p>
   <!-- Tela 1.5: Quantidades Copa do Brasil-->
        <span style="font-size: 9px; color: #fff;">Quantidades Copa do Brasil :</span><span id="quantidadePCOPA" style="font-size: 9px; color: #fff;"> 0</span>
    
    
    </div>





    <!-- Tela 2 Cinza contendo três telas -->
    <div class="gray-box">

<span id="valor" style="font-size: 15.8px; color: #fff;">Empresas de Energia Elétrica</span>

        <!-- Tela 2.1: Construir Empresas de Energia Elétrica -->
<button class="button white-text" onclick="comprarEmpresaLM()"> <span id="lucrosText" class="blinking white-text">Clique Aqui para Construir: <span id= style="font-size: 10.9px; background-color: #FF9900; color: #fff;"></span></span> Empresas de Energia Elétrica Por 999,850 Bilhões (Rende 99 Milhões por dia) Empregando 15,2 Mil funcionários.</button>

<!-- Tela 2.2: Investimentos Empresas de Energia Elétrica -->
        <button class="button white-text" onclick="comprarEmpresaPM()">Clique para Investir em Pesquisa e Desenvolvimento & Propriedade Intelectual na Empresa Por 4,5 Bilhões (Rende 500 Mil por dia) Empregando 0,1 Mil funcionários.</button>
 <span style="font-size:
   8px; color: #fff;">Quantidades de Pesquisas & Propriedades Intelectuais na Empresa: </span><span id="quantidadePM" style="font-size: 8px; color: #fff;">0</span>

<!-- Tela 1.2.2: Vender Transferência de Propriedade Intelectual -->
        <button class="button white-text" onclick="venderPM()">Clique Aqui para Transferência de Tecnologia por 16 Bilhões .</button>


        <!-- Tela 2.2: Vender Empresas de Energia Elétrica-->
        <button class="button white-text" onclick="venderLM()">Clique Aqui para Vender Empresas Energia Elétrica pelo mesmo valor.</button>
        <!-- Tela 2.3: Quantidades de Empresas de Energia Elétrica-->
        <span style="font-size: 8px; color: #fff;">Quantidades de Empresas Energia Elétrica : </span><span id="quantidadeLM" style="font-size: 8px; color: #fff;">0</span>
    </div>
  <div>    
</div>

<script>
     let diasInvestimentoPalmeiras = 0;
     let posicaoCampeonato = 10;
     let maxPosicao = 1;
     let valorReserva = 1990000000000;
        let valorUnidadePAL = 0;
        let quantidadeUnidadesPAL = 0;
        let valorUnidadeLM = 0;
        let quantidadeUnidadesLM = 0;
        let valorUnidadeES = 0;
        let quantidadeUnidadesES = 0;
        let valorUnidadePD = 0;
        let quantidadeUnidadesPD = 0;
        let valorUnidadePM = 0;
        let quantidadeUnidadesPM = 0;
        let valorUnidadePS = 0;
        let quantidadeUnidadesPS = 0;


        let populacaoBrasileira = 214000000; // População inicial definida como 214.000.000
        let data = new Date(2000, 0, 1); // Definir a data inicial para 01/01/2000
        let historicoComprasPAL = [];
        let historicoComprasLM = [];
        let historicoComprasES = [];
        let historicoComprasPD = [];
        let historicoComprasPM = [];
        let historicoComprasPS = [];
        let podeAumentarLucro = false; // Variável que controla o aumento do lucro diário
        let jogoIniciado = false;
        let intervalId;
        function formatNumberWithCommas(number) {
            return number.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
        }
        function formatDate(date) {
            const day = date.getDate().toString().padStart(2, "0");
            const month = (date.getMonth() + 1).toString().padStart(2, "0");
            const year = date.getFullYear().toString();
            return `${day}/${month}/${year}`;
        }
        function updateValues() {
            const lucrosPorEmpresaPAL = 1100000; // Lucro por cada Empresa Palmeiras 
            const lucrosPorEmpresaLM = 99999999; // Lucro por cada Empresa Leroy Merlin
            
const lucrosPorEmpresaPD = 100000; // Lucro por cada Melhoria no elenco 
const lucrosPorEmpresaPM = 500000; // Lucro por cada de Energia Elétrica Pesquisa e Desenvolvimento

const lucrosDiariosPAL = quantidadeUnidadesPAL * lucrosPorEmpresaPAL;
            const lucrosDiariosLM = quantidadeUnidadesLM * lucrosPorEmpresaLM;
            
           const lucrosDiariosPD = quantidadeUnidadesPD * lucrosPorEmpresaPD;
           const lucrosDiariosPM = quantidadeUnidadesPM * lucrosPorEmpresaPM;
          
            document.getElementById("valor").textContent = "R$ " + formatNumberWithCommas(valorReserva);
            document.getElementById("lucros").textContent = "R$ " + formatNumberWithCommas(lucrosDiariosPAL + lucrosDiariosLM + lucrosDiariosPD + lucrosDiariosPM );
            document.getElementById("quantidadePAL").textContent = quantidadeUnidadesPAL;
            document.getElementById("quantidadeLM").textContent = quantidadeUnidadesLM;
                  
           document.getElementById("quantidadePD").textContent = quantidadeUnidadesPD;
          document.getElementById("quantidadePM").textContent = quantidadeUnidadesPM;
          
                       document.getElementById("contagemDias").textContent = formatDate(data);
            document.getElementById("populacao").textContent = formatNumberWithCommas(populacaoBrasileira);
         

        }

        function comprarEmpresaPAL() {
           // Impede a compra se o jogo não estiver iniciado ou se o dinheiro em caixa for negativo
               if (!jogoIniciado || valorReserva < 0) return;

            if (populacaoBrasileira < 1000) {
                document.getElementById("mensagemMaoDeObra").style.display = "flex";
                return;
            }
            historicoComprasPAL.push({
                valorReserva: valorReserva,
                quantidadeUnidadesPAL: quantidadeUnidadesPAL,
                data: new Date(data),
            });
            valorReserva -= 1200000000000;
            valorUnidadePAL += 1;
            quantidadeUnidadesPAL = valorUnidadePAL;
            populacaoBrasileira -= 1000;
            updateValues();
            if (!podeAumentarLucro) {
                podeAumentarLucro = true;
            }
            document.getElementById("valor").classList.add("blinking");
            setTimeout(() => {
                document.getElementById("valor").classList.remove("blinking");
            }, 1000);
        }
        function venderPAL() {
            if (!jogoIniciado) return;
            if (quantidadeUnidadesPAL > 0) {
                historicoComprasPAL.push({
                    valorReserva: valorReserva,
                    quantidadeUnidadesPAL: quantidadeUnidadesPAL,
                    data: new Date(data),
                });
                valorReserva += 1200000000000;
                valorUnidadePAL -= 1;
                quantidadeUnidadesPAL = valorUnidadePAL < 0 ? 0 : valorUnidadePAL;
                populacaoBrasileira += 12200;
                updateValues();
            }
        }

function comprarInvestimentoPalmeiras() {
           // Impede a compra se o jogo não estiver iniciado ou se o dinheiro em caixa for negativo
               if (!jogoIniciado || valorReserva < 0) return;

            if (populacaoBrasileira < 100) {
                document.getElementById("mensagemMaoDeObra").style.display = "flex";
                return;
            }
            historicoComprasPD.push({
                valorReserva: valorReserva,
                quantidadeUnidadesPD: quantidadeUnidadesPD,
                data: new Date(data),
            });
            valorReserva -= 500000000;
            valorUnidadePD += 1;
            quantidadeUnidadesPD = valorUnidadePD;
            populacaoBrasileira -= 100;
            updateValues();
            if (!podeAumentarLucro) {
                podeAumentarLucro = true;
            }
          
           maxPosicao = 1; // Ou 2, dependendo da estratégia
            document.getElementById("valor").classList.add("blinking");
            setTimeout(() => {
                document.getElementById("valor").classList.remove("blinking");
            }, 1000);
        }
        function venderPD() {
    if (!jogoIniciado) return;
    if (quantidadeUnidadesPD > 0) {
        historicoComprasPD.push({
            valorReserva: valorReserva,
            quantidadeUnidadesPD: quantidadeUnidadesPD,
            data: new Date(data),
        });
        valorReserva += 150000000;
        valorUnidadePD -= 0;
        quantidadeUnidadesPD = valorUnidadePD < 0 ? 0 : valorUnidadePD;
        populacaoBrasileira += 1;
        updateValues();
    }
}



        function comprarEmpresaLM() {
            // Impede a compra se o jogo não estiver iniciado ou se o dinheiro em caixa for negativo
            if (!jogoIniciado || valorReserva < 0) return;
            if (populacaoBrasileira < 15200) {
                document.getElementById("mensagemMaoDeObra").style.display = "flex";
                return;
            }
            historicoComprasLM.push({
                valorReserva: valorReserva,
                quantidadeUnidadesLM: quantidadeUnidadesLM,
                data: new Date(data),
            });
            valorReserva -= 936850000000;
            valorUnidadeLM += 1;
            quantidadeUnidadesLM = valorUnidadeLM;
            populacaoBrasileira -= 15200;
            updateValues();
            if (!podeAumentarLucro) {
                podeAumentarLucro = true;
            }
            document.getElementById("valor").classList.add("blinking");
            setTimeout(() => {
                document.getElementById("valor").classList.remove("blinking");
            }, 1000);
        }
        function venderLM() {
            if (!jogoIniciado) return;
            if (quantidadeUnidadesLM > 0) {
                historicoComprasLM.push({
                    valorReserva: valorReserva,
                    quantidadeUnidadesLM: quantidadeUnidadesLM,
                    data: new Date(data),
                });
                valorReserva += 936850000000;
                valorUnidadeLM -= 1;
                quantidadeUnidadesLM = valorUnidadeLM < 0 ? 0 : valorUnidadeLM;
                populacaoBrasileira += 15200;
                updateValues();
              }
          }

function comprarEmpresaPM() {
           // Impede a compra se o jogo não estiver iniciado ou se o dinheiro em caixa for negativo
               if (!jogoIniciado || valorReserva < 0) return;

            if (populacaoBrasileira < 100) {
                document.getElementById("mensagemMaoDeObra").style.display = "flex";
                return;
            }
            historicoComprasPM.push({
                valorReserva: valorReserva,
                quantidadeUnidadesPM: quantidadeUnidadesPM,
                data: new Date(data),
            });
            valorReserva -= 3500000000;
            valorUnidadePM += 1;
            quantidadeUnidadesPM = valorUnidadePM;
            populacaoBrasileira -= 100;
            updateValues();
            if (!podeAumentarLucro) {
                podeAumentarLucro = true;
            }
            document.getElementById("valor").classList.add("blinking");
            setTimeout(() => {
                document.getElementById("valor").classList.remove("blinking");
            }, 1000);
        }
        function venderPM() {
    if (!jogoIniciado) return;
    if (quantidadeUnidadesPM > 0) {
        historicoComprasPM.push({
            valorReserva: valorReserva,
            quantidadeUnidadesPD: quantidadeUnidadesPD,
            data: new Date(data),
        });
        valorReserva += 16000000000;
        valorUnidadePM -= 0;
        quantidadeUnidadesPM = valorUnidadePM < 0 ? 0 : valorUnidadePM;
        populacaoBrasileira += 1;
        updateValues();
    }
}




        function somarAoCaixa() {
            if (!jogoIniciado) return;
            const lucrosPorEmpresaPAL = 1000000;
            const lucrosPorEmpresaLM = 99999999;
           
            const lucrosPorEmpresaPD = 500000;
           const lucrosPorEmpresaPM = 500000;
           

            valorReserva += (quantidadeUnidadesPAL * lucrosPorEmpresaPAL) + (quantidadeUnidadesLM * lucrosPorEmpresaLM) + (quantidadeUnidadesPD * lucrosPorEmpresaPD) + (quantidadeUnidadesPM * lucrosPorEmpresaPM) ;
            updateValues();
        }


        function toggleJogo() {
            const btnIniciarJogo = document.querySelector('.button');
            if (!jogoIniciado) {
                jogoIniciado = true;
                btnIniciarJogo.innerText = 'Pausar Jogo';
                intervalId = iniciarContagem();
            } else {
                jogoIniciado = false;
                btnIniciarJogo.innerText = 'Iniciar Jogo';
                clearInterval(intervalId);
            }
        }
        function iniciarContagem() {
            return setInterval(function () {
                if (podeAumentarLucro) {
                    somarAoCaixa();
                }
                
                
                data.setDate(data.getDate() + 1);
                
     // Atualiza a posição do Palmeiras a cada 3 dias
        diasInvestimentoPalmeiras++;
        if (diasInvestimentoPalmeiras >= 3) {
            diasInvestimentoPalmeiras = 0;
            posicaoCampeonato--;
            if (posicaoCampeonato < maxPosicao) {
                posicaoCampeonato = maxPosicao;
            }
        }

        // Adiciona 1 à quantidade de títulos a cada 30 dias
        if (data.getDate() === 30) {
            quantidadePALBRA++;
            quantidadePLIB++;
            quantidadePCOPA++;
        }           
                
                updateValues();
            }, 1000);
        }
    </script>
</body>
</html>

