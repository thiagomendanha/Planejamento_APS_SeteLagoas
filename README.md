
# Planejamento da Rede de Atenção Primária à Saúde em Sete Lagoas

Este projeto utiliza o **GLPK (GNU Linear Programming Kit)** para resolver um problema de localização de unidades de saúde no município de Sete Lagoas – MG. O modelo foi construído com base em critérios de equidade, cobertura, custo e capacidade instalada, visando à organização racional da Rede de Atenção Primária à Saúde (APS).

---

## 📁 Estrutura do Projeto

```
Planejamento_APS_SeteLagoas/
├── model/
│   └── hc-closest.mod
├── data/
│   └── hc-closest.dat
├── images/
│   └── localizacao_novas_unidades.png
├── README.md
```

---

## 📌 Objetivo

Propor um plano de localização para unidades de saúde que atenda à demanda da população, respeitando os critérios de cobertura geográfica e capacidade das equipes, com foco principal na APS.

---

## ▶️ Como Executar

1. Instale o GLPK: https://www.gnu.org/software/glpk/

2. Execute no terminal:

```bash
glpsol -m model/hc-closest.mod -d data/hc-closest.dat
```

---

## 📊 Resultados da Modelagem

### 3.6. Análise dos Resultados

A solução ótima respeita as restrições do modelo e garante cobertura universal da APS. A seguir estão os principais resultados:

### 3.6.1. Caracterização Financeira

**Custo Total:** R$ 164.271.649,48  
**Custo APS:** R$ 50.633.053,25 (dentro do orçamento de R$ 90.399.976,00)

| Natureza do Custo                          | Valor (R$)         |
|-------------------------------------------|--------------------|
| Custo Logístico                            | 923.115,85         |
| Custo Fixo Unidades Existentes [E]         | 17.209.420,00      |
| Custo Fixo Novas Unidades [C]              | 539.658,00         |
| Custo de Nova Equipe [C]                   | 654.024,00         |
| Custo Variável                              | 144.945.431,63     |

---

### 3.6.2. Novas Unidades Criadas

12 de 15 localidades candidatas foram selecionadas.

![Figura 9 – Localização das Novas Unidades de Atenção Primária](images/localizacao_novas_unidades.png)

---

### 3.6.3. Novas Equipes

15 novas equipes foram alocadas.

| Unidade | Nº eSFs | ME1 | EF1 | TE1 | ACS | DE1 | TD1 |
|---------|---------|-----|-----|-----|-----|-----|-----|
| PHC56   | 2       | 2   | 2   | 2   | 8   | 2   | 2   |
| PHC57   | 1       | 1   | 1   | 1   | 4   | 1   | 1   |
| ...     | ...     | ... | ... | ... | ... | ... | ... |

---

### 3.6.4. Equipes Existentes

- Boa distribuição de médicos, enfermeiros e técnicos
- Déficit na Equipe de Saúde Bucal
- ACSs com distribuição desigual
- eMulti estável e fortalecida por políticas federais

---

### 3.6.5. Capacidade Utilizada

#### APS – Utilização próxima de 100%

| Unidade | Capacidade Total | Utilizada | % |
|---------|------------------|-----------|----|
| PHC1    | 3000             | 3000      |100%|
| PHC2    | 6000             | 6000      |100%|
| ...     | ...              | ...       |... |

*Nota: existe margem de até 50% caso use-se o teto de 4.500 pessoas por UBS.*

#### SHC – Subutilização de 2% a 75%  
#### THC – Subutilização alta, mas explicada por limitações do modelo

---

## 🔗 Repositório

Este projeto está disponível em:  
👉 [https://github.com/thiagomendanha/Planejamento_APS_SeteLagoas](https://github.com/thiagomendanha/Planejamento_APS_SeteLagoas)

---

## 📜 Licença

MIT

## ✉️ Contato

Thiago Mendanha  
📧 [mbm.thiago@gmail.com](mailto:mbm.thiago@gmail.com)
