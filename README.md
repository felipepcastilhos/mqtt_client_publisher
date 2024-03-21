# IMPORTANT

- 'Initial commit' tendo HOST como localhost; \
- Se desejado conectar a um broker MQTT em um endereço IP específico em vez de 'localhost', basta substituir o valor do campo HOST pelo endereço IP desejado:
  mqtt_broker_configs = {
    "HOST": "192.xxx.x.xxx", # Endereço IP do broker MQTT
    "PORT": 1883, # Porta do broker MQTT
    "CLIENT_NAME": "publisher", # Nome do cliente MQTT
    "KEEPALIVE": 15, # Tempo de vida da conexão em segundos
    "TOPIC": "/msgs" # Tópico MQTT para publicação de mensagens
  }
  OBS.: o endereço IP especificado pode não estar acessível por várias razões como:

  - Se o broker MQTT estiver em uma rede diferente do dispositivo onde o código está sendo executado;
  - Certifique-se de que o firewall permita a comunicação na porta utilizada pelo broker MQTT (por padrão, a porta é 1883 para conexões não seguras e 8883 para conexões seguras).
  - Se o broker MQTT não estiver em execução no endereço IP especificado, a conexão falhará. Verifique se o broker MQTT está em execução e acessível na rede.
  - Problemas de conectividade de rede ou endereço IP incorreto, entre outos;

- Considerando a utilização do referente script "mqtt_client_pub.py", o contexto de que o sistema terá comos dispositivos:
  - Dispositivo "cliente_publisher" um software/script em python sendo rodado em um IP de um computador;
  - Por outro lado como um dispositivo "cliente_subscriber" um dispositivo IoT com ESP32.
