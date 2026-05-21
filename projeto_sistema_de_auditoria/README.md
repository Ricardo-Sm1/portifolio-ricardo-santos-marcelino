# 🏢 Auditoria de Orçamentos Corporativos (Python)
 
[![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-concluído-brightgreen.svg)]()
 
## 📖 Sobre o Projeto
Este projeto foi desenvolvido como parte da disciplina de Programação de Computadores do curso de Análise e Desenvolvimentos de Sistemas.
O objetivo do script é processar e calcular o orçamento de uma estrutura organizacional complexa (dicionários aninhados) de uma multinacional, aplicando regras de negócio dinâmicas e auditoria de execução.
 
A solução foi arquitetada utilizando conceitos avançados de Python para garantir flexibilidade, performance e rastreabilidade.
 
## 🚀 Funcionalidades
- **Cálculo Hierárquico:** Varredura completa da estrutura corporativa, independentemente do nível de profundidade.
- **Filtros Dinâmicos:** Capacidade de ignorar setores específicos e todos os seus subsetores na hora do cálculo financeiro.
- **Conversão de Câmbio:** Suporte a parâmetros opcionais para conversão de moedas em tempo de execução.
- **Sistema de Auditoria:** Monitoramento automatizado de tempo de execução e registro (logging) dos parâmetros utilizados na transação financeira.
 
## 🛠️ Tecnologias e Conceitos Aplicados
Este projeto foi construído utilizando Python puro (Standard Library), com foco nos seguintes paradigmas e recursos:
* **Funções Recursivas (Recursion):** Utilizadas para a navegação na árvore de dados (dicionários aninhados).
* **Decorators:** Implementação do `@auditor` para injetar comportamentos de log e cronometragem sem modificar a lógica de negócios.
* **Empacotamento de Argumentos (`*args` e `**kwargs`):** Utilizados tanto no decorator quanto na função principal para permitir a passagem dinâmica de departamentos a serem ignorados e taxas de câmbio.
 
## ⚙️ Como Executar
 
### Pré-requisitos
* Python 3.8 ou superior instalado.
 
### Passo a Passo
1. Clone este repositório:
   ```bash
   git clone https://github.com/Ricardo-Sm1/portfolio-ricardo-santos-marcelino
   ```
2. Acesse a pasta do projeto:
   ```bash
   cd seu-repositorio
   ```
3. Execute o script principal:
   ```bash
   python main.py
   ```
 
## 🧠 Lógica e Estrutura do Código
Breve explicação de como o código foi organizado:
A recursão foi construída pensando na hierarquia da empresa como uma “árvore” de departamentos.
A função calcular_orcamento percorre cada item do dicionário e verifica se o valor encontrado ainda é outro dicionário.
Quando isso acontece, a própria função é chamada novamente, entrando em um nível mais profundo da estrutura até encontrar
os valores numéricos finais dos orçamentos. Esse modelo permite que o algoritmo funcione independentemente da quantidade
de níveis existentes na empresa, tornando a solução flexível e escalável. Além disso, o uso de *args foi integrado para ignorar
departamentos específicos durante a navegação recursiva, fazendo com que a função pule automaticamente esses setores e todos os
seus subdepartamentos.

O decorator @auditor foi acoplado ao projeto para adicionar uma camada de monitoramento sem modificar diretamente a lógica
principal da função. Ele intercepta a execução de calcular_orcamento, registra os argumentos recebidos, mede o tempo de execução
utilizando a biblioteca time e imprime um relatório de auditoria antes e depois do processamento. Para garantir
compatibilidade com qualquer quantidade de parâmetros, o wrapper do decorator também utiliza *args e **kwargs, permitindo capturar
todos os argumentos enviados para a função original.

Os dados da empresa foram organizados em um dicionário aninhado chamado empresa_data, representando a estrutura hierárquica da organização.
O nível principal contém a "Matriz", que se divide em departamentos como "TI", "RH" e "Financeiro". Alguns setores possuem novos subníveis internos,
como "Infraestrutura" e "Desenvolvimento" dentro de "TI", criando uma árvore de informações mais profunda.

Nos níveis finais da estrutura estão os valores numéricos dos orçamentos, como "Servidores": 50000 e "Backend": 25000. Essa organização
facilita o uso da recursão, pois a função consegue navegar automaticamente pelos dicionários internos até encontrar
os valores financeiros que devem ser somados.
 
## 👤 Autor
 
* **Ricardo Santos Marcelino** * LinkedIn: https://www.linkedin.com/in/ricardo-santos-3b3a04291/
* E-mail: ricardo.marcelino455@gmai.com
 
---
[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portfolio-ricardo-santos-marcelino)
