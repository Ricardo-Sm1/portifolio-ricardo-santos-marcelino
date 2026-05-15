# 💵 Algoritmo de Cálculo de Troco com Decomposição em Cédulas

## 📝 Descrição do Projeto

Este projeto consiste em um algoritmo de cálculo de troco que, a partir do valor de uma compra e do valor pago pelo cliente, determina automaticamente o troco devido e o decompõe no menor número de cédulas possível. O objetivo principal é simular o comportamento de um caixa eletrônico ou PDV (ponto de venda), aplicando lógica de divisão e módulo para distribuir o troco entre as denominações disponíveis.

Desenvolvido como parte da disciplina de **Algoritmos e Lógica de Programação**, o projeto foi concebido inteiramente no papel — com **pseudocódigo estruturado** e **fluxogramas desenhados à mão** — antes de qualquer implementação, praticando o raciocínio algorítmico independente de linguagem de programação.

## 🗂️ Artefatos do Projeto

Este repositório documenta as etapas de modelagem manual do algoritmo:

| Artefato | Descrição |
|---|---|
| `fluxograma_troco.pdf` | Fluxograma principal com decisões condicionais e cálculo por cédula |
| `fluxograma_caixa.pdf` | Fluxograma do fluxo de caixa com validação de pagamento insuficiente |
| `pseudocodigo_pagina1.pdf` | Pseudocódigo com coleta, validação e cálculo do troco e cédulas |
| `pseudocodigo_pagina2.pdf` | Pseudocódigo com saída formatada das denominações e encerramento |

## ⚙️ Lógica do Algoritmo

### Etapa 1 — Coleta e Validação
```
LER valor_compra
LER valor_pago
SE valor_pago < valor_compra ENTÃO
    MOSTRAR "Pagamento Insuficiente"
    FIM
```

### Etapa 2 — Cálculo do Troco
```
troco ← valor_pago - valor_compra
MOSTRAR "Troco: ", troco
```

### Etapa 3 — Decomposição em Cédulas
```
notas100 ← troco DIV 100  |  troco ← troco MOD 100
notas50  ← troco DIV 50   |  troco ← troco MOD 50
notas10  ← troco DIV 10   |  troco ← troco MOD 10
notas5   ← troco DIV 5    |  troco ← troco MOD 5
notas1   ← troco
```

### Etapa 4 — Saída
```
MOSTRAR notas100, "Nota de 100"
MOSTRAR notas50,  "Nota de 50"
MOSTRAR notas10,  "Nota de 10"
MOSTRAR notas5,   "Nota de 5"
MOSTRAR notas1,   "Nota de 1"
```

## 📊 Conceitos Abordados

| Conceito | Aplicação no Algoritmo |
|---|---|
| Divisão inteira (`DIV`) | Quantidade de cédulas de cada denominação |
| Módulo (`MOD`) | Valor restante após separar cada denominação |
| Condicional (`SE / SENÃO`) | Validação de pagamento suficiente |
| Sequência lógica | Pipeline ordenado do maior para o menor valor de cédula |
| Fluxograma | Representação visual do fluxo de decisão e processamento |
| Pseudocódigo | Descrição estruturada e independente de linguagem |

## 🔄 Fluxo Resumido

```
INÍCIO
  └── LER valor_compra e valor_pago
        └── SE valor_pago >= valor_compra
              └── troco = valor_pago - valor_compra
                    └── Decompor em cédulas (100 → 50 → 10 → 5 → 1)
                          └── MOSTRAR resultado
                                └── FIM
              └── SENÃO → "Saldo Insuficiente" → FIM
```

## 🚀 Próximos Passos

- [ ] Implementar o algoritmo em Python com base no pseudocódigo
- [ ] Adicionar suporte a valores decimais (moedas de R$ 0,50 e R$ 0,25)
- [ ] Criar interface de terminal interativa com `input()`
- [ ] Implementar testes automatizados para os casos de borda

## 📁 Estrutura do Repositório

```
calculo-de-troco/
│
├── fluxograma_troco.pdf          # Fluxograma principal (cédulas)
├── fluxograma_caixa.pdf          # Fluxograma de validação do caixa
├── pseudocodigo_pagina1.pdf      # Pseudocódigo — coleta, validação e cálculo
├── pseudocodigo_pagina2.pdf      # Pseudocódigo — saída e encerramento
└── README.md                     # Documentação do projeto
```

---

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portfolio-ricardo-santos-marcelino)
