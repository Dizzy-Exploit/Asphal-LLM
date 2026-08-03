# Asphal-LLM

Construção de um LLM From Scratch

Projeto Integrador da disciplina de Inteligência Artificial e Sistemas Inteligentes — Engenharia de Computação, Unoesc Joaçaba.

O objetivo é implementar do zero os principais componentes de um modelo de linguagem baseado em Transformer, seguindo o livro Build a Large Language Model (From Scratch), do Sebastian Raschka.

A ideia não é competir com modelos comerciais, e sim entender na prática como cada peça funciona: tokenização, embeddings, mecanismos de atenção, blocos transformer, treinamento e geração de texto.

Integrantes: Alan Hoffmann Dos Santos e Jackson Professor: Kleyton Hoffmann Fase: 2026/2

Pipeline que vamos construir
Texto → Tokenização → Token IDs → Embeddings → Positional Embeddings
      → Multi-Head Attention → Transformer Blocks → GPT
      → Treinamento → Geração de Texto
Estrutura do repositório
.
├── README.md
├── requirements.txt
├── docs/
│   ├── glossario/          # glossário técnico por capítulo
│   └── relatorios/         # relatórios de cada sprint
├── notebooks/              # experimentos e exploração
├── src/                    # código-fonte dos componentes
├── data/                   # datasets usados no treino
└── experimentos/           # resultados, logs e comparações

Cada sprint vai adicionando componentes em src/, que são reaproveitados nas etapas seguintes.

Como rodar

Requer Python 3.10 ou superior.

bash
git clone [url-do-repositorio]
cd [nome-do-repositorio]

python -m venv .venv
source .venv/bin/activate        # Linux/macOS
.venv\Scripts\activate           # Windows

pip install -r requirements.txt
Verificando se o ambiente está ok
bash
python -c "import torch; print(torch.__version__); print(torch.cuda.is_available())"

Se imprimir a versão do PyTorch sem erro, está funcionando. O segundo valor indica se há GPU disponível — dá pra rodar o projeto sem GPU, só fica mais lento no treinamento.

Ambiente
Item	Versão
Python	3.x
PyTorch	2.x
Sistema	[Windows / Linux / macOS]
GPU	[modelo ou "sem GPU"]
Cronograma
Sprint	Capítulo	Conteúdo	Status
0	—	Ambiente, repositório e estrutura	✅
1	1	Introdução aos LLMs, glossário e mapa conceitual	🔄
2	2	Tokenização, embeddings e DataLoader	⬜
3	3	Self-Attention, Causal e Multi-Head Attention	⬜
4	4	Arquitetura GPT, Transformer Block, LayerNorm	⬜
5	5	Treinamento, função de perda e geração de texto	⬜
6	6 e 7	Fine-tuning e integração final	⬜
Glossário

O glossário é cumulativo — cada capítulo adiciona os termos novos. Fica em docs/glossario/.

Capítulo 1 — Understanding Large Language Models
Referência

RASCHKA, Sebastian. Build a Large Language Model (From Scratch). Manning Publications.
