# 🌡️ Algoritmo do Microclima Local

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Licença](https://img.shields.io/badge/Licença-MIT-lightgrey)

## 📝 Descrição do Projeto

Este projeto consiste em um algoritmo desenvolvido em Python que realiza a **análise de qualidade do ar e conforto urbano** em diferentes pontos da cidade de São Paulo. A partir de dados de temperatura, umidade relativa e Índice de Qualidade do Ar (IQA), o sistema classifica cada local segundo a escala oficial da **CETESB** e calcula uma **Nota de Conforto Urbano** (0 a 10), emitindo recomendações automáticas de exposição ao ar livre.

Desenvolvido como parte da disciplina de **Inteligência Artificial**, o projeto aplica conceitos de modelagem de ambientes urbanos, funções de avaliação baseadas em múltiplos critérios e tomada de decisão orientada a dados.

---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Versão | Uso |
|---|---|---|
| Python | 3.10+ | Linguagem principal |
| `math` | stdlib | Cálculo da nota de conforto (função gaussiana) |
| Jupyter Notebook / Google Colab | — | Ambiente de desenvolvimento |

> Sem dependências externas. Apenas bibliotecas padrão do Python.

---

## 📊 Funcionalidades

### Análise Urbana por Local

- **Coleta de métricas:** temperatura (°C), umidade relativa (%) e IQA por ponto da cidade
- **Classificação do IQA** segundo a escala da CETESB:

  | Faixa de IQA | Classificação |
  |---|---|
  | 0 – 40 | Boa |
  | 41 – 80 | Moderada |
  | 81 – 120 | Ruim |
  | 121 – 200 | Muito Ruim |
  | > 200 | Péssima |

- **Nota de Conforto Urbano (0 a 10):** calculada com pesos ponderados por critério:
  - Temperatura: peso 40% — função gaussiana centrada em 22 °C
  - Umidade: peso 30% — penalidade para valores fora da faixa ideal
  - IQA: peso 30% — penalidade linear proporcional ao índice
- **Recomendações automáticas** de exposição ao ar livre por local

---

## 🔧 Como Executar

### Pré-requisitos

- Python 3.10 ou superior instalado
- Nenhuma dependência externa necessária

### Passos

```bash
# 1. Clone o repositório
git clone https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino.git

# 2. Acesse o diretório do projeto
cd portifolio-ricardo-santos-marcelino

# 3. Execute o algoritmo
python projeto-algoritmo-do-microclima-local.py
```

### Saída Esperada

```
Analise de qualidade do ar e conforto urbano

Local: Praça Brasil
 Temperatura (C): 30
 IQA: 57
 Umidade(%): 44
 Qualidade do Ar (IQA 57): Moderada
 Nota de Conforto Urbano: 4.67 / 10
 Recomendacao: evite exposicao prolongada neste local.
...
```

---

## 📁 Estrutura do Projeto

```
portifolio-ricardo-santos-marcelino/
│
├── projeto-algoritmo-do-microclima-local.py   # Script principal
└── README.md                                  # Documentação do projeto
```

---

## 🧠 Conceitos Aplicados

- **Função gaussiana** para modelagem da zona de conforto térmico
- **Tomada de decisão multi-critério** com pesos ponderados
- **Classificação por intervalos** seguindo padrão regulatório (CETESB)
- **Pattern matching estrutural** com `match/case` (Python 3.10+)

---

## 📌 Pontos Monitorados (Dados de Exemplo)

| Local | Temperatura (°C) | IQA | Umidade (%) |
|---|---|---|---|
| Praça Brasil | 30 | 57 | 44 |
| Metrô Itaquera | 27 | 73 | 45 |
| Terminal Carrão | 29 | 50 | 40 |

---

## 👤 Autor

**Ricardo Santos Marcelino**
🔗 [🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main)
