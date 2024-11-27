# Sistema de Aluguel de Meios de Transporte

Este é um sistema de gerenciamento para o aluguel de meios de transporte individuais, como bicicletas, patinetes, patins e skates, utilizando o padrão de projeto **Abstract Factory** para criar diferentes tipos de transportes, diferenciando-os pelo tipo de propulsão (movido a bateria ou esforço humano).

## Funcionalidades

- **Movidos a Bateria**: Patinetes elétricos e bicicletas elétricas.
- **Movidos pelo Esforço Humano**: Bicicletas convencionais, patins e skates.

O sistema oferece uma interface para criar os diferentes tipos de transportes e gerenciar seu uso, oferecendo uma maneira flexível e extensível de trabalhar com diferentes tipos de transportes.

## Arquitetura

### **Padrão Abstract Factory**
- Utiliza o padrão **Abstract Factory** para criar transportes com diferentes categorias de propulsão (bateria ou esforço humano).
- O sistema possui fábricas específicas para cada categoria de transporte, que garantem a criação de instâncias dos transportes corretos.

### **Interfaces e Classes**
- **Transport**: Interface que define os métodos comuns para todos os meios de transporte.
- **ElectricTransport** e **HumanPoweredTransport**: Interfaces específicas para os tipos de transporte (elétrico e movido por esforço humano), que estendem a interface `Transport`.
- **Classes Concretas**: Implementações de transportes específicos:
  - **ElectricScooter**: Patinete elétrico.
  - **ElectricBike**: Bicicleta elétrica.
  - **Bicycle**: Bicicleta convencional.
  - **RollerSkates**: Patins.
  - **Skateboard**: Skate.

### **Fábricas**
- **TransportFactory**: Fábrica abstrata para criar os transportes.
- **ElectricTransportFactory**: Fábrica concreta para criar transportes movidos a bateria.
- **HumanPoweredTransportFactory**: Fábrica concreta para criar transportes movidos pelo esforço humano.

## Como Rodar o Sistema

### Pré-requisitos

- **Java 8 ou superior**
- **IDE de sua preferência (IntelliJ IDEA, Eclipse, etc.)**

### Passos para Executar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/TransportFactory.git
