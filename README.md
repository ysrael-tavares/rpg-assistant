# [BDK] RPG ASSISTANT - BOT DE AUXILIO RPG

Seja bem-vindo ao manual do [BDK] RPG ASSISTANT.

> ## Adicione o bot ao seu servidor clicando [aqui](http://bit.ly/3uTC70q)

Este bot tem o intuito de deixar a jogatina a distância um pouco mais simples, no momento conta com apenas essas funções mas olha só, um spoiler, enquanto você lê isso outras funções estão sendo desenvolvidas, acompanhe nosso [Instagram](https://www.instagram.com/bdk_rpg/) para não perder nenhuma novidade.

Qualquer duvida, sugestão, reporte de bugs ou qualquer outro assunto não exite em entrar em contato na nossa [página](https://www.instagram.com/bdk_rpg/).

> ## Entre no nosso servidor no [Discord](https://discord.gg/XuNnEwYbx4)

## Menu Rápido

  - [Rolagem de dados](#rolagem-de-dados)
  - [Iniciativa](#iniciativa)
    - [Começando](#inicio-de-uma-disputa)
    - [Jogadores](#jogadores-entrando)
    - [Npcs](#npcs)
    - [Modificadores](#modificadores)
      - [Positivo](#modificador-positivo)
      - [Negativo](#modificador-negativo)
      - [Valor pré-definido](#valor-pré-definido)
    - [Batalha](#hora-da-briga)
  - [Controle de dano](#controle-de-dano)
    - [Causando dano](#causando-dano)
    - [Recebendo cura](#recebendo-cura)
    - [Desmaio/Morte](#o-participante-caiu)
    - [Retornando a luta](#voltando-a-luta)

---

## Rolagem de dados
[Topo](#bdk-rpg-assistant---bot-de-auxilio-rpg)

* Rolagem normal -> 1d20
* Rolagem com modificadores -> 1d20+5
* Rolagem com vantagem(Adicionar * no final) -> 1d20+5*
* Rolagem com desvantagem(Adicionar / no final) -> 1d20+5/
* Rolagem múltipla, basta adicionar a quantidade de vezes seguida de # -> 2#d20+5

>**IMPORTANTE: O número máximo de dados e faces permitidas é 100, acima disso o Bot ira considerar como 1.**

## Iniciativa
[Topo](#bdk-rpg-assistant---bot-de-auxilio-rpg)

### Inicio de uma disputa

O mestre deve enviar **iniciativa** e aparecerá a seguinte resposta:

```
Jogadores, rolem iniciativa!!!
```

### Jogadores entrando

Em seguida os jogadores enviam **ini** seguido do seu bônus e receberá o valor da sua iniciativa para aquela batalha

```
13 ⟷ [13]1d20 + 0 
```

### NPCS

Para adcionar um npc na batalha, basta inserir o nome dele após o 'ini'. Exemplo: **ini monstro**

```
Monstro: 18 ⟷  [18]1d20 + 0
```

### Modificadores

Os detalhes a seguir se aplicam a jogadores e npcs.

#### Modificador positivo

Se meu personagem possui +3 de bônus de iniciativa por exemplo, use **ini +3**.

```
12 ⟷ [9]1d20 + 3
```

#### Modificador negativo

Caso seja negativo adicionar o sinal - por exemplo, use **ini -3**

```
2 ⟷ [5]1d20 - 3
```

#### Valor pré-definido

Para usar um valor pré-definido de iniciativa ao invés de uma rolagem, baste inserir o valor entre (), exemplo: **ini (15)**

```
15 ⟷ Pré-definido
```

> Todos os casos acima são validos para NPCS, apenas use um '.' para separar, exemplo: **ini monstro.+3** ou **ini monstro.(10)**

```
Monstro: 18 ⟷  [15]1d20 + 3
```

### Hora da Briga

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

> Extra: Para ver o valor de Iniciativa dos participantes envie **batalha.i**

## Controle de dano
[Topo](#bdk-rpg-assistant---bot-de-auxilio-rpg)

Para controle de dano é usado o simbolo $ em conjunto com as informações da ordem de combate.

### Causando dano

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

### Recebendo cura

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

### O participante caiu

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

### Voltando a luta

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

[Topo](#bdk-rpg-assistant---bot-de-auxilio-rpg)
