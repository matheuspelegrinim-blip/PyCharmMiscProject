# Previsão de Atrasos em Entregas de E-commerce (Shipping Data)

Este projeto aplica técnicas de Análise Exploratória de Dados (EDA) e Machine Learning para prever se um produto enviado por uma empresa de e-commerce chegará no prazo ou sofrerá atrasos, com base em características logísticas, peso, custos e avaliações de clientes.

---

## Visão Geral do Projeto
A gestão de prazos de entrega é vital para a satisfação do cliente. Utilizando um conjunto de dados de transporte (*shipping data*), este projeto investiga quais fatores mais impactam os atrasos e constrói modelos preditivos capazes de antecipar problemas logísticos.

### Etapas do Pipeline:
1. **Análise Exploratória (EDA):** Identificação de padrões por bloco de armazém, modo de envio, peso do produto, descontos e custos.
2. **Engenharia de Atributos (*Feature Engineering*):** Criação de novas métricas (como a razão custo/peso) e codificação de variáveis categóricas usando *One-Hot Encoding*.
3. **Modelagem Preditiva:** Treinamento e avaliação de algoritmos como **Decision Tree**, **Random Forest** (com otimização de hiperparâmetros) e **Regressão Logística**.
4. **Tratamento de Desbalanceamento:** Aplicação da técnica **SMOTE** para equilibrar as classes no conjunto de treino.

---

## Principais Descobertas
* **Peso vs. Atraso:** Produtos mais pesados tendem a apresentar uma taxa média de atraso superior em comparação aos mais leves.
* **Descontos:** Descontos elevados possuem forte correlação com o comportamento de compra e as rotas de envio.
* **Importância das Variáveis:** Através do *Random Forest*, descobriu-se que o **Peso do Produto (`Weight_in_gms`)** e o **Desconto Oferecido (`Discount_offered`)** são os dois fatores mais determinantes para prever se uma entrega atrasará.

---

## Tecnologias Utilizadas
* **Python** 
* **Pandas & NumPy** (Manipulação e estruturação de dados)
* **Matplotlib** (Visualização gráfica)
* **Scikit-Learn** (Modelos de Machine Learning e métricas)
* **Imbalanced-Learn (SMOTE)** (Balanceamento de dados)

---

## Resultados dos Modelos
* **Árvore de Decisão Básica:** ~64.09% de acurácia
* **Decision Tree (com Limitação de Profundidade):** ~68.05% de acurácia
* **Random Forest Otimizada:** ~67.77% a 67.95% de acurácia com forte ganho de *Recall* para a classe de atrasos.
