````
# 🇵🇹 GEPETO

Modelos e ferramentas de Inteligência Artificial afinados para o **Português Europeu** (pt-PT) — criados à unha, sem tretas.

> **“Não sabes? Pergunta ao Gepeto.”**

---

## 🎯 Objectivos do Projeto

**GEPETO** é uma LLM concebida com foco absoluto na variante portuguesa da língua, orientada para:

- Suporte **nativo e exclusivo** para **Português Europeu (pt‑PT)**
- Capacidade bilingue limitada: apenas **Português (pt‑PT)** e **Inglês formal (EN‑GB)**
- Eliminação total de interferência do **Português do Brasil (pt‑BR)**
- Geração de texto, código e instruções com **clareza, precisão técnica e estilo tuga**
- Aplicação em tarefas práticas como:
  - Tradução pt‑EN
  - Compreensão de instruções complexas
  - Geração de SQL e scripts técnicos
  - Parsing de documentos (faturas, PDFs, tabelas fiscais)
  - Execução **offline** com modelos locais (quantizados)

---

## 📜 Regras do Projeto

### ✅ Permitido

- Dados em **pt‑PT** ou **EN‑GB**, curados manualmente ou com validação assistida
- Datasets em `.parquet` para I/O otimizado
- Conteúdo de código:
  - Comentado em português europeu ou inglês formal
  - Com boas práticas modernas
  - Sem lixo legado ou exemplos desatualizados

### ❌ Proibido

- Qualquer conteúdo em **português do Brasil**
- Expressões, instruções ou sintaxe com traços de pt‑BR
- Datasets traduzidos automaticamente sem validação rigorosa

---

## 📦 Estrutura dos Dados

Todos os datasets seguem o formato **instruction-style**:

- `instruction`: comando ou pergunta
- `input`: (opcional) conteúdo auxiliar
- `output`: resposta esperada

Organizados por diretório:
```plaintext
/datasets/alpaca_ptpt_clean.parquet
/datasets/codigo/
/datasets/curados_manual/
````

---

## ⚙️ Estado do Projeto

* ✅ Tradução e validação do **Alpaca cleaned**
* 🔄 Tradução manual em curso do **GPT-4 Self Instruct DE → pt‑PT**
* 🔜 Geração SQL context-aware
* 🔜 Quantização local (GGUF int3 / int4)
* 🔜 Criação de **tokenizer** especializado para português europeu

---

## 📚 Tecnologias Usadas

* **Python** (Pandas, PyArrow, TQDM)
* **Transformers**, **OpenLLM**, `peft`, `FastAPI`
* Quantização com `llm.cpp`, `optimum`, `gguf`, `mlc-llm`
* Tradução assistida com **LibreTranslate**, **Yandex API** + revisão humana

---

## 🤝 Contribuições

Este projeto é feito com **amor, café e ranho técnico**. Se queres contribuir:

* Garante que todo o conteúdo segue o **pt‑PT** puro
* Justifica os teus pull requests
* Inclui **amostras legíveis** para revisão
* Lembra-te: **isto não é um dataset qualquer** — é o Gepeto.

---

## 🧠 Autor & Licença

**Autor**: Helder Lopes
**Licença**: Apache 2.0

> ⚠️ *Os datasets principais são privados. Apenas amostras representativas são incluídas.*

---

> ✨ **GEPETO** — Porque o português europeu também merece um LLM que não se verga.

```
