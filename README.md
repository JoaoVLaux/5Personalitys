## Documentação para o Projeto de Clusterização de Personalidade

### Introdução
Este projeto tem como objetivo agrupar indivíduos com base em seus traços de personalidade usando os algoritmos KMeans e Spectral Biclustering. Os traços de personalidade são extraídos de um conjunto de dados contendo vários atributos psicológicos. O processo de clusterização divide os indivíduos em grupos que compartilham características de personalidade semelhantes.

### Pré-requisitos
Certifique-se de ter instalado:
- Python (3.x)
- pandas
- scikit-learn
- matplotlib

### Estrutura do Projeto
O projeto consiste em um único script JupyterNotebook chamado `personality_clustering`.

### Fluxo de Trabalho do Projeto
1. **Carregamento de Dados**: 
    - O conjunto de dados é carregado usando o pandas a partir do arquivo `data-final.csv`, assumindo que ele está no mesmo diretório.
2. **Limpeza de Dados**:
    - Colunas do índice 50 ao 110 são removidas para reduzir a dimensionalidade.
    - Linhas com todos os valores zero são removidas do conjunto de dados.
3. **Clusterização usando KMeans**:
    - A clusterização KMeans é realizada com 5 clusters.
    - Cada indivíduo é atribuído a um dos 5 clusters de personalidade.
4. **Transformação de Dados**:
    - Um novo DataFrame é criado contendo os valores médios dos traços de personalidade para cada cluster.
5. **Visualização**:
    - Os traços de personalidade de cada cluster são plotados para inspeção visual.
6. **Clusterização usando Spectral Biclustering**:
    - O Spectral Biclustering é aplicado ao conjunto de dados com 5 clusters.
    - Os indivíduos são rotulados com seus respectivos números de cluster.
7. **Transformação de Dados para Spectral Biclustering**:
    - Outro DataFrame é gerado com os valores médios dos traços de personalidade para cada cluster obtido do Spectral Biclustering.
8. **Visualização para Spectral Biclustering**:
    - Semelhante à clusterização KMeans, os traços de personalidade de cada cluster obtido do Spectral Biclustering são visualizados.

### Uso
1. Certifique-se de que o conjunto de dados `data-final.csv` está no mesmo diretório que o script.
2. Execute o script.
3. O script irá produzir visualizações dos clusters de personalidade obtidos dos algoritmos KMeans e Spectral Biclustering.

### Conclusão
Este projeto fornece insights sobre a clusterização de indivíduos com base em seus traços de personalidade. As visualizações ajudam a entender as características de cada cluster de personalidade, o que pode ser valioso para diversas aplicações, como marketing direcionado ou análise psicológica.
