# 🏥 Sistema de Triagem de Emergência Hospitalar

## 📝 Descrição do Projeto

Este projeto consiste em um algoritmo de triagem clínica que classifica automaticamente pacientes em níveis de prioridade de atendimento com base em sinais vitais e fatores de risco coletados na entrada da emergência. O objetivo principal é simular o protocolo de triagem de Manchester, determinando a urgência do atendimento de forma estruturada e reproduzível, eliminando subjetividade na fila de espera.

Desenvolvido como parte da disciplina de **Algoritmos e Lógica de Programação**, o projeto foi modelado inteiramente no papel — com **fluxograma de decisão** e **pseudocódigo estruturado com laço de repetição** — antes de qualquer implementação, praticando o raciocínio algorítmico aplicado a um contexto real da área da saúde.

## 🗂️ Artefatos do Projeto

| Artefato | Descrição |
|---|---|
| `fluxograma_triagem.pdf` (pág. 1) | Fluxograma com pipeline de triagem e as quatro faixas de prioridade |
| `pseudocodigo_decisoes.pdf` (pág. 2) | Pseudocódigo com decisões 2 e 3, laço de repetição e encerramento |
| `pseudocodigo_variaveis.pdf` (pág. 3) | Pseudocódigo com declaração de variáveis, entrada de dados e decisão 1 |

## ⚙️ Lógica do Algoritmo

### Variáveis de Entrada

| Variável | Tipo | Descrição |
|---|---|---|
| `Idade` | Inteiro | Idade do paciente em anos |
| `Freq_Cardiaca` | Inteiro | Frequência cardíaca (bpm) |
| `Saturacao` | Real | Saturação de O₂ (%) |
| `Temperatura` | Real | Temperatura corporal (°C) |
| `Dor` | Inteiro | Nível de dor — escala de 0 a 10 |
| `Comorbidade` | Lógico | Presença de comorbidade (Verdadeiro/Falso) |

### Árvore de Decisão Clínica

```
// Decisão 1 — Risco de Vida Imediato
SE Freq_Cardiaca >= 130 OU Saturacao < 90 ENTÃO
    → 🔴 PRIORIDADE VERMELHA — Atendimento Imediato

// Decisão 2 — Sintomas Graves
SE Dor >= 8 OU Temperatura >= 39 ENTÃO
    → 🟡 PRIORIDADE AMARELA — Atendimento Rápido

// Decisão 3 — Grupo de Risco
SE Idade >= 60 OU Idade < 5 OU Comorbidade = Verdadeiro ENTÃO
    → 🟠 PRIORIDADE LARANJA — Atendimento Prioritário

// Nenhuma condição acima
→ 🟢 PRIORIDADE VERDE — Aguardar Atendimento
```

### Estrutura de Repetição

O algoritmo opera em **laço contínuo** (`enquanto Continuar = Verdadeiro`), permitindo triagens sequenciais sem reiniciar o sistema — ao final de cada avaliação, o operador decide se deseja realizar uma nova triagem.

```
continuar ← Verdadeiro
enquanto (continuar = Verdadeiro) faça
    // Coleta de dados → Análise → Classificação → Exibição
    Escreva ("Deseja realizar nova triagem? (Verdadeiro/Falso): ")
    Leia (continuar)
fimenquanto
```

## 📊 Conceitos Abordados

| Conceito | Aplicação no Projeto |
|---|---|
| Declaração de variáveis tipadas | `Inteiro`, `Real`, `Lógico` para cada sinal vital |
| Condicional encadeada (`SE / SENÃO`) | Triagem em três níveis de prioridade decrescente |
| Operadores lógicos (`OU`) | Combinação de condições clínicas em cada decisão |
| Laço `enquanto` com flag booleana | Controle de repetição para múltiplas triagens |
| Fluxograma de decisão | Representação visual do protocolo clínico |
| Pseudocódigo estruturado | Modelagem independente de linguagem de programação |

## 🚦 Tabela de Prioridades

| Cor | Nível | Critério | Conduta |
|---|---|---|---|
| 🔴 Vermelho | Crítico | FC ≥ 130 bpm **ou** SpO₂ < 90% | Atendimento Imediato |
| 🟡 Amarelo | Urgente | Dor ≥ 8 **ou** Temperatura ≥ 39°C | Atendimento Rápido |
| 🟠 Laranja | Prioritário | Idade ≥ 60 **ou** < 5 anos **ou** Comorbidade | Atendimento Prioritário |
| 🟢 Verde | Não urgente | Nenhuma condição anterior | Aguardar Atendimento |

## 🔄 Fluxo Resumido

```
INÍCIO
  └── LAÇO: enquanto Continuar = Verdadeiro
        └── TRIAGEM (entrada de dados)
              └── Decisão 1: FC >= 130 ou SpO₂ < 90?
                    ├── SIM → 🔴 VERMELHO
                    └── NÃO → Decisão 2: Dor >= 8 ou Temp >= 39?
                                ├── SIM → 🟡 AMARELO
                                └── NÃO → Decisão 3: Idade >= 60 ou < 5 ou Comorbidade?
                                            ├── SIM → 🟠 LARANJA
                                            └── NÃO → 🟢 VERDE
        └── Nova triagem? → SIM: repete | NÃO: FIM
```

## 🚀 Próximos Passos

- [ ] Implementar o algoritmo em Python com base no pseudocódigo
- [ ] Adicionar validação de entradas fora dos intervalos clínicos esperados
- [ ] Gerar relatório de triagem por paciente com timestamp
- [ ] Implementar interface de terminal interativa com `input()`
- [ ] Explorar visualização dos dados coletados com `matplotlib`

## 📁 Estrutura do Repositório

```
triagem-emergencia/
│
├── fluxograma_triagem.pdf          # Fluxograma principal com as 4 prioridades
├── pseudocodigo_decisoes.pdf       # Pseudocódigo — decisões 2 e 3, laço e fim
├── pseudocodigo_variaveis.pdf      # Pseudocódigo — variáveis, entrada e decisão 1
└── README.md                       # Documentação do projeto
```

---

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portfolio-ricardo-santos-marcelino)
