## Descrição
Primeiro trabalho para a disciplina SIN393. Este projeto implementa um pipeline de classificação de formas em imagens binarizadas usando o dataset **MPEG7 Modificado**. O objetivo é extrair características morfológicas das imagens e comparar o desempenho de três algoritmos de classificação: 
- **k-Nearest Neighbors (k-NN)**,
- **Support Vector Machine (SVM)**,
- **Random Forest (RF)**.

As principais etapas incluem:
1. Segmentação de imagens e extração de características.
2. Normalização dos dados.
3. Treinamento e validação de classificadores.
4. Avaliação do desempenho com matrizes de confusão e relatórios de classificação.

---

## Estrutura do Código
### 1. **Importação de Bibliotecas**
O código utiliza bibliotecas amplamente adotadas, como:
- `OpenCV` para manipulação e segmentação de imagens.
- `NumPy` para manipulação de dados numéricos.
- `Matplotlib` e `Seaborn` para visualização dos resultados.
- `scikit-learn` para pré-processamento, modelagem e avaliação.

### 2. **Função de Extração de Características**
A função `extract_features(image)` calcula as seguintes características morfológicas de contornos:
- **Área**: Quantidade de pixels no contorno.
- **Perímetro**: Comprimento do contorno.
- **Circularidade**: Métrica que avalia a similaridade com um círculo.

### 3. **Carregamento do Dataset**
As imagens do dataset são carregadas a partir do caminho especificado em `dataset_path`. Cada imagem é binarizada para facilitar a segmentação e a extração de características.

### 4. **Divisão dos Dados**
Os dados são divididos em:
- **Treinamento (50%)**,
- **Validação (20%)**,
- **Teste (30%)**.

### 5. **Normalização**
Os dados são normalizados com `StandardScaler` para padronizar os valores em torno de uma média 0 e desvio padrão 1.

### 6. **Classificadores**
Três classificadores são treinados e avaliados:
- **k-NN** (k = 3),
- **SVM** com kernel RBF,
- **Random Forest** com 100 árvores de decisão.

### 7. **Avaliação**
Os modelos são avaliados usando:
- **Matriz de Confusão** para análise visual de predições.
- **Relatório de Classificação** (`classification_report`) para métricas detalhadas como precisão, recall e F1-score.
- **Acurácia Média** para comparar os modelos.

---

## Resultados
Ao final, o script apresenta:
- Matriz de confusão para cada modelo.
- Métricas detalhadas no relatório de classificação.
- Acurácia média entre os modelos.

---

## Pré-requisitos
Certifique-se de que os seguintes pacotes estão instalados:
- `opencv-python`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Instale-os com o comando:
```bash
pip install opencv-python numpy matplotlib seaborn scikit-learn
```

---

## Como Usar
1. **Configure o caminho do dataset**:
   Altere a variável `dataset_path` para o caminho do dataset MPEG7 modificado.

2. **Execute o script**:
   ```bash
   python script.py
   ```

3. **Visualize os resultados**:
   O script exibirá gráficos e relatórios diretamente no terminal.

---

## Notas
- O dataset deve conter subpastas, onde cada subpasta representa uma classe.
- Verifique as configurações de normalização e parâmetros dos classificadores para adaptar ao seu caso de uso.

---

## Integrantes do projeto:
- João Matheus Rosano Rocha - 6031. **email**: joao.rosano@ufv.br
- Grazielle Stefane Cruz - 7021. **email**: grazielle.cruz@ufv.br

