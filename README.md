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
