# Trabalho Sobre Máquina de Estados Finitos

O Trabalho deverá ser implementado por uma máquina de estados finitos. Ou seja, deverá ser primeiramente projetado com um diagrama de estados, seguido de uma tabela de transição e por fim implementado no simulador [logisim-evolution](https://github.com/logisim-evolution/logisim-evolution). 

Trabalhos que utilizam circuitos 'prontos', como contadores, e os adaptam para resolver o problema, **serão desconsiderados**.

## Intersecção com Sensores de Tráfego

Projete uma máquina de estados para controlar os semáforos de uma intersecção.
Essa intesecção possui dois semáforos, S1 e S2; e cada rua possui sensores de tráfego, Ta e Tb. 
Cada sensor de tráfego ativa em nível alto caso tenha carros em sua pista (i.e., Ta=1).

![Semáforos](./imgs/traffic_intersection_sensors.png)

Caso o S1 esteja aberto (luz verde), e não tenha carros em Tb (i.e., Tb=0), então S1 permanece verde até que tenha carros em Tb (i.e., Tb=1).

O mesmo vale para o S2: Caso o S2 esteja aberto (luz verde), e não tenha carros em Ta (i.e., Ta=0), então S2 permanece verde até que tenha carros em Ta (i.e., Ta=1).

As luzes nos semáforos se alternam da maneira tradicional:

1. (S1=verde / S2=vermelho)
2. (S1=amarelo / S2=vermelho)
3. (S1=vermelho / S2=verde)
4. (S1=vermelho / S2=amarelo)
5. volta ao primeiro ciclo

### Entradas

A máquina de estados receberá três entradas: Ta, Tb e Clock. As luzes se alternaram de acordo com o Clock, sendo que a duração de cada estado pode ser de apenas uma batida do Clock.

## O que deve ser entrege

- Diagrama de estados
- Tabela de transição com escolha de flip-flops
- Simplificações das expressões booleanas
- Circuito implementado no [logisim-evolution](https://github.com/logisim-evolution/logisim-evolution)
- Relatório sucinto descrevendo seu projeto

Multiplexadores também podem ser utilizados para implementar funções lógicas. Porém, para uma função com N variáveis, apenas um **multiplexador com N-1 bits de seleção poderá ser usado**.

Após a entrega, o trabalho deverá ser apresentado de forma oral. Caso contrário, não será considerado.
