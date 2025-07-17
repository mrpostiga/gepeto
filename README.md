# 🇵🇹 AlbertinaLLM  
Modelos e ferramentas de Inteligência Artificial afinadas para o **Português Europeu** (pt-PT)

---

## 🎯 Objectivos do Projecto

AlbertinaLLM é uma LLM cuidadosamente construída com o propósito de:

- Suporte nativo e exclusivo para **Português Europeu (pt-PT)**  
- Capacidade bilingue limitada a **Português (pt-PT)** e **Inglês (EN)**
- Eliminação total de conteúdos em **Português do Brasil (pt-BR)**
- Geração de instruções, respostas e código com clareza, utilidade e rigor linguístico
- Aplicação prática em tarefas como:
  - Tradução pt-EN
  - Compreensão de instruções
  - Geração de SQL e código
  - Parsing inteligente de documentos (ex: faturas, PDFs)
  - Suporte offline com modelos locais (quantizados)

---

## 📜 Regras do Projecto

### ✅ Permitido

- Línguas suportadas: **Português Europeu** e **Inglês**
- Datasets curados manualmente ou validados automaticamente com assistente pt-PT
- Dados em formato **Parquet** para maximizar performance de I/O e treino
- Datasets de código, desde que:
  - Comentados em pt-PT ou inglês formal (EN-GB)
  - Com boas práticas modernas
  - Limpos de exemplos obsoletos

### ❌ Proibido

- Qualquer dataset em **português do Brasil**
- Conteúdo com vocabulário, expressões, instruções ou sintaxe típicas de pt-BR
- Datasets não curados ou traduzidos automaticamente sem verificação

---

## 📦 Formato e Organização dos Dados

- Todos os datasets são convertidos para **`.parquet`**  
- A estrutura dos datasets segue o formato:
  - `instruction` – a tarefa ou comando
  - `input` – conteúdo adicional (opcional)
  - `output` – resposta esperada
- Dados são armazenados em diretórios como:
  - `/datasets/alpaca_ptpt_clean.parquet`
  - `/datasets/codigo/`
  - `/datasets/curados_manual/`

---

## ⚙️ Estado do Projecto

- [x] Tradução completa do dataset **Alpaca cleaned** (validação manual)
- [x] Tradução em curso do dataset **GPT-4 Self Instruct DE → pt-PT**
- [ ] Integração de capacidade de geração SQL
- [ ] Quantização para execução local (GGUF int3 / int4)
- [ ] Criação de tokenizer próprio para português europeu

---

## 📚 Tecnologias Utilizadas

- Python (Pandas, PyArrow, TQDM)
- OpenLLM / Transformers
- FastAPI (para UI auxiliar de conversão e treino)
- Quantização com `llm.cpp`, `gguf`, `optimum`, ou `mlc-llm`
- Ferramentas de tradução assistida: Yandex API, LibreTranslate local, pós-edited

---

## 🤝 Contribuições

Este é um projecto **curado manualmente** com muito cuidado e atenção à variante europeia da língua portuguesa.  
Se queres contribuir:

- Evita conteúdos em pt-BR
- Segue o padrão pt-PT
- Garante que o conteúdo seja realmente **útil e educativo**
- Pull requests com datasets devem ser justificados e acompanhados de amostra visível

---

## 🧠 Autor e Licença

**Autor**: Helder Lopes  
**Licença**: MIT (excepto datasets, sujeitos às suas próprias licenças)

⚠️ **Os datasets completos usados para treinar a AlbertinaLLM são privados.**  
Apenas amostras representativas são incluídas para demonstração da estrutura.


---

**AlbertinaLLM** — porque o Português Europeu também merece um LLM de excelência 🇵🇹
