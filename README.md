# Projeto de Previsão com Azure Machine Learning

## Descrição

Este projeto foi desenvolvido como parte do desafio da DIO com o objetivo de criar um modelo de previsão utilizando o Azure Machine Learning e documentar todas as etapas do processo.

## Objetivo

* Criar um modelo de Machine Learning.
* Implantar o modelo como um serviço.
* Configurar os pontos de extremidade (Endpoints).
* Documentar todo o processo.
* Disponibilizar os arquivos no GitHub.

---

## Tecnologias Utilizadas

* Azure Machine Learning
* Azure AI Services
* Git
* GitHub

---

## Etapas do Projeto

### 1. Criação do Workspace

Foi criado um Workspace no Azure Machine Learning para centralizar todos os recursos do projeto.

### 2. Criação do Modelo

Utilizando o Automated Machine Learning, foi configurado um experimento de previsão com o conjunto de dados escolhido.

Durante essa etapa foram definidos:

* Tipo de tarefa: Previsão (Forecasting)
* Dataset
* Coluna alvo
* Métrica de avaliação
* Configurações de treinamento

### 3. Treinamento

Após a configuração, o Azure treinou diversos modelos automaticamente e selecionou aquele que apresentou melhor desempenho.

### 4. Implantação

O melhor modelo foi implantado em um Endpoint Online para realizar previsões em tempo real.

### 5. Testes

Foram realizados testes utilizando o endpoint criado para verificar o funcionamento do modelo.

---

## Estrutura do Repositório

```
/
├── README.md
├── endpoint.json
└── imagens/
    ├── workspace.png
    ├── treinamento.png
    ├── endpoint.png
```

---

## Arquivo endpoint.json

O arquivo `endpoint.json` contém a configuração do endpoint implantado no Azure Machine Learning.

{
  "name": "previsao-endpoint",
  "authMode": "key",
  "location": "brazilsouth",
  "properties": {
    "scoringUri": "https://<endpoint>.inference.ml.azure.com/score",
    "provisioningState": "Succeeded"
  }
}

## Resultados

O modelo foi treinado e implantado com sucesso, permitindo realizar previsões através do endpoint disponibilizado pelo Azure.

---

## Aprendizados

Durante este desafio foi possível aprender:

* Criação de Workspaces no Azure
* Automated Machine Learning
* Treinamento automático de modelos
* Implantação de modelos
* Configuração de Endpoints
* Organização de projetos utilizando Git e GitHub

---

## Autor

Ricardo Farias
