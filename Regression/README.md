# **Inteligência Artificial e Aprendizado de Máquina**   
**Professor:** Francisco de Assis Boldt  
**Aluno:** Evandro Canal Severgnini  
**Data:** 04/02/2025  

---

# **Predição de Preço das Casas em Boston**

Esse notebook ensina como funciona a Regressão Linear, que é uma forma de prever valores com base em dados. Para isso, ele usa um conjunto de dados chamado Boston Housing, que contém informações sobre bairros e preços de casas. O objetivo é encontrar uma fórmula matemática que relacione essas informações com o preço das casas.

---

## O que esse projeto faz?**
✔ **Carrega os dados** de preços de casas em Boston.  
✔ **Analisa os dados** com estatísticas e gráficos.  
✔ **Treina um modelo de regressão linear** para prever os preços.  
✔ **Avalia o modelo usando o Erro Médio Quadrático (MSE).**  

## **1. Carregando os Dados  (`fetch_openml`)**  
A primeira coisa que o código faz é **carregar o conjunto de dados Boston Housing**.  

- **Os números são guardados em `X`**, que contém informações como:  
  - Renda média da população no bairro  
  - Índice de criminalidade  
  - Número médio de quartos por casa  
  - Distância até o centro da cidade  
- **Os preços das casas são armazenados em `y`**, que é o que queremos prever.  

**Pergunta:** Será que existe uma relação entre essas informações e o preço das casas?   

---

## **2. Explorando os Dados com Gráficos**  
Para entender os dados, o código cria **gráficos de dispersão** (pontos) que mostram como cada informação se relaciona com o preço das casas.  

Um dos gráficos mais importantes mostra a **relação entre a variável "LSTAT" (percentual de pessoas de baixa renda no bairro) e o preço das casas**. Isso porque bairros com renda menor geralmente têm casas mais baratas.  

📊 **Conclusão:** Os dados sugerem que conforme a variável **LSTAT** aumenta, o preço das casas diminui.  

---

## **3. Criando um Modelo Simples de Regressão Linear**  
Agora, o código cria um modelo matemático que tenta **desenhar uma reta que melhor represente os dados**.  

A fórmula desse modelo é:  

\[
\text{preço} = a \times \text{LSTAT} + b
\]

Onde:  
- **`a`** controla a inclinação da reta  
- **`b`** indica onde a reta começa no eixo do preço  

**Primeiro, o código escolhe valores aleatórios para `a` e `b` e desenha essa reta sobre o gráfico.**  

Mas esses valores ainda **não são os melhores**! O próximo passo é **encontrar `a` e `b` corretos** para que a reta se aproxime ao máximo dos pontos reais.  

---

## **4. Como Saber se o Modelo Está Bom? (Métricas de Erro)**  
Para medir se um modelo faz boas previsões, usamos algumas **métricas de erro**, que mostram **o quanto o modelo errou** ao prever o preço das casas.  

O código calcula 3 tipos de erro:  

1. **Erro Médio Absoluto (MAE)** → Mede a diferença média entre os preços reais e os preços previstos.  
2. **Erro Quadrático Médio (MSE)** → Eleva os erros ao quadrado para evitar números negativos.  
3. **Raiz do Erro Quadrático Médio (RMSE)** → Faz a raiz quadrada do MSE para que o erro fique na mesma escala dos preços reais.  

**Se o erro for muito grande, significa que nosso modelo precisa ser ajustado!**  

---

## **5. Melhorando o Modelo com Gradiente Descendente**  
O código usa um método chamado **Gradiente Descendente** para **ajustar os valores de `a` e `b`** e melhorar as previsões.  

### **Como o Gradiente Descendente funciona?**  
- O modelo **faz previsões** com valores iniciais de `a` e `b`.  
- Calcula **o erro** (diferença entre os valores reais e os previstos).  
- **Ajusta `a` e `b` aos poucos** para diminuir esse erro.  
- **Repete esse processo várias vezes** até encontrar os melhores valores.  

**Isso faz com que a reta se aproxime dos pontos reais do gráfico!**  

O código ainda **desenha um gráfico 3D** que mostra como o erro muda conforme ajustamos `a` e `b`.  

---

## **6. Comparando com um Modelo Pronto (`sklearn`)**  
Depois de construir nosso próprio modelo de regressão linear, o código usa a biblioteca **`sklearn`**, que já tem um modelo pronto.  

Esse modelo:  
- **Aprende os melhores valores de `a` e `b` sozinho**.  
- **Faz previsões rapidamente**.  
- **Calcula o erro automaticamente**.  

**O código compara nosso modelo com o do `sklearn` para ver se os resultados são parecidos!**  

---

## **Conclusão**
- **O notebook mostrou como criar um modelo de regressão linear do zero!**  
- **Usamos gráficos para entender os dados e prever preços de casas.**  
- **Aprendemos a medir o erro do modelo e a melhorá-lo com Gradiente Descendente.**  
- **Por fim, comparamos nossa implementação com um modelo profissional do `sklearn`.**  

Agora **sabemos como prever valores com Regressão Linear!** 
