# 🔍 Sistema de Auditoria e Análise de Vendas

## 📝 Descrição do Projeto

Este projeto consiste em um algoritmo de auditoria de dados voltado para o monitoramento e validação de registros de vendas. O objetivo principal é identificar automaticamente anomalias, discrepâncias e valores suspeitos em lotes de transações comerciais, emitindo alertas e permitindo ajustes dinâmicos de limites de segurança em tempo de execução.

Desenvolvido como parte da disciplina de **Algoritmos e Estrutura de Dados**, o sistema aplica conceitos fundamentais de programação como **casting de tipos**, **escopo de variáveis**, **variáveis globais** e **lógica condicional** para processar entradas do usuário e gerar relatórios diagnósticos das vendas analisadas.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab / Jupyter Notebook
* **Paradigma:** Programação Procedural com uso de funções e escopo global

## ⚙️ Funcionalidades

* **Entrada e Casting de Dados:** Leitura de três valores de venda via `input()` com conversão explícita para `float`
* **Cálculo de Média:** Processamento da média aritmética simples entre as vendas informadas
* **Detecção de Anomalias:** Identificação de vendas com valor 5x superior à média (revisão manual)
* **Alerta de Quarentena:** Acionamento automático quando a média ultrapassa o `LIMITE_SEGURANCA`
* **Ajuste Dinâmico de Limite:** Interface interativa para redefinição do limite de segurança em tempo de execução
* **Inspeção de Tipos:** Exibição dos tipos de dados (`type()`) de cada variável processada

## 🔧 Como Executar

1. Clone o repositório:
```bash
   git clone https://github.com/seu-usuario/auditoria-de-dados.git
```
2. Acesse o diretório do projeto:
```bash
   cd auditoria-de-dados
```
3. Execute o script principal:
```bash
   python projeto_algoritomo_de_altoria_de_dados.py
```
4. Informe os valores das três vendas quando solicitado pelo terminal.

> **Alternativa:** Abra o arquivo `.ipynb` diretamente no [Google Colab](https://colab.research.google.com/) ou Jupyter Notebook.

## 📊 Conceitos Abordados

| Conceito | Aplicação no Projeto |
|---|---|
| `input()` e `float()` | Leitura e casting de dados do usuário |
| Variável Global | `LIMITE_SEGURANCA` compartilhado entre escopos |
| Funções e Escopo | Encapsulamento da lógica em `analisar_vendas()` |
| Condicionais `if` | Detecção de anomalias e alertas |
| f-strings | Formatação de saída monetária (`R$ {valor:.2f}`) |
| `type()` | Inspeção e auditoria dos tipos de dados |

## 🐛 Problemas Conhecidos

* A variável `resposta` pode gerar `UnboundLocalError` caso nenhuma venda ultrapasse o `LIMITE_SEGURANCA`, pois o bloco de leitura e o bloco de atribuição de `LIMITE_SEGURANCA` estão em níveis de indentação inconsistentes.
* Recomenda-se refatorar o bloco condicional de ajuste de limite para corrigir o escopo da variável `resposta`.

## 📁 Estrutura do Projeto

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main)
