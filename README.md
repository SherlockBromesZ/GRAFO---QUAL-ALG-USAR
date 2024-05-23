# GRAFOS: QUAL ALGORITMO USAR?

## DJIKSTRA
- **Objetivo:** Encontrar o *menor caminho* entre um *início* e um *fim* (vértice de início e vértice final).
- **Características:**
  - Grafos com pesos não negativos.

**Exemplo de uso:**
- Sistemas de navegação GPS para encontrar a rota mais curta entre dois pontos.
- Redes de computadores para encontrar o caminho mais eficiente entre servidores.

---

## FLOYD-WARSHALL
- **Objetivo:** Encontrar os *menores caminhos* entre *todos os pares de vértices*.
- **Características:**
  - Grafos com pesos negativos, mas sem ciclos negativos.

**Exemplo de uso:**
- Análise de rotas entre todas as cidades de um país.
- Encontrar a menor distância entre todos os pares de servidores em uma rede.

---

## BELLMAN-FORD
- **Objetivo:** Encontrar o *menor caminho* (igual ao Dijkstra) para grafos com pesos negativos.
- **Características:**
  - Grafos com pesos negativos.
  - Detectar ciclos negativos.

**Exemplo de uso:**
- Análise de rotas em redes de transporte com custos variáveis.
- Encontrar caminhos mais curtos em redes de computadores com custos variáveis.

---

## ÁRVORE GERADORA MÍNIMA (Prim e Kruskal)
- **Objetivo:** Encontrar a *árvore geradora mínima* (MST) de um grafo.
- **Características:**
  - Grafos não direcionados e conectados.

### Algoritmo de Prim
- Melhor para grafos densos.
- Usa uma estrutura de dados de fila de prioridade.

### Algoritmo de Kruskal
- Melhor para grafos esparsos.
- Usa a estrutura de dados de união-find.

**Exemplo de uso:**
- Planejamento de redes de distribuição de energia elétrica.
- Construção de redes de comunicação.

---

## ORDENAÇÃO TOPOLÓGICA (Algoritmo de Kahn)
- **Objetivo:** Ordenar os vértices de um grafo acíclico direcionado (DAG) de forma que para cada aresta \( u \to v \), \( u \) venha antes de \( v \).
- **Características:**
  - Grafos direcionados acíclicos (DAG).

**Exemplo de uso:**
- Planejamento de tarefas com dependências.
- Compilação de código-fonte com dependências entre módulos.

---

## BFS (Busca em Largura)
- **Objetivo:** Encontrar o *caminho mais curto* entre dois vértices em um grafo sem pesos (não ponderado).
- **Características:**
  - Explora todos os vértices de um grafo.

**Exemplo de uso:**
- Encontrar a menor quantidade de movimentos para resolver um quebra-cabeça.
- Verificar a conectividade de um grafo.

---

## RESUMO
- **Dijkstra:** Caminho mais curto de um ponto para todos os outros (pesos não negativos).
- **Floyd-Warshall:** Caminho mais curto entre todos os pares (pesos negativos permitidos, mas sem ciclos negativos).
- **Prim/Kruskal:** Árvore geradora mínima.
- **Kahn:** Ordenação topológica.
- **Bellman-Ford:** Caminho mais curto de um ponto para todos os outros (pesos negativos permitidos).
- **BFS:** Caminho mais curto em grafos não ponderados.

---

Vou fornecer exemplos de problemas que podem ser encontrados na Olimpíada Brasileira de Informática (OBI) e que podem ser resolvidos com cada um dos algoritmos mencionados.

### Algoritmo de Dijkstra
**Problema:**
Você é responsável por encontrar a rota mais curta entre duas cidades em um país. As cidades são conectadas por estradas com diferentes comprimentos. Dado um mapa com \( N \) cidades e \( M \) estradas, encontre a menor distância entre a cidade \( A \) e a cidade \( B \).

**Entrada:**
- \( N \) (número de cidades)
- \( M \) (número de estradas)
- \( A \) e \( B \) (cidades de origem e destino)
- Lista de \( M \) estradas, cada uma com três inteiros \( u \), \( v \) e \( d \) (estrada entre \( u \) e \( v \) com distância \( d \))

**Saída:**
- Menor distância entre \( A \) e \( B \)

