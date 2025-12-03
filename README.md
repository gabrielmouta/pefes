# PEFES — Prompt Engineering for Epidemiological Surveillance  
**LLM Framework for Reproducible and Validated Epidemiological Analyses using Data Dictionary-Based Analysis**
**Framework de LLM para Análises Epidemiológicas Reprodutíveis e Validadas por Dicionários de Dados**

A dictionary-validated, structured system for safe generation of epidemiological analysis scripts using Large Language Models (LLMs).  
Um sistema estruturado e validado por dicionários oficiais para geração segura de scripts epidemiológicos com LLMs.

---

# ENGLISH VERSION

## Overview
PEFES is a reproducible, dictionary-grounded framework that transforms natural language epidemiological questions into validated analysis scripts using Large Language Models (LLMs).  
It ensures:
- strict adherence to dataset dictionaries
- validated variable usage
- deterministic flow of reasoning
- safe generation of R, Python, or SQL scripts
- transparency and full reproducibility for scientific use

---

## Repository Structure

/
├── instruction.json
│   
├── dictionaries/
│   ├── sinan_dengue.json
│   ├── sivep.json
│   └── additional dictionaries (...)
└── README.md

---

## Description of Components

### instruction.json
Defines PEFES’ internal logic:
- LLM role and objectives
- plan_vars → answer execution flow
- strict variable validation against dictionaries
- fallback logic
- municipal code harmonization guidelines
- script generation rules
- constraints (no external data, no execution, no fabricated variables)

### dictionaries/
Each JSON dictionary includes:
- variable names
- allowed values and labels
- formats and types
- constraints for valid analytical usage

---

## Scientific Motivation
Public health datasets (e.g., SINAN, SIVEP) are large, complex, and heterogeneous.  
PEFES addresses key challenges:
- variable name inconsistencies
- risk of hallucinations in LLMs
- lack of reproducibility in LLM-generated code

---

## How to Use PEFES with an LLM

1. Open ChatGPT or another LLM that supports system prompts.
2. Paste:
   - instruction.json
   - one or more dictionary JSONs
3. Ask epidemiological questions in natural language.

Examples:
- “Compare dengue hospitalizations by sex and age group from 2018 to 2023.”
- “Generate an R script to summarize severe dengue cases by municipality.”

---

## Citation (English)

TODO

---

# PORTUGUÊS

## Visão Geral
O PEFES é um framework baseado em dicionários e projetado para transformar perguntas epidemiológicas em linguagem natural em scripts validados.

---

## Estrutura do Repositório

/
├── instruction.json
│   
├── dictionaries/
│   ├── sinan_dengue.json
│   ├── sivep.json
│   └── outros dicionários (...)
└── README.md

---

## Componentes

### instruction.json
Define:
- papel e objetivos do LLM
- fluxo plan_vars → answer
- validação rígida das variáveis
- fallback
- padronização dos códigos municipais
- regras para gerar scripts
- restrições de segurança

### dictionaries/
Incluem:
- variáveis oficiais
- valores permitidos
- tipos e formatos

---

## Como Usar

1. Abrir ChatGPT.
2. Inserir instruction.json e dicionários.
3. Fazer perguntas epidemiológicas.

Exemplos:
- “Compare hospitalizações por dengue por sexo de 2018 a 2023.”
- “Gere um script em R para casos graves por município.”

---

## Citação (Português)

TODO

