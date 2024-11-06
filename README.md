# M5Stack-Snake | Just Fun

Este é um projeto de um jogo de cobrinha básico desenvolvido para o microcontrolador ESP32. O jogo é exibido em uma matriz de LEDs e controlado por um joystick analógico. Assim como o clássico jogo de Snake, o objetivo é guiar a cobrinha para coletar a comida e crescer sem colidir com as bordas ou com o próprio corpo.

Pré-requisitos
ESP32
Matriz de LEDs 8x8 (controlada pelo driver MAX7219)
Joystick analógico
Arduino IDE com suporte para ESP32
Instalação
Configure o ESP32 no Arduino IDE:

Abra o Arduino IDE.
Vá em Arquivo > Preferências.
Adicione https://dl.espressif.com/dl/package_esp32_index.json na seção URLs adicionais para gerenciadores de placas.
Vá em Ferramentas > Placa > Gerenciador de Placas e instale o pacote do ESP32.
Instale as bibliotecas necessárias:

Max72xxPanel: Biblioteca para controlar a matriz de LEDs com o driver MAX7219.
Adafruit GFX: Biblioteca de gráficos para controlar e desenhar na matriz.
Para instalar, vá em Sketch > Incluir Biblioteca > Gerenciar Bibliotecas e procure por cada uma para instalar.

Faça o clone do repositório e carregue o código:

Clone o repositório:

git clone https://github.com/seuusuario/snake-game-esp32.git
Conexões do Hardware
Joystick:

Conecte o eixo X a um pino analógico do ESP32 (exemplo: GPIO 34).
Conecte o eixo Y a outro pino analógico (exemplo: GPIO 35).
Conecte o SW (botão) a um pino digital (exemplo: GPIO 15).
Matriz de LEDs (8x8):

Conecte o CS (ou LOAD) ao pino GPIO 5 do ESP32.
Conecte os pinos de DATA e CLOCK aos respectivos pinos de comunicação SPI do ESP32.
Funcionamento do Jogo
Objetivo: Coletar a comida (um ponto brilhante na matriz) para aumentar o tamanho da cobra.
Movimento: Use o joystick para mover a cobra em quatro direções (cima, baixo, esquerda, direita).
Crescimento da Cobra: Cada vez que a cobra come a comida, seu tamanho aumenta.
Colisões: Quando a cobra atinge as bordas da matriz, ela reaparece no lado oposto.
Código
O código principal está estruturado da seguinte forma:

Leitura do Joystick: O joystick determina a direção da cobra.
Movimentação e Crescimento: A cobra se move e aumenta de tamanho ao comer a comida.
Atualização da Matriz: A matriz de LEDs exibe a posição atual da cobra e da comida.
Melhorias Sugeridas
Fim de jogo: Detectar colisões com o próprio corpo da cobra.
Níveis de dificuldade: Aumentar a velocidade conforme o jogador coleta mais comidas.
Pontuação: Exibir a pontuação na tela (ou, se possível, em um display adicional).
Contribuições
Sinta-se à vontade para contribuir com melhorias, novos recursos ou correções de bugs. Para contribuir:

Faça um fork do repositório.
Crie um branch para sua nova feature ou correção.
Envie um pull request descrevendo suas mudanças.
Licença
Este projeto é distribuído sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Captura de Tela
Caso tenha uma imagem ou vídeo do funcionamento do projeto, você pode incluir uma seção de captura de tela para mostrar o jogo em ação!

Espero que isso te ajude a configurar o repositório! Se precisar de mais alguma ajuda, é só avisar.
