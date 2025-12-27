# Automação Industrial usando Machine Learning

- Um caso de estudo sobre bons desempenho de modelos de IA

<br>



## Dataset

[AI4I 2020](https://www.kaggle.com/datasets/stephanmatzka/predictive-maintenance-dataset-ai4i-2020)

- Dados sintéticos referentes à dados de fresadora, um tipo de máquina industrial que usa o corte rotativo da fresa para remover partes de uma peça, seja de metal ou de plástico, com o intuito de modelar a peça
- O dataset foi criado junto ao artigo "Explainable Artificial Intelligence for Predictive Maintenance Applications”, de Stephan Matzka

## Teste 4

- Referência ao notebook de [Abdelrahman Nabil](https://www.kaggle.com/code/abdonabil23/multi-classification-machine-failure-types-99)
- t4.ipynb
- Modelo salvo em modelo_salvo-teste4
- A fim de seguir a ideia do artigo que originou esse dataset, foi realizado mudanças no output para não somente identificar possíveis falhas, mas também mostrar qual tipo de falha
- Essa prática está associada ao conceito de Inteligência Artificial Explicada (XAI) que busca elucida a tomada de decisão que um modelo de aprendizagem de máquina possa ter, auxiliando na compreensão, nesse contexto, de que tipo de manutenção preditiva realizar
- Random Forest foi o que obteu melhor acurácia, não usei XGBoost, mas vale a pena testar futuramente

<br>
<img width="242" height="200" alt="image" src="https://github.com/user-attachments/assets/b0fd648e-3d7d-4149-9f05-aee4e4a42126" />
<br>
- Feito a avaliação de cada uma das inferências das 5 tipos de falhas existente no dataset

### TWF - tool wear failure (desgaste)

<img width="433" height="220" alt="image" src="https://github.com/user-attachments/assets/6358fcb6-6479-4bfd-a7f3-38a5898f474d" />

<img width="450" height="465" alt="image" src="https://github.com/user-attachments/assets/83bb1a4f-f574-4f34-98df-d7ed0de3f69d" />

<br>

### HDF - heat dissipation failure  (dissipação de calor)

<img width="440" height="223" alt="image" src="https://github.com/user-attachments/assets/1296e30f-2d4c-44ba-a4aa-9d0b7c0ed440" />

<img width="453" height="464" alt="image" src="https://github.com/user-attachments/assets/30252eb5-1746-47db-b5fc-e3140ddcdad8" />

### PWF - power failure (potência)

<img width="440" height="218" alt="image" src="https://github.com/user-attachments/assets/fffbba95-d8d0-421f-aff3-1ae9b2ce3717" />

<img width="451" height="458" alt="image" src="https://github.com/user-attachments/assets/3c11af54-92ec-4849-87ba-5e35ea4e2f3c" />

### OSF - overstrain failure (sobrecarga)

<img width="428" height="221" alt="image" src="https://github.com/user-attachments/assets/86461734-b3b0-4b6b-8fa8-cb6a9fd32c91" />

<img width="453" height="465" alt="image" src="https://github.com/user-attachments/assets/f6144544-1306-4ae6-b093-5c8aac0d531c" />

### RNF - random failures (aleatório)

<img width="436" height="221" alt="image" src="https://github.com/user-attachments/assets/58ba9b89-9a0d-4e83-a384-968e2e9569e1" />

<img width="452" height="463" alt="image" src="https://github.com/user-attachments/assets/ff376127-1120-471a-92cb-4fb2807122eb" />


## Teste 3

- Referência ao notebook de [Adil Ahmad](https://www.kaggle.com/code/damhalida/machine-failure-about99)
- t3.ipynb
- Simplificado o dataset a fim de considerar somente se a peça é falha (Classe 1) ou não falha (Classe 0)
- Os modelos salvos desse treinamento estão na pasta saved_models


### 1.xgboost

<img width="462" height="220" alt="image" src="https://github.com/user-attachments/assets/6ce8ce54-c658-4f8e-83d5-3bfd6971098e" />


<img width="489" height="390" alt="image" src="https://github.com/user-attachments/assets/e1e577b6-c631-4175-b6de-af7f22dd9e3a" />


### 2.random forest

<img width="461" height="199" alt="image" src="https://github.com/user-attachments/assets/621bc1fd-7be8-4eac-aa5c-7a1d72d431eb" />


<img width="489" height="390" alt="image" src="https://github.com/user-attachments/assets/e202b345-0c1c-4b80-b0cf-317f7eeff72f" />


### 3.knn 

<img width="455" height="216" alt="image" src="https://github.com/user-attachments/assets/acfbf5db-02da-4345-b43f-ae17e06d03c0" />


<img width="489" height="390" alt="image" src="https://github.com/user-attachments/assets/5db48f81-c770-4ad3-8f16-33762c21cbfc" />


### 4.svc    

<img width="459" height="196" alt="image" src="https://github.com/user-attachments/assets/5b73e653-0aa1-4854-b30e-09b61d05b3d5" />


<img width="489" height="390" alt="image" src="https://github.com/user-attachments/assets/0f0af974-095b-430a-9a35-e5f47a47fd94" />


### 5.logistic regression

<img width="457" height="194" alt="image" src="https://github.com/user-attachments/assets/aa76f2fd-97c1-4ddb-b569-464618995f13" />


<img width="489" height="390" alt="image" src="https://github.com/user-attachments/assets/f3a38c3c-9ab5-4fa0-a689-652b718095ce" />

### Comparativo

<img width="325" height="129" alt="image" src="https://github.com/user-attachments/assets/8dc0a62a-b66a-45e5-8bed-c174a9fe5fdd" />

## Considerações sobre os testes

### Colunas do dataset

'UDI', identificador único que varia de 1 a 10.000<br><br>

'Product ID', composto pelas letras L, M ou H para baixa (50% de todos os produtos), média (30%) e <br>
alta (20%) qualidades do produto, respectivamente, e um número de série específico para cada variante.<br><br>

'Type', apenas o tipo de produto L, M ou H da coluna 'Product ID'.<br><br>

'Air temperature [K]', gerada usando um processo de caminhada aleatória, posteriormente normalizada <br>
para um desvio padrão de 2 K em torno de 300 K<br><br>

'Process temperature [K]', gerada usando um processo de caminhada aleatória, normalizada para <br>
um desvio padrão de 1 K, somada à temperatura do ar mais 10 K<br><br>

'Rotational speed [rpm]', calculada a partir de uma potência de 2860 W, sobreposta com um ruído de distribuição normal<br><br>

'Torque [Nm]', os valores de torque são normalmente distribuídos em torno de 40 Nm com um desvio padrão de 10 Nm. Valores negativos<br><br>

'Tool wear [min]', As variantes de qualidade H/M/L adicionam 5/3/2 minutos de desgaste à ferramenta utilizada no processo<br><br>

'Machine failure', Informa se a ferramenta está falha (1) ou não(1)<br><br>

'TWF', Falha por desgaste da ferramenta<br><br>

'HDF', Falha por dissipação de calor<br><br>

'PWF', Falha de potência <br><br>

'OSF', Falha por sobrecarga<br><br>

'RNF', Falhas aleatórias<br><br>

### Utilização da técnica SMOTE

- Usado para balancear o conjunto de dados
- Smote cria amostras sintéticas
- Como ele faz isso?
<br>
1.Escolhe uma amostra da classe minoritária<br>
Exemplo: um ponto da classe TWF<br><br>

2.Encontra um vizinho próximo dessa mesma classe<br>
Outro ponto TWF parecido<br><br>

3.Desenha uma “linha” entre os dois pontos<br>
Entre ponto A e ponto B<br><br>

4.Cria um novo ponto no meio dessa linha<br>
Uma combinação dos dois<br><br>

### Modelos de Aprendizagem de Máquina utilizados
- Nos testes descritos aqui, foi feito um rol de treinamento com diferentes modelos e optado por escolher o melhor
- Quais modelos?

1.XGBoost
- Usa diversas árvores de decisão, treinando uma após a outra, sendo que cada árvore tenta corrigir os erros da anterior
- Várias árvores em série que corrigem erros

2.Random Forest
- Conjunto de árvores que tomam decisões independentes, há uma votação e a decisão que tiver o maior número de votos vence como valore de output
- Várias árvores independentes votando

3.KNN
- K-Nearest Neighbors
- Gera outputs baseado nos seus vizinhos, após o treinamento haverá agrupamentos de dados e a partir do input o modelo tenta identificar em qual conjunto eles são semelhantes, identificando assim a classificação do output
- Classificação por vizinhos

4.SVC
- Support Vector Classifier
- Cria um limite(vetor) que divide entre valores de uma classe e de outra ao colocar os dados em um plano cartesiano
- Separa classes com a melhor fronteira

5.Regressão Logística
- Estima a probabilidade de os dados de input pertencer a uma classe
- Modelo probabilístico

6.Gaussian Naïve Bayes
- Uma adaptação do modelo Naïve Bayes, assume que as features são indepedentes, trabalha em torno de probabilidades de ser ou não determinado output
- Modelo probabilístico

7.Árvores de Decisão
- Divide dados em ramos, features que fazem mais sentido de explicar determinada classificação são usados para criar um conjunto de decisões utilizadas para gerar o modelo treinado
- Usa regras “se/então”

### Porque não usar Redes Neurais?
- Dados tabulares(em formato de tabelas) são mais adequados para modelos de aprendizado de máquina tradicionais
- Redes Neurais são mais apropriados quando os dados tem estruturas complexas, como treinar um modelo para entender quais pixels está um gato, por exemplo
- Dados não-lineares, que apresentam comportamentos que fogem de uma função linear podem ser bons valores para serem treinado com Random Forest e XGBoost


## Referências

- S. Matzka, "Explainable Artificial Intelligence for Predictive Maintenance Applications”
- [Adil Ahmad](https://www.kaggle.com/damhalida)
- [Abdelrahman Nabil](https://www.kaggle.com/code/abdonabil23/multi-classification-machine-failure-types-99)
- [Ilya Palkin - Илья Палкин](https://www.kaggle.com/rander447)
- [Daniel Smyth](https://www.pexels.com/de-de/foto/industrie-herstellung-maschine-werkzeug-10406128/)
