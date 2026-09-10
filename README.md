# MEMORUSH — Jogo de Memória e Velocidade

Projeto desenvolvido para a unidade curricular de **Levantamento de Requisitos**, do curso Técnico em Desenvolvimento de Sistemas — SESI/SENAI Itapeva.

## Identificação

| **Aluno** | Melissa Gomes Gouvêa |
| --- | --- |
| **Turma** | 2°B |
| **Professor** | Rafael Ribas |
| **Data** | 31/08/2026 |

## Sobre o projeto

O **Memo Rush** é um jogo de memória, atenção e velocidade que criei com a ideia de transformar uma atividade simples de memorização em uma experiência mais **divertida, desafiadora e dinâmica**.

Durante cada rodada, o jogador precisa memorizar uma sequência de elementos apresentada na tela durante alguns segundos. Depois que a sequência desaparece, uma pergunta é apresentada e o jogador precisa identificar a resposta correta.

O jogo foi desenvolvido para que a dificuldade aumente progressivamente. Conforme o jogador avança pelas fases, as sequências ficam maiores, o tempo para memorização diminui, as perguntas ficam mais complexas e os elementos utilizados são selecionados de forma mais variada e imprevisível.

Com o desenvolvimento do projeto, o jogo ganhou diversas funcionalidades, como diferentes modos de jogo, sistema de vidas, níveis, XP, combos, missões diárias, conquistas, estatísticas, ranking, personalização, temas e armazenamento dos dados no navegador.

## Como o jogo funciona

Em cada rodada, uma sequência de elementos é apresentada na tela.

O jogador precisa memorizar:

- A ordem dos elementos;
- A posição de cada elemento;
- A presença ou ausência de determinados elementos;
- A quantidade de vezes que um elemento aparece;
- A relação entre elementos da sequência.

Depois do tempo de memorização, a sequência desaparece e uma pergunta é apresentada com algumas opções de resposta.

O jogador deve responder corretamente e, sempre que possível, com rapidez.

Os acertos podem gerar:

- Pontos;
- Combo;
- XP;
- Progresso de fase;
- Progresso em missões;
- Progresso em conquistas.

Os erros possuem consequências de acordo com o modo de jogo escolhido.

## Sistema de vidas

O Memo Rush possui um sistema real de vidas que influencia diretamente o andamento da partida.

Nos modos que utilizam vidas, o jogador começa normalmente com **3 vidas**.

Sempre que uma pergunta é respondida incorretamente:

**Erro = perda de 1 vida.**

A quantidade de vidas é atualizada tanto internamente na lógica do jogo quanto visualmente na interface.

Por exemplo:

**3 vidas → 2 vidas → 1 vida → 0 vidas**

Ao chegar a **0 vidas**, a partida é encerrada e o jogador recebe o feedback de **Fim de Jogo**.

O jogo também impede que a quantidade de vidas fique negativa e não remove vidas quando o jogador acerta uma pergunta.

O sistema possui regras específicas de acordo com cada modo:

- **Modo Clássico** — utiliza 3 vidas e perde 1 vida a cada erro;
- **Modo Infinito** — mantém o sistema de vidas enquanto as fases continuam;
- **Sudden Death** — possui apenas 1 vida, portanto um único erro encerra a partida;
- **Modo Treino** — não remove vidas;
- **Time Attack** — utiliza sua própria mecânica baseada no tempo.

## Sistema de dificuldade progressiva

Uma das principais melhorias do Memo Rush é o aumento real da dificuldade conforme o jogador avança.

A dificuldade não depende apenas da quantidade de fases. O jogo aumenta gradualmente a quantidade de informações que o jogador precisa memorizar e reduz o tempo disponível para isso.

A progressão inicial foi definida da seguinte forma:

| Fase | Elementos | Tempo de memorização |
| --- | ---: | ---: |
| 1 | 3 | 5 segundos |
| 2 | 4 | 4,5 segundos |
| 3 | 5 | 4 segundos |
| 4 | 6 | 3,8 segundos |
| 5 | 7 | 3,5 segundos |
| 6 | 8 | 3,2 segundos |
| 7 | 9 | 3 segundos |
| 8 | 10 | 2,8 segundos |
| 9 | 11 | 2,6 segundos |
| 10 | 12 | 2,5 segundos |

Após a fase 10, a dificuldade continua aumentando gradualmente, adicionando mais elementos e/ou reduzindo o tempo de memorização de forma progressiva.

Além disso, perguntas mais difíceis passam a aparecer conforme o jogador avança.

Assim, quanto maior a fase:

**→ Mais elementos para memorizar**

**→ Menos tempo para memorizar**

**→ Perguntas mais complexas**

**→ Maior variedade de palavras**

**→ Sequências mais imprevisíveis**

## Informações apresentadas durante a partida

Para que o jogador consiga perceber claramente a evolução da dificuldade, o HUD apresenta informações relacionadas à fase atual.

Entre elas estão:

- Fase atual;
- Pontuação;
- Combo;
- Quantidade de elementos;
- Nível de dificuldade;
- Tempo de memorização;
- Vidas restantes;
- Cronômetro, quando utilizado pelo modo.

Por exemplo:

```text
FASE 5
ELEMENTOS: 7
DIFICULDADE: MÉDIA
TEMPO DE MEMORIZAÇÃO: 3.5s
VIDAS: ❤️ ❤️ 🖤