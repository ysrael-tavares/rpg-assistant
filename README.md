# [BDK] RPG ASSISTANT - BOT DE AUXILIO RPG 🤖

Seja bem-vindo ao manual do [BDK] RPG ASSISTANT.

Este bot tem o intuito de deixar a jogatina a distância um pouco mais simples, no momento conta com apenas essas funções mas olha só, um spoiler, enquanto você lê isso outras funções estão sendo desenvolvidas, acompanhe nosso [Instagram](https://www.instagram.com/bdk_rpg/) para não perder nenhuma novidade.

Qualquer duvida, sugestão, reporte de bugs ou qualquer outro assunto não exite em entrar em contato no nossa [página](https://www.instagram.com/bdk_rpg/).

## Rolagem de dados 🎲

* Rolagem normal -> 1d20
* Rolagem com modificadores -> 1d20+5
* Rolagem com vantagem(Adicionar * no final) -> 1d20+5*
* Rolagem com desvantagem(Adicionar / no final) -> 1d20+5/
* Rolagem múltipla, basta adicionar a quantidade de vezes seguida de # -> 2#d20+5

>**IMPORTANTE: O número máximo de dados e faces permitidas é 100, acima disso o Bot ira considerar como 1.**

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
>**IMPORTANTE: Não é necessário incluir o + caso seu bônus seja positivo.**
Caso seja negativo adicionar o sinal -, por exemplo: !-3
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

Para declarar um participante como incapacitado na batalha basta enviar o mesmo comando de dano apenas substituindo o dano por 'ko' (2$ko).
```
Jogador 3 foi um(a) guerreiro(a) que um dia sonhou com a paz.

Ordem de combate:

1 - Monstro 1 (0) 
2 - Jogador 3 (0) (K.O)
3 - Monstro 2 (2) 
4 - Monstro 3 (0) 
5 - Jogador 2 (0) 
6 - Jogador 1 (0)
```

>Bônus: Quando um participante é incapacitado, uma frase ou brincadeira é enviada enfatizando o ocorrido.

Mas a morte nem sempre é o fim, você sempre pode contar com aquele clérigo gente boa que vai te prestar socorro e em casos mais extremos, trazer você de volta a vida. Nessa ocasião basta substituir o dano/cura por 'revive' (2$revive).

```
Jogador 3 deve se fazer uma pergunta: 'Estou com sorte?' 

Ordem de combate:

1 - Monstro 1 (0) 
2 - Jogador 3 (0) 
3 - Monstro 2 (2)
4 - Monstro 3 (0) 
5 - Jogador 2 (0) 
6 - Jogador 1 (0)
```

>Bônus: Quando um participante é revivido, uma frase ou brincadeira é enviada enfatizando o ocorrido.
