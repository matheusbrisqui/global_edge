O problema de saúde abordado refere-se à gestão e administração adequada de doses de medicamentos. É comum que pacientes enfrentem desafios ao seguir corretamente os horários e dosagens prescritas, levando a lapsos na adesão ao tratamento. Essa falta de aderência pode comprometer a eficácia terapêutica e, consequentemente, a saúde geral do paciente. A não conformidade com as instruções de medicação pode resultar em consequências sérias, impactando negativamente os resultados dos tratamentos médicos.

A solução proposta consiste no desenvolvimento de um sistema de alerta e gestão de doses de medicamentos. Este sistema tem como objetivo principal fornecer lembretes precisos e personalizados aos usuários, garantindo a administração correta dos medicamentos. Além disso, visa permitir o acompanhamento remoto por cuidadores e médicos, proporcionando uma abordagem abrangente para assegurar a eficácia do tratamento.

O sistema utilizará conceitos matemáticos para analisar o comportamento das doses ao longo do tempo. Essa análise permitirá ajustar os lembretes de acordo com as necessidades individuais de cada paciente. A personalização dos lembretes incluirá variações nos horários de administração, dosagens específicas e outras instruções relevantes. Dessa forma, o sistema busca não apenas oferecer alertas, mas também adaptar-se às características únicas de cada usuário.

Ao incorporar a possibilidade de acompanhamento remoto, o sistema visa criar uma rede de suporte em torno do paciente. Cuidadores e médicos poderão monitorar a conformidade com o tratamento à distância, permitindo intervenções precoces se necessário. Isso não só melhora a adesão ao tratamento, mas também contribui para uma gestão mais eficaz da saúde do paciente.

Em resumo, a proposta apresenta uma abordagem abrangente e tecnologicamente avançada para resolver o desafio da gestão de doses de medicamentos, garantindo uma administração correta, eficaz e segura para melhorar os resultados dos tratamentos médicos.


Explicação do código:
O código é um programa para um dispositivo baseado no ESP32 que utiliza diversos módulos e APIs para realizar várias funcionalidades.
Inclusão de Bibliotecas:
-#include <Keypad.h>: Biblioteca para lidar com um teclado matricial.
-"Clock.h": Arquivo de cabeçalho (header) para a classe Clock, que parece ser usada para operações relacionadas ao relógio.
-"Weather.h": Arquivo de cabeçalho para a manipulação de informações meteorológicas.
-#include <WiFi.h>: Biblioteca para a comunicação Wi-Fi.
-#include <PubSubClient.h>: Cliente MQTT para comunicação com um broker MQTT.
-#include <HTTPClient.h>: Biblioteca para fazer requisições HTTP.
-#include <ArduinoJson.h>: Biblioteca para manipulação de dados JSON.
-#include <LiquidCrystal_I2C.h>: Biblioteca para controlar displays LCD com interface I2C.

Definições Iniciais:
-Define o endereço I2C, número de colunas e linhas para o display LCD.
-Define os tópicos MQTT para publicação e subscrição, bem como o ID MQTT.
-Configurações de Wi-Fi e MQTT.

Inicialização de Objetos:
-WiFiClient espClient;: Objeto para a comunicação Wi-Fi.
-PubSubClient MQTT(espClient);: Objeto para a comunicação MQTT.
-LiquidCrystal_I2C lcd(I2C_ADDR, LCD_COLUMNS, LCD_LINES);: Objeto para controlar o display LCD.
-Clock rtc(&lcd);: Objeto para operações relacionadas ao relógio.
-Keypad keypad = Keypad(makeKeymap(keys), rowPins, colPins, ROWS, COLS);: Objeto para lidar com o teclado matricial.

Funções de Controle de Tempo:
-enterTime(), enterAlarm(): Funções para configurar o relógio e o alarme.
-nextChar(), eraseChar(): Funções para manipular a entrada de dados.
-keyPadState0(), keyPadState1(), keyPadState2(): Funções que definem o comportamento do teclado em diferentes estados.

Funções de Configuração:
-initSerial(), initWiFi(), initMQTT(): Funções para inicializar a comunicação serial, Wi-Fi e MQTT.
-reconectWiFi(), `reconnectMQ

Para executar o código no simulador é somente esperar a internet ser concetada e clicar nas telas do teclado (que demoram um pouco para serem gravadas no cursor, talvez tenha que clicar mais de uma vez), além disso clicar nas telas conforme a legenda do lado, podendo alterar o horário, definir o alarme, entrar no modo silencioso ou concluir as alterações.

Link do wokwi: https://wokwi.com/projects/382210993722529793 
