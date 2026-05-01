# 🌡️ Analisador de Clima Semanal

## 📝 Descrição do Projeto

Este projeto consiste em um analisador de dados climáticos que coleta e processa as temperaturas diárias de uma semana completa, gerando um relatório automático com estatísticas e alertas de segurança. O objetivo principal é identificar padrões de calor extremo e condições climáticas perigosas, emitindo avisos operacionais com base em limiares predefinidos.

Desenvolvido como parte da disciplina de **Algoritmos e Lógica de Programação**, o sistema aplica conceitos fundamentais como **acumuladores**, **contadores**, **flags booleanas**, **laços de repetição** e **lógica condicional**, simulando um cenário real de monitoramento ambiental automatizado.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab / Jupyter Notebook
* **Paradigma:** Programação Procedural com funções e guard clause (`__main__`)

## ⚙️ Funcionalidades

* **Coleta Semanal:** Entrada das temperaturas dos 7 dias da semana via terminal
* **Acumulador de Temperatura:** Soma progressiva para cálculo da média semanal ao final do ciclo
* **Contagem de Dias Quentes:** Registro automático dos dias com temperatura acima de `35°C`
* **Detecção de Alertas Extremos:** Flag booleana ativada ao detectar temperaturas acima de `45°C` ou abaixo de `-5°C`
* **Relatório Final:** Exibição da média semanal, contagem de dias quentes e status operacional do clima

### Critérios de Classificação

| Condição | Limiar | Ação |
|---|---|---|
| Dia quente | `temp > 35°C` | Incrementa contador `dias_quentes` |
| Alerta extremo | `temp > 45°C` ou `temp < -5°C` | Ativa flag `alerta_extremo` |
| Clima normal | Nenhum alerta ativado | Exibe mensagem de normalidade |

## 🔧 Como Executar

1. Clone o repositório:
```bash
   git clone https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main
```
2. Acesse o diretório do projeto:
```bash
   cd analisador-de-clima
```
3. Execute o script principal:
```bash
   python projeto_analisador_de_clima.py
```
4. Insira a temperatura de cada dia quando solicitado pelo terminal.

> **Alternativa:** Abra o arquivo `.ipynb` diretamente no [Google Colab](https://colab.research.google.com/) ou Jupyter Notebook.

## 📊 Conceitos Abordados

| Conceito | Aplicação no Projeto |
|---|---|
| Acumulador (`soma_temperaturas`) | Soma progressiva das temperaturas ao longo do laço |
| Contador (`dias_quentes`) | Incremento condicional a cada dia acima de 35°C |
| Flag booleana (`alerta_extremo`) | Ativada uma única vez ao detectar condição perigosa |
| `for` + `range(1, 8)` | Iteração controlada pelos 7 dias da semana |
| `if` com operadores lógicos | Condições compostas com `or` para alertas extremos |
| f-strings com `:.1f` | Formatação da média com uma casa decimal |
| Guard clause `__main__` | Boas práticas de execução modular do script |

## 📈 Exemplo de Saída

```
Digite a temperatura do dia 1: 32.0
Digite a temperatura do dia 2: 36.5
Digite a temperatura do dia 3: 28.0
Digite a temperatura do dia 4: 46.2
Digite a temperatura do dia 5: 33.0
Digite a temperatura do dia 6: 30.5
Digite a temperatura do dia 7: 29.0

Média semanal: 33.6°C
Dias acima de 35°C: 2
CUIDADO: Condições climáticas perigosas detectadas!
```

## 📁 Estrutura do Projeto

```
analisador-de-clima/
│
├── projeto_analisador_de_clima.py     # Script principal
├── projeto-analisador-de-clima.ipynb  # Notebook original (Colab)
└── README.md                          # Documentação do projeto
```

---

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main)
