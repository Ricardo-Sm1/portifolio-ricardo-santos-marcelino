# 🎨 Criador e Processador de Emojis em Pixel Art

## 📝 Descrição do Projeto

Este projeto consiste em um processador de imagens em pixel art que representa emojis como matrizes de pixels RGB e aplica transformações de cor programaticamente. O objetivo principal é demonstrar como imagens digitais podem ser manipuladas pixel a pixel por meio de estruturas de dados nativas do Python, sem o uso de bibliotecas de processamento de imagem de alto nível.

Desenvolvido como parte da disciplina de **Algoritmos e Estrutura de Dados**, o sistema utiliza um **dicionário** como estrutura central de armazenamento da grade de pixels, percorre a matriz com **laços aninhados** e aplica uma transformação de escurecimento seletivo sobre pixels amarelos `(255, 255, 0)` via **divisão inteira por canal RGB**, renderizando o resultado visualmente com `matplotlib`.

## 🚀 Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Bibliotecas:** Matplotlib (`pyplot`, `imshow`)
* **Ambiente:** Google Colab / Jupyter Notebook
* **Paradigma:** Programação Procedural com manipulação de estruturas de dados aninhadas

## ⚙️ Funcionalidades

* **Representação em Matriz RGB:** O emoji é armazenado como uma lista de listas de tuplas `(R, G, B)` dentro de um dicionário Python
* **Iteração Aninhada:** Percurso completo da grade por linha e por pixel usando `for` encadeado com `.items()`
* **Transformação Seletiva de Cor:** Pixels amarelos `(255, 255, 0)` têm cada canal reduzido à metade via divisão inteira (`// 2`), resultando em tom mais escuro `(127, 127, 0)`; pixels pretos permanecem inalterados
* **Atualização In-Place do Dicionário:** A grade processada substitui a original dentro de `emoji_data["grade"]`
* **Renderização Visual:** Exibição da grade transformada como imagem com `plt.imshow()`, sem eixos

### Pipeline de Transformação

```
emoji_data["grade"]          →     Leitura por linha e pixel
     ↓
Pixel == (255, 255, 0)?      →     Sim: aplica pixel // 2 por canal
     ↓                             Não: mantém pixel original
nova_grade (lista acumulada) →     Substitui emoji_data["grade"]
     ↓
plt.imshow()                 →     Renderização visual
```

## 🔧 Como Executar

1. Clone o repositório:
```bash
   git clone https://github.com/seu-usuario/criador-de-emojis.git
```
2. Acesse o diretório do projeto:
```bash
   cd criador-de-emojis
```
3. Instale a dependência necessária:
```bash
   pip install matplotlib
```
4. Execute o script principal:
```bash
   python projeto_criador_de_emojis.py
```

> **Alternativa:** Abra o arquivo `.ipynb` diretamente no [Google Colab](https://colab.research.google.com/) — ambiente recomendado para visualização inline da imagem gerada.

## 📊 Conceitos Abordados

| Conceito | Aplicação no Projeto |
|---|---|
| Dicionário (`dict`) | Estrutura central de armazenamento da grade de pixels |
| Lista de listas | Representação matricial da imagem (linhas × pixels) |
| Tuplas RGB | Cada pixel armazenado como `(R, G, B)` imutável |
| Laços aninhados (`for` triplo) | Iteração sobre dicionário → linhas → pixels |
| `.items()` | Desestruturação de chave-valor no laço externo |
| Divisão inteira (`//`) | Escurecimento canal a canal sem arredondamento |
| Condicional por igualdade de tupla | Comparação direta `pixel == (255, 255, 0)` |
| `matplotlib.pyplot` | Renderização da grade RGB como imagem visual |

## 📈 Exemplo de Saída no Terminal

```python
# Grade transformada impressa linha a linha:
[(127, 127, 0), (127, 127, 0), (0, 0, 0)]
[(127, 127, 0), (0, 0, 0),     (127, 127, 0)]
[(127, 127, 0), (127, 127, 0), (127, 127, 0)]
```
> Os pixels amarelos `(255, 255, 0)` foram escurecidos para `(127, 127, 0)`.
> Os pixels pretos `(0, 0, 0)` permaneceram inalterados.

## 📁 Estrutura do Projeto

```
criador-de-emojis/
│
├── projeto_criador_de_emojis.py     # Script principal
├── projeto_criador_de_emojis.ipynb  # Notebook original (Colab)
└── README.md                        # Documentação do projeto
```

---

[🔝 Voltar ao início](https://github.com/seu-usuario/criador-de-emojis)
