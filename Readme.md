# **Desafio:**

## **Machine Learning na prática.**

### Para concluir esse desafio seguir os seguintes passos:

#### Primeiramente Criar uma conta gratuita na Microsoft Azure.

#### Após isso acessar o marketplace através da guia Serviços do Azure e clicar em Criar um recurso, dentro de criar recurso clicar Azure Machine Learning.

### **Dentro de Azure Machine Learning:**

#### Clicar na opção de criar novo workspace;

#### Preencher o formulário conforme as instruções dadas pela **Valéria Baptista** no video: **"Trabalhando com Machine Learning na Prática".**

---

## **Detalhes do Recurso:**

#### Assinatura: Azure ....

#### Grupo de recursos: LABAI-900

---

## **Detalhes do workspace**

#### **Nome:** laboratorioai900 (após colocar essa informação é adiciionado automaticamente: conta de armazenamento, cofre de chaves, application insights....abaixo da opção Região)

#### **Região:** East US

#### **Conta de armazenamento:**

#### **Cofre de chaves:**

#### **Application insights:**

#### **Registro de container:** Nenhum

---

## **Próximo passo:**

#### Clicar em examinar e criar

#### Verificar os dados para saber se estão corretos e depois dar prosseguimento;

#### Clicar em criar novamente;

#### Aguardar a criação e configuração.

## **Após a implantação concluída:**

#### Clicar em Ir para o recurso;

#### clicar em iniciar o estúdio ao final da página.

---

## **Dentro do Workspace:**

### Ir na barra lateral da esquerada e clicar em ML automatizado

#### Dentro de ML automatizado,clicar em novo trabalho automatizado.

### Em configurações básicas:

#### **Nome de trabalho:**mslearn-bike-automl

#### **Novo nome de experimento:**mslearn-bike-rental

#### **Descrição:** Aprendizado de máquina automatizado para previsão de aluguel de bicicletas.

### Após isso avançar!

## **Tipo de tarefa:**

#### Selecionar Regressão

## Em selecionar os dados:

### Clicar em criar ativo de dados

### **Nome de ativo de dados:** alugueldebicicletas

### **Descrição:** Dados históricos de aluguel de bicicletas

### **Tipo:** Tabular

### Avançar

### **Selecionar:** Fontes de Dados de Arquivos da Web

### Avançar

## https://aka.ms/bike-rentals

### Avançar

### **Configurações:**

### Formato do arquivo: Delimitado

### Delimitador: Virgula

### Codificação: UTF-8

### Cabeçalhos de coluna:Somente o primeiro

### Ignorar linhas: Nenhuma

## **Esperar o carregamento das informações**

### Após isso Avançar

## **Esquema**

### Deixar como está e clicar em avançar.

## **Examinar**

### Criar

## Aguardar a criação.

### Logo após, em selecionar dados: clicar em aluguel de bicicletas e depois em avançar.

## **Em configuração de tarefas:**

### Mudar coluna de destino para rentals(Integer)

### **Em configurações adicionais:**

#### Métrica primária: NormalizedRootMeanSquaredError

#### Desmarcar opções

#### Em modelos permitidos: Ticar RandomForest e LigthGBM

#### Clicar em Salvar.

## **Limites:**

### 3

### 3

### 3

### 0.085

### 15

### 15

### _HABILTAR ENCERRAMENTO ANTECIPADO_

## **Tipo de validação:** Divisão de validação de treinamento...

### Avançar

### **Computação:**

## Sem servidor

## Tipo de máquina virtual: CPU

## Tipo de máquina virtual: Dedicado

## Tamanho da máquina virtual

## Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.29/hr)

## Número de Instâncias: 1

### Avançar novamente.

## **Enviar trabalho de treinamento**

### Aguardar aproximadamente 15 minutos dependendo da configuração do seu computador

## **Após esse periodo,quando o trabalho for concluído,revisar o Melhor modelo na guia:**

#### Visão geral>>

#### Melhor modelo>>

#### Nome do algoritmo>>>(clicar nele).

### Selecionar métricas >>>

#### Gráficos residuais e predito_true se não estiverem selecionados também.

## **Implantação e teste do modelo**

### Na guia Modelo dentro do melhor modelo,selecionar implantar e usar serviço web para implantar o modelo com as configurações:

#### **Nome** : prever-aluguéis

#### **Descrição** : Prever aluguel de bicicletas

#### **Tipo de computação** : Instância de Contêiner do Azure

#### **Habilitar autenticação** : selecionado

### Aguardar o inicio da implantação

### Verificar o status de implantação do ponto de extremidade da previsão de aluguel que aparecerá na parte principal da pagina como running.

### Aguardar a implantção concluir

## **Testar**

### Selecionar ponto de extremidade

### Abrir em tempo real previsão de aluguel

## Em ponto de extremidade, em tempo real de previsao de aluguel, visualizar a guia Teste.

### Em dados de entrada para testar ponto de extemidade,substituir o modelo JSON pelos dados de entrada personalizados.

## **Utilizei**

### {

### "Inputs": {

### "data": [

### {

### "day": 1,

### "mnth": 1,

### "year": 2022,

### "season": 2,

### "holiday": 0,

### "weekday": 1,

### "workingday": 1,

### "weathersit": 2,

### "temp": 0.3,

### "atemp": 0.3,

### "hum": 0.3,

### "windspeed": 0.3

### }

### ]

### },

### "GlobalParameters": 1.0

### }

### Após isso testar, revisar os resultados que incluem numeros previstos com base nos recursos de entrada

### Meu resultado foi:

### {

### "Results": [ 1 item

### 0 : 354.2983225425056

### ]

### }
