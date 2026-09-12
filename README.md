# Simulador de Negociação — Converty Recuperadora de Ativos

Ferramenta interna para simulação de descontos em negociações.
As políticas de desconto são lidas automaticamente do arquivo `politicas.xlsx`
no próprio repositório — sem editar código.

---

## Estrutura do repositório

```
/
├── index.html         ← Simulador (não editar)
├── politicas.xlsx     ← Tabela de políticas — ÚNICO arquivo que você edita
└── README.md
```

---

## Como atualizar as políticas

1. Abra o `politicas.xlsx` no Excel
2. Edite os percentuais na aba **Políticas** (leia a aba **Leia-me**)
3. Salve como `.xlsx` (não mude o formato)
4. Faça o commit no GitHub
5. Aguarde ~1 min — o simulador já carrega os novos valores

---

## Estrutura da planilha (aba Políticas)

| Coluna | Campo                  | Exemplo              |
|--------|------------------------|----------------------|
| A      | Tipo de Devedor        | `Ex Colaborador`     |
| B      | Faixa de Atraso        | `31 a 60 dias`       |
| C      | À Vista (%)            | `10`                 |
| D      | Até 3 Parcelas (%)     | `7`                  |
| E      | 4 a 6 Parcelas (%)     | `5`                  |
| F      | 7 a 10 Parcelas (%)    | `3`                  |
| G      | Mais de 10 Parcelas (%)| `1`                  |

**Regras importantes:**
- Coluna A deve conter `Ex` (Ex Colaborador) ou `Ativo` (Colaborador Ativo)
- Percentuais são números inteiros: `15` = 15% de desconto
- Não usar símbolo `%` nas células — só o número
- Não usar fórmulas nas colunas de percentual
- Manter o formato `.xlsx` ao salvar

---

## Publicando no GitHub Pages

1. Acesse **Settings → Pages** no repositório
2. Em *Source*: **Deploy from a branch**
3. Em *Branch*: **main** / **/ (root)**
4. Clique em **Save**
5. Aguarde 1–2 min e acesse o link gerado

---

## Testando localmente

O navegador bloqueia leitura de arquivos locais por segurança.
Para testar no computador, rode um servidor local:

```bash
# Python 3
python -m http.server 8080
```

Depois acesse: `http://localhost:8080`

---

*Converty Recuperadora de Ativos — Uso Interno*
