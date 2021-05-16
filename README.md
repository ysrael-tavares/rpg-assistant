# [BDK] RPG ASSISTANT - BOT DE AUXILIO RPG 🤖

## Rolagem de dados 🎲

* Rolagem normal -> 1d20
* Rolagem com modificadores -> 1d20+5
* Rolagem com vantagem(Adicionar * no final) -> 1d20+5*
* Rolagem com desvantagem(Adicionar / no final) -> 1d20+5/
* Rolagem múltipla, basta adicionar a quantidade de vezes seguida de # -> 2#d20+5

## Iniciativa

Inicio de uma disputa o mestre deve enviar 'iniciativa'.
```
Jogadores, rolem iniciativa!!!
```
Em seguida os jogadores enviam '!' seguido do seu bônus e receberam o valor da sua iniciativa para aquela batalha
```
13 ⟷ [13]1d20 + 0 
```
Se meu personagem possui +3 de bônus de iniciativa, por exemplo !3
```
12 ⟷ [9]1d20 + 3
```
Caso seja negativo adicionar o sinal '-', por exemplo: !-3
```
2 ⟷ [5]1d20 - 3
```
Depois de todos participantes rolarem suas iniciativas basta enviar 'batalha' para ver a ordem de combate e o dano sofrido de cada participante
```
Ordem de combate:

1 - Monstro 1 (0) 
2 - Jogador 3 (0) 
3 - Monstro 2 (0) 
4 - Monstro 3 (0) 
5 - Jogador 2 (0) 
6 - Jogador 1 (0)
```

## Controle de dano ⚔️

Para controle de dano é usado o simbolo $ em conjunto com as informações da ordem de combate.

Para causar dano a um participante da batalha deve inserir a posição dele que é a primeira coluna do exemplo:

Para causar 5 de dano ao Monstro 2, basta enviar no chat 3$5.

```
Monstro 2 sofreu 5 de dano!

Ordem de combate:

1 - Monstro 1 (0) 
2 - Jogador 3 (0) 
3 - Monstro 2 (5) 
4 - Monstro 3 (0) 
5 - Jogador 2 (0) 
6 - Jogador 1 (0)
```

De forma semelhante para cura, devendo apenas adicionar o valor negativo (3$-3).

```
Monstro 2 recuperou 3 pontos de vida!

Ordem de combate:

1 - Monstro 1 (0) 
2 - Jogador 3 (0) 
3 - Monstro 2 (2) 
4 - Monstro 3 (0) 
5 - Jogador 2 (0) 
6 - Jogador 1 (0)
```

## Frases de ko
## Frases de renascimento
