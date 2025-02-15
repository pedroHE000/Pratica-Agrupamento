﻿# Pratica-Agrupamento
O **K-Means** é um algoritmo muito usado em aprendizado de máquina para agrupar dados semelhantes. Em vez de precisar de rótulos pré-definidos, ele encontra padrões por conta própria, organizando os dados em **K grupos** com base nas semelhanças entre eles. Ele é útil em várias áreas, como segmentação de clientes, análise de padrões e até processamento de imagens.  

### **Como o K-Means funciona na prática?**  
O algoritmo segue alguns passos simples:  

1. **Escolher o número de grupos (K)**: Antes de tudo, precisamos definir quantos clusters queremos. Esse número pode ser escolhido com base na análise dos dados ou usando métodos como o **método do cotovelo**.  
2. **Selecionar os centroides iniciais**: O algoritmo escolhe **K pontos aleatórios** dentro dos dados para servirem de pontos centrais dos clusters.  
3. **Atribuir cada ponto ao centroide mais próximo**: Aqui, cada dado é associado ao cluster cujo centro está mais perto. Para medir essa proximidade, geralmente usamos a **distância Euclidiana**:  

   \[
   d(A, B) = \sqrt{(x_B - x_A)^2 + (y_B - y_A)^2}
   \]

   Onde \( A \) e \( B \) são pontos no espaço e \( x, y \) são suas coordenadas.  
4. **Recalcular os centroides**: Depois de agrupar os dados, o centro de cada cluster é atualizado como a **média dos pontos dentro dele**:  

   \[
   C_j = \frac{1}{n} \sum_{i=1}^{n} X_i
   \]

   Onde \( C_j \) é o novo centroide do cluster \( j \) e \( X_i \) são os pontos pertencentes a ele.  
5. **Repetir até a convergência**: Os passos 3 e 4 se repetem até que os centroides não mudem mais ou até atingir um número máximo de iterações.  

### **Pontos fortes do K-Means**  
- **Rápido e eficiente** para grandes conjuntos de dados.  
- **Simples e intuitivo**, fácil de entender e implementar.  
- **Flexível**, podendo ser usado em diferentes tipos de problemas.  

### **Limitações e desafios**  
- **Escolher K pode ser complicado**: Se o número de clusters não for bem definido, o agrupamento pode não fazer sentido.  
- **Pontos iniciais importam**: Se os centroides forem mal escolhidos, o resultado pode ser ruim (por isso métodos como o K-Means++ melhoram essa parte).  
- **Sensível a outliers**: Valores muito distantes podem distorcer os grupos.  

### **Onde o K-Means é aplicado?**  
- **Empresas** usam para **segmentação de clientes**, agrupando consumidores com perfis semelhantes.  
- **Processamento de imagens**, como **compressão de cores** e segmentação de objetos.  
- **Agrupamento de documentos**, facilitando a organização de textos ou notícias por temas.  

Mesmo com algumas limitações, o **K-Means continua sendo um dos algoritmos mais populares** para clustering por sua simplicidade e eficiência.
