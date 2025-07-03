# Projeto de Localização de Unidades de Saúde

Este projeto utiliza o **GLPK (GNU Linear Programming Kit)** para resolver um problema de localização de unidades de saúde. O modelo matemático está implementado em linguagem MathProg (.mod), e os dados específicos do problema estão em um arquivo .dat.

---

## 📁 Estrutura do Projeto

```
meu_projeto_glpk/
├── model/
│   └── hc-closest.mod         # Modelo matemático
├── data/
│   └── hc-closest.dat         # Dados de entrada
├── README.md                  # Este arquivo
```

---

## 📌 Objetivo

Determinar a melhor alocação de unidades de saúde, considerando critérios como:
- Capacidade de atendimento
- Distância dos pacientes às unidades
- Níveis de atenção (ex.: atenção primária)

---

## ▶️ Como Executar

Você precisa ter o GLPK instalado.

1. Instale o GLPK:
   - [https://www.gnu.org/software/glpk/](https://www.gnu.org/software/glpk/)

2. No terminal, execute:

```bash
glpsol -m model/hc-closest.mod -d data/hc-closest.dat
```

3. O GLPK exibirá a solução no terminal (variáveis, objetivos e alocações).

---

## 🧩 Prévia do Modelo (.mod)

```mod
#############################################################################
# Operations Research for Health Care
# TCC II
# Author: Thiago Mendanha Bahia Moura <mbm.thiago@gmail.com>
# Orientador: João Flá¡vio de Freitas Almeida <joao.flavio@dep.ufmg.br>
# LEPOINT: Laboratório de Estudos em Planejamento de Operações Integradas
# Departmento de Engenharia de Produção
# Universidade Federal de Minas Gerais - Escola de Engenharia
#############################################################################
# Health Care Facility Location Problem: Considering fixed facilities, 
...
```

---

## 📊 Prévia dos Dados (.dat)

```dat
#############################################################################
# Operations Research for Health Care
# TCC II
# Author: Thiago Mendanha Bahia Moura <mbm.thiago@gmail.com>
# Orientador: João Flá¡vio de Freitas Almeida <joao.flavio@dep.ufmg.br>
# LEPOINT: Laboratório de Estudos em Planejamento de Operações Integradas
# Departmento de Engenharia de Produção
# Universidade Federal de Minas Gerais - Escola de Engenharia
#############################################################################
# Health Care Facility Location Problem: Considering fixed facilities, 
...
```

---

## 📜 Licença

Este projeto está licenciado sob a Licença MIT. Sinta-se à vontade para reutilizar com créditos ao autor.

## ✉️ Contato

Thiago Mendanha  
[mbm.thiago@gmail.com](mailto:mbm.thiago@gmail.com)
