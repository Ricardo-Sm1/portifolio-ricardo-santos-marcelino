# 🧠 Engenharia de Contexto e Lógica Física em Python

## 📝 Descrição do Projeto

Este projeto reúne dois módulos independentes que exploram **engenharia de contexto aplicada** e **simulação de agentes inteligentes** com lógica física e ambiental.

Desenvolvido como parte da disciplina de **Engenharia de Contexto e Lógica Física**, o projeto demonstra como dados do mundo real e estados de ambiente podem ser modelados computacionalmente para suportar tomada de decisão automatizada — desde análise de qualidade do ar urbano até simulação de evacuação com agente reativo.

---

## 📦 Módulos do Projeto

### 🌆 `executar_analise()` — Análise de Qualidade do Ar e Conforto Urbano

Processa dados ambientais de múltiplos pontos urbanos e calcula métricas de habitabilidade:

- Classifica o **Índice de Qualidade do Ar (IQA)** seguindo a escala oficial da **CETESB**:

  | Faixa IQA | Classificação |
  |---|---|
  | 0 – 40 | Boa |
  | 41 – 80 | Moderada |
  | 81 – 120 | Ruim |
  | 121 – 200 | Muito Ruim |
  | > 200 | Péssima |

- Calcula uma **Nota de Conforto Urbano (0 a 10)** usando pesos ponderados:
  - 40% para temperatura (curva gaussiana centrada em 22°C)
  - 30% para umidade relativa
  - 30% para qualidade do ar

- Emite **recomendações automáticas** de exposição ao ambiente externo com base nos limites de segurança

---

### 🚨 Simulador de Evacuação — Agente Cego

Simula um **agente reativo** navegando por 10 nós de um ambiente interno até a saída, sob restrições de energia:

- O agente percorre locais sequenciais com **estados e obstáculos variáveis**
- Implementa lógica de **coleta de item** (chave do portão) e **uso condicional** do item
- Introduz **aleatoriedade física**: risco de tropeço na escada estreita com penalidade de energia
- Encerra com **relatório de evacuação**: sucesso ou falha por exaustão de energia

---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| **Python 3.10+** | Linguagem principal |
| **`math`** | Cálculo da nota de conforto (função gaussiana) |
| **`random`** | Simulação de eventos probabilísticos |
| **`time`** | Controle de ritmo da simulação |
| **`match/case`** | Classificação declarativa do IQA (Python 3.10+) |
| **Google Colab** | Ambiente de desenvolvimento |

---

## 🔧 Como Executar

### Pré-requisitos

- Python **3.10 ou superior** (obrigatório para o uso de `match/case`)
- Sem dependências externas — apenas bibliotecas padrão

### Execução local

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Acesse o diretório
cd seu-repositorio

# Execute o projeto
python projeto_engenharia_de_contexto_e_logica_fisica.py
```

> ⚠️ **Atenção:** Versões anteriores ao Python 3.10 não suportam a sintaxe `match/case`. Verifique sua versão com `python --version`.

---

## 📂 Estrutura do Projeto

---

## 📊 Conceitos Aplicados

- ✅ Modelagem de dados ambientais reais (IQA / CETESB)
- ✅ Funções matemáticas aplicadas (`math.exp`, normalização)
- ✅ Pesos ponderados para métricas compostas
- ✅ Simulação de agente reativo com estado e inventário
- ✅ Controle de fluxo com `match/case` (Python 3.10+)
- ✅ Eventos probabilísticos com `random`
- ✅ Lógica de nós e transições de estado

---

## 🤝 Como Contribuir

1. Faça um **fork** do repositório
2. Crie uma branch para sua feature: `git checkout -b feature/minha-feature`
3. Commit suas alterações: `git commit -m 'feat: adiciona nova funcionalidade'`
4. Envie para a branch: `git push origin feature/minha-feature`
5. Abra um **Pull Request**

---

## 📄 Licença

Este projeto está licenciado sob a licença **MIT**. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

[⬆ Voltar ao início](#-https://github.com/Ricardo-Sm1/portfolio-ricardo-santos-marcelino)
