# PLC300 Sample Modbus (Node-Red)

Para fazer uma comunicação via Modbus primeiramente é necessário baixar um módulo de Modbus para o Node-Red. (Indico instalar o Node-Red 0.16.1 para seguir o passo a passo)

1º Clicar em “Manage Palette”

 ![alt tag](https://github.com/weg/plc300-sample-modbus/blob/master/img-readme/ManagePalette.jpg)

2º Clicar na Tab Install localizada na área de “Manage Palette”, buscar por Modbus e instalar a biblioteca node-red-contrib-modbus

 ![alt tag](https://github.com/weg/plc300-sample-modbus/blob/master/img-readme/InstallModule.jpg)

3º Adicionar nós de Modbus Getter e Write 
 
  ![alt tag](https://github.com/weg/plc300-sample-modbus/blob/master/img-readme/CreateFlow.jpg)

4º Configurar Nós criando uma configuração de “Server” que nada mais é que o endereço do slave modbus. Adicionar o tipo de leitura e os endereços a serem lidos.
  
  ![alt tag](https://github.com/weg/plc300-sample-modbus/blob/master/img-readme/ConfigNode.jpg)   ![alt tag](https://github.com/weg/plc300-sample-modbus/blob/master/img-readme/ConfigServer.jpg)

O <a target="_blank" href="https://github.com/weg/plc300-sample-modbus/blob/master/ModbusTCP.json">Flow</a> permite ler o Scan Cycle do PLC300 e escrever na DO2. Alterando os endereços modbus é possivel que se escreva ou leia qualquer endereço modbus mapeado no PLC300. 
Existem alguns outros nós modbus disponiveis nesse módulo que permitem que todos os itens configurados (tipo de leitura, endereço, quantidade de variaveis...) sejam passados dinamicamente via payload do nó.
