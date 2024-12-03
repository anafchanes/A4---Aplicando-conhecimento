# Sistema de Gestão de Energia com IoT

Este projeto implementa um sistema de gestão de energia utilizando IoT (Internet das Coisas), integrando sensores e atuadores para monitoramento e controle automatizado do consumo de energia em ambientes urbanos. O sistema utiliza sensores para medir condições ambientais (temperatura, umidade, luminosidade) e otimizar o uso de dispositivos como iluminação e ventilação, promovendo maior eficiência energética.

## Componentes

- **ESP32** (Microcontrolador)
- **Sensor DHT22** (Temperatura e Umidade)
- **Sensor BH1750** (Luminosidade)
- **Relé de Estado Sólido (SSR)** (Controle de dispositivos de alta potência)
- **Broker MQTT** (Comunicação entre os dispositivos e plataforma IoT)
- **Plataforma IoT** (ThingSpeak ou Ubidots)

## Funcionalidade

Este sistema monitora em tempo real o ambiente através de sensores e ajusta o uso de dispositivos (ventiladores, iluminação, etc.) com base nas condições ambientais. Os dados são enviados via MQTT para um broker, permitindo que o usuário monitore o sistema remotamente através de uma plataforma IoT (como ThingSpeak ou Ubidots).

### Exemplo de Aplicação:
1. **Controle Automatizado de Iluminação:**
   O sensor de luminosidade (BH1750) ajusta automaticamente o brilho da iluminação conforme a luz natural disponível.
   
2. **Controle de Climatização:**
   O sensor de temperatura e umidade (DHT22) controla o acionamento de ventiladores ou sistemas de climatização com base nas condições ambientais.

3. **Monitoramento Remoto:**
   Os dados de consumo de energia e condições ambientais são enviados à nuvem via MQTT, permitindo o monitoramento remoto e a automação dos sistemas.

## Objetivos do Projeto

- **Otimização do Consumo de Energia:** Automatizar o controle de iluminação e climatização com base em sensores ambientais.
- **Monitoramento Remoto:** Facilitar o acesso aos dados de consumo e condições ambientais através de uma interface web ou aplicativo.
- **Sustentabilidade:** Contribuir para a redução de desperdícios energéticos e a promoção de ambientes mais sustentáveis.

## Como Funciona

1. **Sensoriamento:** 
   - O sensor DHT22 coleta dados de temperatura e umidade, enquanto o sensor BH1750 monitora a intensidade da luz ambiente.
   
2. **Controle de Dispositivos:** 
   - O ESP32 processa os dados dos sensores e aciona o relé de estado sólido para ligar ou desligar dispositivos de alta potência (como ventiladores e lâmpadas) conforme necessário.
   
3. **Comunicação MQTT:** 
   - Os dados dos sensores são enviados ao broker MQTT, que os publica em tópicos específicos para visualização remota na plataforma IoT escolhida.

## Exemplos de Aplicações

1. **Automação de Iluminação:** 
   O sistema ajusta automaticamente o brilho da iluminação com base na luminosidade detectada, economizando energia quando há luz natural suficiente.

2. **Controle de Temperatura e Umidade:** 
   O sistema monitora as condições ambientais e aciona ventiladores ou sistemas de aquecimento/resfriamento quando os valores ultrapassam os limites predefinidos.

## Materiais e Métodos

### Componentes de Hardware:

- **ESP32:** Microcontrolador central para controle e comunicação.
- **DHT22:** Sensor de temperatura e umidade.
- **BH1750:** Sensor de luminosidade.
- **Relé SSR:** Atuador para controle de dispositivos de alta potência.

### Software:

- **Arduino IDE:** Para programação do ESP32.
- **Broker MQTT (Mosquitto):** Para gerenciamento da comunicação entre dispositivos.
- **Plataforma IoT (ThingSpeak ou Ubidots):** Para visualização e controle remoto.

### Métodos:

1. **Montagem do Circuito:** Conecte os sensores e o relé ao ESP32, configurando a comunicação via MQTT.
2. **Programação:** Escreva o código no Arduino IDE para configurar a leitura dos sensores e o controle do relé.
3. **Monitoramento Remoto:** Utilize a plataforma IoT para visualizar os dados em tempo real e controlar os dispositivos conectados.

## Como Configurar

1. **Instale o Arduino IDE** e adicione a biblioteca ESP32.
2. **Conecte os sensores e o relé** ao ESP32 conforme o diagrama de montagem.
3. **Implemente o código Arduino** para configurar os sensores e a comunicação MQTT.
4. **Configure o broker MQTT** e conecte-o à sua plataforma IoT preferida.
5. **Teste a automação** de dispositivos e o monitoramento remoto dos dados.
