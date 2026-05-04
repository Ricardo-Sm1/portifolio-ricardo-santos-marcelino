# 🚀 Simulador de Navegação e Evacuação Espacial

## 📝 Descrição do Projeto

Este projeto implementa um **simulador de evacuação com agente autônomo cego**, desenvolvido em Python. O agente navega por um ambiente sequencial de 10 locais — do quarto dos fundos até a rua — com energia limitada, tomando decisões baseadas no estado de cada nó do caminho.

O simulador modela conceitos fundamentais de **Inteligência Artificial**, como navegação em ambientes desconhecidos, gerenciamento de recursos, coleta de itens e resolução de dependências entre ações (ex.: necessidade de chave para abrir o portão).

Desenvolvido como parte da disciplina de **Inteligência Artificial**, o projeto aplica conceitos de **algoritmos de busca em ambientes determinísticos e estocásticos**, tomada de decisão baseada em estados e modelagem de agentes reflexivos simples.

---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Descrição |
|---|---|
| **Python 3.10+** | Linguagem principal |
| `time` | Controle de ritmo da simulação |
| `random` | Eventos estocásticos (ex.: tropeço na escada) |
| **Google Colab / Jupyter Notebook** | Ambiente de desenvolvimento |

Sem dependências externas — execução nativa com a biblioteca padrão do Python.

---

## 🗺️ Mapa do Ambiente

O agente percorre 10 locais sequenciais, cada um com um estado associado que determina o comportamento da navegação:

```
[0] Quarto dos fundos      → Caminho Livre
[1] Porta do quarto        → porta aberta
[2] Corredor da casa       → Caminho livre
[3] Porta da cozinha       → porta aberta
[4] Cozinha                → virar à esquerda até a área externa
[5] Área externa           → virar à direita até o fim do corredor
[6] Escada estreita        → ⚠️ 20% de chance de tropeço (-1 energia extra)
[7] Garagem                → 🔑 coleta chave do portão
[8] Portão de saída        → 🔒 requer chave do portão
[9] RUA — SAÍDA!           → ✅ evacuação concluída
```

---

## ⚙️ Funcionalidades

### Agente Autônomo
- Navega sequencialmente por 10 nós de um grafo linear
- Opera com **energia limitada** (20 ações iniciais)
- Toma decisões baseadas no **estado atual do nó**

### Sistema de Inventário
- Coleta e armazena itens durante a navegação (ex.: `chave do portão`)
- Usa itens coletados para desbloquear obstáculos futuros

### Eventos Estocásticos
- **Escada estreita**: 20% de probabilidade de tropeço com perda de energia adicional

### Condições de Término
| Condição | Resultado |
|---|---|
| Agente alcança o nó `[9] RUA` | ✅ Evacuação bem-sucedida |
| Energia chega a zero | ❌ Simulação encerrada por falta de energia |

---

## 🔧 Como Executar

### Pré-requisitos
- Python 3.10 ou superior instalado
- Sem necessidade de instalar dependências externas

### Execução Local

```bash
# 1. Clone o repositório
git clone https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino.git

# 2. Acesse o diretório do projeto
cd portifolio-ricardo-santos-marcelino

# 3. Execute o simulador
python projeto_navegação_e_evacuação_espacial.py
```

### Execução no Google Colab
Acesse diretamente pelo link do notebook original no Colab e execute as células em sequência.

---

## 📊 Exemplo de Saída

```
-------------------------------------------------------
 Simulador De Evacuação Agente Cego
-------------------------------------------------------
 Locais no mapa : 10
 Energia inicial: 20 ações
-------------------------------------------------------

[Energia: 20] Local: Quarto dos fundos
Estado : Caminho Livre
-> Agente executa: Caminho Livre.

[Energia: 19] Local: Porta do quarto
Estado : porta aberta
-> Porta aberta! Agente passa sem obstáculo.

...

[Energia: 12] Local: Escada estreita
Estado : descer escada estreita até a garagem
 ATENCAO: Agente tropeça na escada! Perde 1 energia extra.

...

Agente Chegou á Rua! Evacuação Bem Sucedida!
-------------------------------------------------------
Simulação Concluida Agente Evacuado Com Sucesso
Energia restante : 10 ações
-------------------------------------------------------
```

---

## 📐 Conceitos de IA Aplicados

- **Agente Reflexivo Simples**: decisões tomadas com base exclusivamente no estado atual do nó
- **Ambiente Parcialmente Observável**: agente não conhece o mapa completo a priori
- **Ambiente Estocástico**: eventos aleatórios introduzem imprevisibilidade na navegação
- **Gestão de Recursos**: energia finita exige eficiência na tomada de decisão
- **Dependência entre Ações**: a chave coletada na garagem é pré-requisito para abrir o portão

---

## 👤 Autor

**Ricardo Santos Marcelino**  
Disciplina de Inteligência Artificial

---

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main)
