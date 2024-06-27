# Sistema de Gerenciamento de Eventos

## Informações Gerais sobre o Projeto
Este projeto é um sistema de gerenciamento de eventos que permite a organização, registro e monitoramento de eventos e participantes. O objetivo principal é fornecer uma interface para gerenciar eventos, participantes e check-ins, além de gerar relatórios sobre a participação e engajamento dos participantes.

## Objetivos
- Facilitar o gerenciamento de eventos e participantes.
- Permitir o registro de check-ins em eventos.
- Fornecer relatórios detalhados sobre a participação e engajamento dos participantes.

## Funcionalidades Principais
- Adicionar, listar e remover eventos.
- Adicionar, listar e remover participantes.
- Registrar check-ins de participantes em eventos.
- Gerar relatórios de participação por evento, frequência por participante e estatísticas de engajamento.

## Informações sobre as Classes e suas Relações
### Classes Principais
- **Evento**: Representa um evento, contendo nome, data e uma lista de participantes.
- **Participante**: Representa um participante de um evento, herda da classe abstrata Pessoa.
- **CheckIn**: Representa um check-in de um participante em um evento, contendo as informações do participante, evento e data do check-in.
- **GerenciadorEventos**: Gerencia a lista de eventos, permitindo adicionar, remover e listar eventos. Implementa a interface `Organizavel` para organizar eventos por nome ou data.
- **GerenciadorParticipantes**: Gerencia a lista de participantes, permitindo adicionar, remover e listar participantes.
- **GerenciadorCheckIns**: Gerencia a lista de check-ins, permitindo registrar novos check-ins e listar check-ins por evento ou participante.
- **Persistencia**: Classe responsável por salvar e carregar dados de eventos, participantes e check-ins em arquivos de texto.
- **Relatorio**: Classe responsável por gerar relatórios de participação, frequência e engajamento.
- **Organizavel**: Interface que define métodos para organizar eventos por nome e por data.

### Relações entre as Classes
- **Agregação**: A classe `Evento` agrega `Participante`, pois um evento pode ter vários participantes, mas os participantes existem independentemente dos eventos.
- **Composição**: A classe `CheckIn` é composta por `Participante` e `Evento`, pois um check-in não faz sentido sem um participante e um evento.
- **Associação**: As classes `GerenciadorEventos`, `GerenciadorParticipantes` e `GerenciadorCheckIns` estão associadas às classes que gerenciam (`Evento`, `Participante` e `CheckIn` respectivamente).
- **Implementação de Interface**: A classe `GerenciadorEventos` implementa a interface `Organizavel`, o que a obriga a fornecer implementações dos métodos `organizarPorNome` e `organizarPorData`.

## Como Executar o Projeto
### Requisitos
- Java JDK 8 ou superior
- IDE de sua preferência (Eclipse, IntelliJ, etc.)

### Passos para Executar
1. Clone o repositório para sua máquina local:
   ```sh
   git clone https://github.com/luangl/eventos_java.git
2. Importe o projeto em sua IDE.
3. Compile e execute a classe Main que contém o método main.
4. Instruções Adicionais
5. Certifique-se de que os arquivos eventos.txt, participantes.txt e checkins.txt estejam no diretório raiz do projeto, pois serão usados para carregar e salvar dados.

## Uso do ChatGPT
### O ChatGPT foi utilizado no desenvolvimento deste projeto para:

- Fornecer sugestões e exemplos de implementação.
- Auxiliar na estruturação da lógica de classes e métodos.

## Referências e Recursos
- Documentação Oficial do Java
- Guia de Boas Práticas de Programação
- ChatGPT para assistência na implementação do projeto.
