# 🛒 Processador de Vendas com Desconto Progressivo

## 📝 Descrição do Projeto

Este projeto consiste em um sistema de processamento de vendas no varejo que calcula o valor total de uma compra com múltiplos produtos e aplica descontos automaticamente de acordo com o volume da transação. O objetivo principal é simular o fluxo real de um caixa comercial, com validação de entradas, cálculo de subtotais por item e aplicação de uma política de descontos progressivos sobre o total da compra.

Desenvolvido como parte da disciplina de **Algoritmos e Lógica de Programação**, o sistema aplica conceitos fundamentais como **acumuladores**, **contadores**, **validação de dados com `if`**, **laços de repetição** e **lógica condicional encadeada**, simulando um cenário real de automação comercial.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Ambiente:** Google Colab / Jupyter Notebook
* **Paradigma:** Programação Procedural com funções e guard clause (`__main__`)

## ⚙️ Funcionalidades

* **Cadastro de Produtos:** Entrada do nome, preço unitário e quantidade para cada tipo de produto da compra
* **Validação de Dados:** Rejeição automática de preços e quantidades com valores inválidos (`<= 0`), exibindo mensagem de erro por produto
* **Cálculo de Subtotal:** Multiplicação do preço unitário pela quantidade para cada item registrado
* **Acumuladores:** Soma progressiva do valor total e contagem total de itens ao longo do laço
* **Desconto Progressivo:** Aplicação automática de desconto com base no valor bruto da compra:

| Total da Compra | Desconto | Fator Aplicado |
|---|---|---|
| Acima de R$ 500,00 | 10% | `× 0.90` |
| Entre R$ 200,01 e R$ 500,00 | 5% | `× 0.95` |
| Até R$ 200,00 | Sem desconto | `× 1.00` |

* **Resumo Final:** Exibição do total de itens comprados e do valor final com desconto aplicado

## 🔧 Como Executar

1. Clone o repositório:
```bash
   git clone https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main
```
2. Acesse o diretório do projeto:
```bash
   cd processador-de-vendas
```
3. Execute o script principal:
```bash
   python projeto_processador_de_vendas.py
```
4. Siga as instruções no terminal para registrar os produtos da compra.

> **Alternativa:** Abra o arquivo `.ipynb` diretamente no [Google Colab](https://colab.research.google.com/) ou Jupyter Notebook.

## 📊 Conceitos Abordados

| Conceito | Aplicação no Projeto |
|---|---|
| Acumulador (`total_compra`) | Soma progressiva dos subtotais de cada produto |
| Contador (`itens_comprados`) | Totalização da quantidade de unidades compradas |
| Validação de entrada | Rejeição de preço ou quantidade `<= 0` com mensagem de erro |
| `for` + `range()` | Iteração sobre cada tipo de produto informado |
| `if / elif / else` | Política de descontos progressivos por faixa de valor |
| Subtotal por item | Cálculo de `preco * qtd` antes de acumular |
| f-strings com `:.2f` | Formatação monetária do total final |
| Guard clause `__main__` | Boas práticas de execução modular do script |

## 📈 Exemplo de Saída

```
Quantos produtos diferentes foram comprados? 2

Nome do produto: Camiseta
Preço unitário: 89.90
Quantidade deste produto: 3

Nome do produto: Calça
Preço unitário: 0
Quantidade deste produto: 1
Erro: Valores inválidos para Calça

Desconto de 10% aplicado!
Resumo: 3 itens. Total a pagar: R$ 242.73
```

## 📁 Estrutura do Projeto

```
processador-de-vendas/
│
├── projeto_processador_de_vendas.py     # Script principal
├── projeto-processador-de-vendas.ipynb  # Notebook original (Colab)
└── README.md                            # Documentação do projeto
```

---

[🔝 Voltar ao início](https://github.com/Ricardo-Sm1/portifolio-ricardo-santos-marcelino/tree/main)
