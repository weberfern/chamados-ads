# API de Chamados de Suporte — Semana 01

## 1. Identificação do Estudante
- **Nome completo:** Weber Fernandes da Silva
- **Matrícula:** 2025019356
- **Disciplina:** [ADS0021] Programação para Web
- **Entrega:** Tag `semana-01`

## 2. Objetivo do Projeto
Desenvolver a estrutura inicial da API Web em Python com Flask para gerenciamento de chamados de suporte de TI, configurando o ambiente virtual, o gerenciador de pacotes `uv` e disponibilizando a rota inicial `GET /` (sem cadastro de chamados ou banco de dados nesta etapa).

## 3. Como Instalar as Dependências
Primeiro instale o `uv`:

```bash
pip install uv
```

Com o `uv` instalado e na raiz do repositório, execute o comando abaixo para criar o ambiente virtual e instalar exatamente as versões travadas em `uv.lock`:

```bash
uv sync --locked
```

## 4. Como Executar a Aplicação
No GitHub Codespaces, inicie o servidor Flask expondo na porta `5000`:

```bash
uv run flask --app app run --host=0.0.0.0 --port=5000
```

## 5. Como Acessar a Rota Inicial e Resposta Esperada
Com o servidor rodando, teste a rota `GET /` pelo navegador (via porta `5000` encaminhada no Codespaces) ou pelo terminal com `curl`:

```bash
curl -i http://localhost:5000/
```

### Resposta Esperada
- **Status HTTP:** `200 OK`
- **Cabeçalho:** `Content-Type: application/json`
- **Corpo (JSON):**

```json
{
  "mensagem": "API de chamados em funcionamento"
}
```