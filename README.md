# K-Means com Penguins (Seaborn) 

Projeto prático de **clusterização com K-Means** usando o dataset **penguins** do `seaborn`.  
O objetivo é explorar agrupamentos nos dados, comparar a visualização antes e depois da padronização e aplicar o algoritmo em três cenários: **base mista**, **fêmeas** e **machos**.

## Objetivos do trabalho

✅ Verificar e preparar o dataset para o K-Means (remoção de valores ausentes e exclusão de variáveis categóricas)  
✅ Explorar os dados com análise descritiva e visualizações  
✅ Padronizar features numéricas com `StandardScaler`  
✅ Treinar `KMeans` com `n_clusters = 3` e inicialização `k-means++`  
✅ Visualizar clusters e centróides em gráficos de dispersão  
✅ Discutir aplicações reais de clusterização

## Dataset

Base: `penguins` do pacote `seaborn` (medições físicas de pinguins na Antártica).

Principais colunas utilizadas (numéricas):
- `bill_length_mm` (comprimento do bico)
- `bill_depth_mm` (profundidade do bico)
- `flipper_length_mm` (comprimento da barbatana)
- `body_mass_g` (massa corporal)

Colunas removidas para o K-Means:
- `species` e `island` (categóricas)
- `sex` foi usada apenas para separar os subconjuntos e depois removida das features

## Metodologia

### 1) Preparação e limpeza
- Carregamento do dataset `penguins`
- Remoção de valores ausentes (`dropna`)
- Seleção apenas das variáveis numéricas para o modelo

### 2) Análise exploratória
- Visualizações com `pairplot` para inspecionar separação por espécie
- Observação de sobreposição entre grupos na base mista
- Comparação com as bases separadas por sexo

### 3) Padronização
- Padronização das features com `StandardScaler`
- Visualização dos dados padronizados em múltiplos gráficos de dispersão

### 4) Treinamento do K-Means
- Treino do modelo em cada base (misto, feminino, masculino)
- Configurações:
  - `n_clusters=3`
  - `init='k-means++'`
  - `random_state=42`

### 5) Visualização dos clusters
- Gráficos com pontos coloridos por cluster
- Marcação dos centróides
- Pairplots com os clusters como rótulo para comparar padrões

## Principais entregas

📌 Notebook com:
- EDA e pairplots por espécie
- Padronização e comparação visual
- Treinamento do K-Means nos três subconjuntos
- Visualização de clusters e centróides
- Texto final com aplicações práticas de clusterização

## Como executar

### Opção 1) Rodar localmente

1. Clone o repositório:
```bash
git clone https://github.com/SEU_USUARIO/SEU_REPO.git
cd SEU_REPO
