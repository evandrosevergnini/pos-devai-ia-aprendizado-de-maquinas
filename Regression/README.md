# **Inteligência Artificial e Aprendizado de Máquina**   
**Professor:** Francisco de Assis Boldt  
**Aluno:** Evandro Canal Severgnini  
**Data:** 04/02/2025  

---

# **🏠 Predição de Preço das Casas em Boston**

Este projeto analisa um conjunto de dados sobre casas em Boston e usa **Regressão Linear** para prever seus preços.  

---

## **📌 1. O que esse projeto faz?**
✔ **Carrega os dados** de preços de casas em Boston.  
✔ **Analisa os dados** com estatísticas e gráficos.  
✔ **Treina um modelo de regressão linear** para prever os preços.  
✔ **Avalia o modelo usando o Erro Médio Quadrático (MSE).**  

---

## **📥 2. De onde vêm os dados?**
Os dados vêm de um arquivo CSV disponível publicamente:  

🔗 **[Boston Housing Dataset](https://raw.githubusercontent.com/selva86/datasets/master/BostonHousing.csv)**  

O dataset contém **506 registros** e **14 colunas**, incluindo:  
- **Características das casas**, como número de quartos e idade.  
- **Condições do bairro**, como taxa de criminalidade.  
- **Preço médio das casas (`medv`)**, que queremos prever.  

---

## **📊 3. Como analisamos os dados?**
### 🔹 **3.1 Estatísticas gerais**
Antes de treinar o modelo, verificamos:  
✔ Número total de registros e colunas.  
✔ Valores ausentes (se houver).  
✔ Estatísticas como média, mediana e desvio padrão.  

### 🔹 **3.2 Histogramas**
Criamos um **histograma** para visualizar a distribuição dos preços das casas.  

🔽 **Exemplo de gráfico - Histograma do Preço das Casas**  

📌 **O que percebemos?**  
- A maioria das casas custa **menos de 30 mil dólares**.  
- Existem **valores extremos**.  

### 🔹 **3.3 Scatter Plots**
Criamos **gráficos de dispersão** para ver como cada variável influencia o preço das casas.  

🔽 **Exemplo de gráfico - Relação entre Número de Quartos e Preço**  

📌 **O que percebemos?**  
- Casas com **mais quartos tendem a ser mais caras**.  
- Bairros com **alta taxa de criminalidade** têm casas mais baratas.  

### 🔹 **3.4 Heatmap de Correlação**
Criamos um **heatmap** para ver quais variáveis têm mais impacto no preço.  

🔽 **Exemplo de gráfico - Correlação entre Variáveis**  

📌 **O que percebemos?**  
- **Mais quartos = Preços mais altos**.  
- **Bairros mais pobres = Preços mais baixos**.  

---

## **🏗 4. Como treinamos o modelo?**
Usamos **Regressão Linear**, um modelo que tenta encontrar padrões entre os preços e as variáveis.  

### **Passos:**
1️⃣ **Dividimos os dados** → 80% treino, 20% teste.  
2️⃣ **Treinamos o modelo** usando os dados de treino.  
3️⃣ **Fazemos previsões** para os dados de teste.  
4️⃣ **Medimos o erro médio das previsões (MSE)**.  

---

## **📈 5. Como avaliamos o modelo?**
Usamos o **Erro Médio Quadrático (MSE)**, que mede o erro médio das previsões.  

📌 **Resultado obtido:**  
**Erro Médio Quadrático (MSE): 21.89**  

📌 **O que isso significa?**  
- Quanto **menor o MSE**, **melhor** o modelo.  
- Um erro **de 21.89** indica que as previsões têm **um erro médio razoável**.  

---

## **📉 6. Como visualizamos as previsões?**
Criamos um gráfico que compara os **valores reais** com as **previsões do modelo**.  

🔽 **Exemplo de gráfico - Preços Reais vs. Preços Preditos**  

📌 **Como interpretar?**  
✔ Se os pontos estão **próximos da linha vermelha**, o modelo fez boas previsões.  
❌ Se os pontos estão **muito espalhados**, o modelo teve dificuldades.  

---

## **✅ 7. Conclusão**
✔ O modelo conseguiu **fazer previsões razoáveis**, mas pode ser melhorado.  
✔ Algumas variáveis, como **número de quartos**, têm forte impacto no preço.   

---

## **📌 O que melhoramos?**
✅ **Linguagem mais simples e acessível** para qualquer aluno.  
✅ **Explicação clara** sobre **o que os gráficos e métricas significam**.  
✅ **Removemos o R²**, como solicitado.  
✅ **Tudo aparece na tela**, sem caixas de código.  
