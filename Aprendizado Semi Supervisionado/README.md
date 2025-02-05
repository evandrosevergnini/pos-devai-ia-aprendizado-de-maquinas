# **Inteligência Artificial e Aprendizado de Máquina**   
**Professor:** Francisco de Assis Boldt  
**Aluno:** Evandro Canal Severgnini  
**Data:** 04/02/2025  

---

# **Aprendizado Semi-Supervisionado com K-Means e Regressão Logística**  

Este notebook apresenta uma abordagem de **aprendizado semi-supervisionado**, combinando **agrupamento K-Means** e **Regressão Logística** para melhorar o desempenho do modelo de classificação em um conjunto de dados de dígitos escritos à mão.  

O objetivo principal é **usar um pequeno conjunto de dados rotulados** e **propagar os rótulos para outras amostras** usando um modelo de agrupamento.  

---

## **1. Objetivo do Notebook**  
O aprendizado semi-supervisionado é útil quando temos **poucos dados rotulados** e **muitos dados não rotulados**. Neste projeto, utilizamos:  
- **Agrupamento K-Means** para identificar padrões nos dados.  
- **Propagação de rótulos** para rotular automaticamente outras amostras.  
- **Regressão Logística** para treinar um modelo de classificação e avaliar o desempenho.  

---

## **2. Conjunto de Dados Utilizado**  
O conjunto de dados utilizado é o **Digits**, da biblioteca `sklearn.datasets`, que contém **imagens 8×8 de dígitos escritos à mão** (0 a 9).  

### **Divisão dos Dados**  
- **`imagens_treino` e `etiquetas_treino`**: Conjunto de treinamento (1.400 imagens).  
- **`imagens_teste` e `etiquetas_teste`**: Conjunto de teste (restante das imagens).  

---

## **3. Etapas do Notebook**  

### **3.1. Carregamento e Visualização dos Dados**  
- Carregamos o conjunto de dados Digits e o dividimos em treino e teste.  
- Visualizamos algumas imagens para entender os padrões dos dígitos.  

### **3.2. Treinamento de um Modelo Inicial com Poucos Dados**  
- Treinamos um modelo de **Regressão Logística** com apenas **50 amostras rotuladas**.  
- Avaliamos a acurácia no conjunto de teste.  

### **3.3. Agrupamento K-Means e Seleção de Amostras Representativas**  
- Aplicamos **K-Means** com **50 clusters** para encontrar grupos de dígitos semelhantes.  
- Selecionamos **as imagens mais representativas** de cada cluster.  

### **3.4. Propagação de Rótulos para Todo o Conjunto de Treinamento**  
- Propagamos os rótulos dos dígitos representativos para todas as imagens do conjunto de treino.  
- Treinamos um novo modelo de **Regressão Logística** com os rótulos propagados.  
- Avaliamos o desempenho no conjunto de teste.  

### **3.5. Refinamento da Propagação de Rótulos**  
- Selecionamos apenas as amostras **mais próximas dos centróides** para reduzir erros.  
- Criamos um **novo conjunto de treino parcialmente propagado**.  
- Treinamos novamente a Regressão Logística e comparamos os resultados.  

---

## **4. Principais Resultados**  

| Método | Dados de Treinamento | Acurácia no Teste |
|--------|----------------------|-------------------|
| Regressão Logística (50 amostras) | Apenas 50 amostras rotuladas | Baixa |
| Regressão Logística (propagação completa) | Todas as amostras rotuladas via K-Means | Melhor |
| Regressão Logística (propagação parcial) | Apenas amostras confiáveis | Melhor ainda |

O uso de **aprendizado semi-supervisionado** permitiu melhorar a acurácia sem precisar rotular manualmente todos os dados.  

---

## **5. Conclusão**  
Este notebook demonstra como podemos **aproveitar um pequeno conjunto de dados rotulados** e **propagar informações** de maneira eficiente usando **K-Means**.  

A abordagem **reduz a necessidade de rótulos manuais** e pode ser aplicada em diversos problemas onde a rotulação de dados é cara ou demorada.  

---

## **6. Tecnologias Utilizadas**  
- **Python 3**  
- **Scikit-Learn** (`sklearn`)  
- **NumPy**  
- **Matplotlib**  
