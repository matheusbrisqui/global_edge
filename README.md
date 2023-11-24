O problema de saúde abordado refere-se à gestão e administração adequada de doses de medicamentos. É comum que pacientes enfrentem desafios ao seguir corretamente os horários e dosagens prescritas, levando a lapsos na adesão ao tratamento. Essa falta de aderência pode comprometer a eficácia terapêutica e, consequentemente, a saúde geral do paciente. A não conformidade com as instruções de medicação pode resultar em consequências sérias, impactando negativamente os resultados dos tratamentos médicos.

A solução proposta consiste no desenvolvimento de um sistema de alerta e gestão de doses de medicamentos. Este sistema tem como objetivo principal fornecer lembretes precisos e personalizados aos usuários, garantindo a administração correta dos medicamentos. Além disso, visa permitir o acompanhamento remoto por cuidadores e médicos, proporcionando uma abordagem abrangente para assegurar a eficácia do tratamento.

O sistema utilizará conceitos matemáticos para analisar o comportamento das doses ao longo do tempo. Essa análise permitirá ajustar os lembretes de acordo com as necessidades individuais de cada paciente. A personalização dos lembretes incluirá variações nos horários de administração, dosagens específicas e outras instruções relevantes. Dessa forma, o sistema busca não apenas oferecer alertas, mas também adaptar-se às características únicas de cada usuário.

Ao incorporar a possibilidade de acompanhamento remoto, o sistema visa criar uma rede de suporte em torno do paciente. Cuidadores e médicos poderão monitorar a conformidade com o tratamento à distância, permitindo intervenções precoces se necessário. Isso não só melhora a adesão ao tratamento, mas também contribui para uma gestão mais eficaz da saúde do paciente.

Em resumo, a proposta apresenta uma abordagem abrangente e tecnologicamente avançada para resolver o desafio da gestão de doses de medicamentos, garantindo uma administração correta, eficaz e segura para melhorar os resultados dos tratamentos médicos.


Este código é destinado a um dispositivo baseado no ESP32, incorporando vários módulos e APIs para realizar diversas funcionalidades. 

O propósito geral do código é criar um dispositivo que gerencie doses de medicamentos, fornecendo alertas personalizados e permitindo o acompanhamento remoto por meio de diversos componentes.

O código inclui a utilização de módulos específicos, como um transistor para controlar um buzzer piezo, um level shifter para um display LCD, e estabelece conexões com APIs de tempo e clima.

Diversas bibliotecas são incorporadas, como Keypad, WiFi, PubSubClient, e LiquidCrystal_I2C. Além disso, são utilizadas APIs para obter informações de tempo e clima.

As configurações e a inicialização envolvem a definição de parâmetros como tópicos MQTT e credenciais de Wi-Fi. Também são inicializados objetos para facilitar a comunicação, como WiFiClient para Wi-Fi, PubSubClient para MQTT, LiquidCrystal_I2C para o display LCD, um objeto Clock para operações relacionadas ao relógio, e um objeto Keypad para lidar com a entrada do teclado matricial.

Funções específicas são implementadas para configuração do relógio e do alarme, manipulação da entrada de dados do teclado, e controle do estado do dispositivo.

No loop principal, o código verifica e reconecta Wi-Fi e MQTT se necessário. Simula dados de temperatura e umidade (a serem substituídos por dados reais), publica esses dados em um tópico MQTT e aguarda um intervalo de tempo antes de repetir o processo.

Para executar o código no simulador é somente esperar a internet ser concetada e clicar nas telas do teclado (que demoram um pouco para serem gravadas no cursor, talvez tenha que clicar mais de uma vez), além disso clicar nas telas conforme a legenda do lado, podendo alterar o horário, definir o alarme, entrar no modo silencioso ou concluir as alterações.

Link do wokwi: https://wokwi.com/projects/382210993722529793 
