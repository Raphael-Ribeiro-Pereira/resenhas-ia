# Sentiment Hub

> Análise inteligente de sentimentos em resenhas do JetGPT usando modelos de IA rodando localmente.

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![LM Studio](https://img.shields.io/badge/LM%20Studio-Compatible-green.svg)](https://lmstudio.ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

## 🎯 O Projeto

Sentiment Hub processa resenhas de aplicativos em múltiplos idiomas, extrai insights através de um modelo de IA local (Qwen 2.5), e retorna uma análise estruturada com contagens de sentimentos, gráficos visuais e métricas de satisfação.

**Por que local?** Nenhum dado sai do seu computador. Privacidade total, custo zero.

## 🚀 Quick Start

### Pré-requisitos

- Python 3.10 ou superior
- [LM Studio](https://lmstudio.ai) instalado
- 8GB de RAM (recomendado para rodar Qwen 2.5 7B)

### 1️⃣ Instalar LM Studio e carregar o modelo

1. Baixe em https://lmstudio.ai
2. Abra LM Studio → clique em 🔍 **Discover**
3. Procure por `Qwen 2.5 7B Instruct`
4. Clique em **Download**
5. Quando terminar, vá para **Developer** → selecione o modelo → clique em **Start Server**

O servidor vai rodar em `http://127.0.0.1:1234`

### 2️⃣ Clonar o repositório

```bash
git clone https://github.com/seu-usuario/sentiment-hub.git
cd sentiment-hub
```

### 3️⃣ Instalar dependências Python

```bash
pip install openai matplotlib
```

### 4️⃣ Abrir e rodar o notebook

Abra `desafio_jetgpt_v2.ipynb` no VS Code ou Jupyter e execute célula por célula com `Shift + Enter`.

## 📊 O que você consegue

A análise retorna:

✅ **Contagens de Sentimento** — quantas resenhas foram positivas, negativas, neutras

✅ **Gráfico Visual** — bar chart mostrando distribuição

✅ **Análise por Idioma** — qual idioma teve mais elogios/reclamações

✅ **Índice de Satisfação** — número único (-1 a +1) que resume o "humor geral"

✅ **Cache Automático** — segunda execução é 100x mais rápida

## 📁 Estrutura

```
sentiment-hub/
├── desafio_jetgpt_v2.ipynb      # Notebook principal (7 etapas)
├── resenhas_expandidas.txt      # 75 resenhas em 15 idiomas
├── README.md                     # Este arquivo
├── LICENSE                       # MIT License
└── .gitignore
```

## 🔄 O Fluxo das 7 Etapas

| Etapa | Função |
|-------|--------|
| **1** | Carrega arquivo `.txt` e monta lista Python |
| **2** | Configura conexão com LM Studio e testa |
| **3** | Processa todas as resenhas (com cache) |
| **4** | Conta sentimentos e gera string concatenada |
| **5** | Cria gráfico de barras das contagens |
| **6** | Analisa distribuição por idioma |
| **7** | Calcula índice de satisfação numérico |

## 🌍 Idiomas Suportados

Francês • Inglês • Espanhol • Turco • Polonês • Romeno • Italiano • Sueco • Alemão • Japonês • Árabe • Russo • Grego • Vietnamita • Português

## ⚙️ Configuração

No notebook, célula de **Configuração**, você pode ajustar:

```python
BASE_URL = "http://127.0.0.1:1234/v1"  # URL do LM Studio
MODEL_NAME = "qwen2.5"                  # Modelo rodando
ARQUIVO_RESENHAS = "resenhas_expandidas.txt"
ARQUIVO_CACHE = "cache_resenhas.json"
```

## 📈 Exemplo de Saída

```
==================================================
📈 RELATÓRIO
==================================================
😊 Positivas: 34
😠 Negativas: 28
😐 Neutras:   13
📦 Total:     75
==================================================

Índice de satisfação: +0.08
🙂 Saldo positivo, mas tem espaço pra melhorar.
```

## 🛠️ Tecnologias

- **Python 3.10+**
- **LM Studio / Qwen 2.5** — modelo de IA local
- **OpenAI SDK** — cliente compatível com API local
- **Matplotlib** — visualização de gráficos
- **Jupyter Notebook** — ambiente interativo

## 💡 Extensões Possíveis

- Adicionar suporte a mais idiomas
- Exportar resultados em Excel/CSV
- Dashboard web com Flask/Streamlit
- Análise de trending de sentimentos ao longo do tempo
- Integração com banco de dados

## 📝 Licença

Este projeto está licenciado sob a [MIT License](./LICENSE).

## 🤝 Contribuindo

Encontrou um bug? Quer sugerir algo? Abra uma issue ou faça um PR!

## 📧 Contato

Desenvolvido como desafio de aprendizado em Python + IA Local.

---

**Feito com ❤️ e muito café** ☕