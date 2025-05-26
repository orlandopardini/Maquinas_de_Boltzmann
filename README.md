# Modelagem com Restricted Boltzmann Machines (RBMs)

As **Boltzmann Machines** são modelos probabilísticos baseados em energia, utilizados para aprender representações e padrões ocultos em conjuntos de dados. Elas consistem em unidades visíveis (dados de entrada) e unidades ocultas (features latentes), conectadas de maneira simétrica.

## Diferença entre Boltzmann Machine Padrão e RBM

### Boltzmann Machine (BM)
- Conexões **entre todas as unidades** (inclusive entre unidades ocultas e entre visíveis).
- Mais poderosa, mas **muito difícil de treinar** devido ao grande número de conexões e interdependência.

### Restricted Boltzmann Machine (RBM)
- Conexões **apenas entre camadas visíveis e ocultas**, **sem conexões internas em uma mesma camada**.
- Treinamento mais eficiente, usando o algoritmo de **Contrastive Divergence (CD)**.
- Muito usada para **redução de dimensionalidade, pré-treinamento de redes profundas e sistemas de recomendação**.

### Funcionamento Intuitivo
Imagine que você tem avaliações de filmes feitas por usuários. A RBM aprende **quais filmes são parecidos** com base nas avaliações, mesmo que o usuário nunca tenha assistido o filme, permitindo **recomendações personalizadas**.

---

## 📂 Estrutura dos Notebooks e Scripts

### 1. `RBM1_Recomendacao_Orlando.ipynb`
**📌 Tarefa:** Sistema de recomendação baseado em preferências binárias  
**📚 Dataset:** Matriz de usuários x filmes (ou produtos)  
**🔍 Destaques:**
- Treinamento da RBM para prever itens não avaliados
- Representação binária das preferências
- Recomendações com base em padrões latentes

### 2. `RBM2_Reducao_dimensionalidade_Orlando.ipynb`
**📌 Tarefa:** Redução de dimensionalidade em dados de alta dimensão  
**📚 Dataset:** Dados com múltiplas variáveis de entrada  
**🔍 Destaques:**
- Compressão de dados com RBM
- Visualização do espaço latente
- Comparação antes/depois da redução

### 3. `RBM3_exemplo_Orlando.py`
**📌 Tarefa:** Implementação didática de uma RBM do zero  
**📚 Dataset:** Exemplo sintético (matriz simples)  
**🔍 Destaques:**
- Construção manual da RBM (sem bibliotecas externas)
- Algoritmo de treinamento passo a passo (Contrastive Divergence)
- Funções para reconstrução de visíveis e geração de amostras (`daydream`)

---

## 📈 Métricas e Avaliação

As RBMs são avaliadas por:

- **Erro de reconstrução** (diferença entre entrada e reconstrução)
- **Capacidade de generalização** (ex: recomendações corretas)
- **Visualização dos pesos e ativações ocultas**

---

## ⚙️ Técnicas Utilizadas

- Algoritmo **Contrastive Divergence**
- Ativação com função logística (sigmoide)
- Normalização dos dados binários
- Amostragem estocástica via Gibbs Sampling
"""