**Exemplo:**
```plaintext
Entrada:
5 6
1 5
1 2 2
1 3 4
2 3 1
2 4 7
3 5 3
4 5 1

Saída:
7
```

### Algoritmo de Floyd-Warshall
**Problema:**
Você tem um mapa de cidades conectadas por estradas com diferentes comprimentos. Dado um mapa com \( N \) cidades e \( M \) estradas, encontre a menor distância entre todas as cidades.

**Entrada:**
- \( N \) (número de cidades)
- \( M \) (número de estradas)
- Lista de \( M \) estradas, cada uma com três inteiros \( u \), \( v \) e \( d \) (estrada entre \( u \) e \( v \) com distância \( d \))

**Saída:**
- Matriz \( N \times N \) com as menores distâncias entre todas as cidades

**Exemplo:**
```plaintext
Entrada:
4 4
1 2 3
2 3 1
3 4 2
4 1 5

Saída:
0 3 4 6
3 0 1 3
4 1 0 2
5 2 3 0
```

### Árvore Geradora Mínima (Prim e Kruskal)
**Problema:**
Você é responsável por construir uma rede de comunicação entre várias cidades. Dado um mapa com \( N \) cidades e \( M \) estradas, encontre a menor rede de comunicação que conecte todas as cidades.

**Entrada:**
- \( N \) (número de cidades)
- \( M \) (número de estradas)
- Lista de \( M \) estradas, cada uma com três inteiros \( u \), \( v \) e \( d \) (estrada entre \( u \) e \( v \) com custo \( d \))

**Saída:**
- Custo total da menor rede de comunicação

**Exemplo:**
```plaintext
Entrada:
4 5
1 2 1
1 3 4
2 3 2
2 4 5
3 4 3

Saída:
7
```

### Ordenação Topológica (Algoritmo de Kahn)
**Problema:**
Você precisa organizar as tarefas de um projeto. Cada tarefa tem dependências que precisam ser concluídas antes de começar a próxima. Dado um conjunto de tarefas e suas dependências, encontre uma ordem válida para realizar todas as tarefas.

**Entrada:**
- \( N \) (número de tarefas)
- \( M \) (número de dependências)
- Lista de \( M \) dependências, cada uma com dois inteiros \( u \) e \( v \) (tarefa \( u \) deve ser concluída antes da tarefa \( v \))

**Saída:**
- Ordem válida das tarefas

**Exemplo:**
```plaintext
Entrada:
6 6
1 2
1 3
2 4
3 4
4 5
4 6

Saída:
1 2 3 4 5 6
```

### Algoritmo de Bellman-Ford
**Problema:**
Você é responsável por encontrar a rota mais curta entre duas cidades em um país. As cidades são conectadas por estradas com diferentes comprimentos, incluindo estradas com custos negativos. Dado um mapa com \( N \) cidades e \( M \) estradas, encontre a menor distância entre a cidade \( A \) e a cidade \( B \).

**Entrada:**
- \( N \) (número de cidades)
- \( M \) (número de estradas)
- \( A \) e \( B \) (cidades de origem e destino)
- Lista de \( M \) estradas, cada uma com três inteiros \( u \), \( v \) e \( d \) (estrada entre \( u \) e \( v \) com custo \( d \))

**Saída:**
- Menor distância entre \( A \) e \( B \)

**Exemplo:**
```plaintext
Entrada:
5 6
1 5
1 2 2
1 3 4
2 3 1
2 4 7
3 5 3
4 5 -2

Saída:
6
```

### Busca em Largura (BFS)
**Problema:**
Você precisa encontrar a menor quantidade de movimentos para resolver um quebra-cabeça. Dado um tabuleiro \( N \times N \) com obstáculos, encontre o menor caminho entre a posição inicial e a posição final.

**Entrada:**
- \( N \) (tamanho do tabuleiro)
- \( M \) (número de obstáculos)
- \( x_0 \), \( y_0 \) (posição inicial)
- \( x_f \), \( y_f \) (posição final)
- Lista de \( M \) obstáculos, cada um com dois inteiros \( x \) e \( y \)

**Saída:**
- Menor quantidade de movimentos entre a posição inicial e a posição final

**Exemplo:**
```plaintext
Entrada:
5 3
0 0
4 4
1 1
2 2
3 3

Saída:
8
```
