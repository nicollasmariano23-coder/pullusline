# CodeQL Lab — Pipeline CI/CD com GitHub Actions

Projeto desenvolvido para estudo de **Pipeline CI/CD** com foco em **Segurança da Informação**, utilizando **GitHub Actions** e **CodeQL** para análise automatizada de segurança.

Este repositório demonstra uma pipeline com três etapas principais:

1. Análise de segurança com CodeQL
2. Execução de testes automatizados
3. Simulação de deploy para ambiente de stage

---

## Objetivo

O objetivo deste projeto é criar uma pipeline CI/CD capaz de validar automaticamente o código enviado ao repositório.

A pipeline foi criada para:

* verificar vulnerabilidades no código com CodeQL;
* executar testes automatizados;
* validar o funcionamento básico do projeto;
* simular uma etapa de deploy;
* demonstrar boas práticas de integração contínua e segurança.

---

## Tecnologias utilizadas

* GitHub
* GitHub Actions
* CodeQL
* Python
* Flask
* Pytest
* Flake8

---

## Estrutura do repositório

```text
codeql-lab/
├── .github/
│   └── workflows/
│       └── codeql.yml
├── tests/
│   └── test_main.py
├── code.py
├── requirements.txt
└── README.md
```

---

## Arquivo principal

O arquivo principal do projeto é:

```text
code.py
```

Ele contém uma aplicação simples em Python com Flask.

O projeto também possui um exemplo de código utilizado para demonstrar a análise de segurança feita pelo CodeQL.

---

## Pipeline CI/CD

A pipeline está configurada no arquivo:

```text
.github/workflows/codeql.yml
```

Ela é executada automaticamente quando ocorre alteração no repositório, como um `push` para a branch principal.

A pipeline é composta por três Jobs:

```text
Job 1 → Análise CodeQL
Job 2 → Testes Automatizados
Job 3 → Deploy para Stage
```

---

## Job 1 — Análise CodeQL

O primeiro Job executa a análise de segurança do código usando o CodeQL.

Essa etapa tem como objetivo identificar possíveis vulnerabilidades no projeto antes que o código avance para as próximas etapas.

Exemplos de vulnerabilidades que podem ser identificadas:

* SQL Injection
* Command Injection
* uso inseguro de dados de entrada
* falhas de segurança em código Python
* más práticas de desenvolvimento seguro
Imagem de identificação de vunerabilidade
<img width="1446" height="347" alt="image" src="https://github.com/user-attachments/assets/a6f5eddd-1c5d-4fa6-b95a-08d5b0e996df" />

---

## Job 2 — Testes Automatizados

O segundo Job executa os testes automatizados do projeto.

Os testes ficam na pasta:

```text
tests/
```

O comando utilizado para rodar os testes é:

```bash
pytest tests/ -v
```

Essa etapa garante que o código continue funcionando corretamente após alterações.

---

## Job 3 — Deploy para Stage

O terceiro Job simula um deploy para o ambiente de stage.

Essa etapa representa o envio da aplicação para um ambiente de testes ou homologação.

O deploy só deve acontecer se as etapas anteriores forem concluídas com sucesso.

---

## Fluxo da pipeline

O funcionamento esperado da pipeline é:

```text
Código enviado para o GitHub
        ↓
Análise de segurança com CodeQL
        ↓
Execução dos testes automatizados
        ↓
Deploy simulado para stage
```

Se alguma etapa falhar, as próximas etapas não devem ser executadas.

---

## Dependências do projeto

As dependências estão no arquivo:

```text
requirements.txt
```

Para instalar as dependências localmente, utilize:

```bash
pip install -r requirements.txt
```

---

## Como executar localmente

Clone o repositório:

```bash
git clone https://github.com/GusDUGrau/codeql-lab.git
```

Entre na pasta do projeto:

```bash
cd codeql-lab
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Execute os testes:

```bash
pytest tests/ -v
```

---

## Como verificar a pipeline

Para verificar a execução da pipeline no GitHub:

1. Acesse o repositório
2. Clique na aba **Actions**
3. Selecione a execução mais recente
4. Verifique o status de cada Job

Legenda:

```text
Verde    → execução concluída com sucesso
Vermelho → ocorreu falha
Amarelo  → execução em andamento
```

---

## Como verificar alertas de segurança

Os alertas do CodeQL podem ser vistos na aba:

```text
Security → Code scanning alerts
```

Nessa área, o GitHub mostra detalhes sobre possíveis vulnerabilidades encontradas no código.

---

# Evidências da Pipeline

Nesta seção estão as evidências do funcionamento da pipeline.

Adicione abaixo os prints das execuções realizadas no GitHub Actions.

---

## 1. Pipeline executada com sucesso

Adicione aqui o print mostrando a pipeline com os Jobs concluídos com sucesso.

```text
Inserir print aqui
```

---

## 2. Job de Análise CodeQL

Adicione aqui o print do Job responsável pela análise de segurança com CodeQL.

```text
Inserir print aqui
```
<img width="1853" height="907" alt="image" src="https://github.com/user-attachments/assets/9ee54b9e-9f61-42a8-b747-66800bcad075" />

---

## 3. Job de Testes Automatizados

Adicione aqui o print do Job responsável pela execução dos testes automatizados.

```text
Inserir print aqui
```
<img width="1301" height="566" alt="image" src="https://github.com/user-attachments/assets/f4e2f2fe-b6a1-486a-8d1b-5f373dd5000b" />

---


## 4. Alertas de segurança no CodeQL

Adicione aqui o print da aba **Security → Code scanning alerts**, caso existam alertas detectados pelo CodeQL.

```text
Inserir print aqui
```
<img width="1446" height="347" alt="image" src="https://github.com/user-attachments/assets/56bcbce9-eb22-42b1-8050-a0d201fa3a3c" />

---

## 5. Correção da vulnerabilidade

Adicione aqui o print mostrando que, após a correção do código, a pipeline voltou a executar com sucesso.

```text
Inserir print aqui
```

---

## Comandos Git utilizados

Durante o desenvolvimento do projeto, foram utilizados comandos básicos do Git:

```bash
git status
git add .
git commit -m "ci: adiciona pipeline com CodeQL"
git push origin main
```

---


## Autor

**Nicollas Gabriel**

Projeto acadêmico desenvolvido para estudo de **CI/CD**, **GitHub Actions** e **CodeQL**.

---

## Conclusão

Este projeto demonstra a criação de uma pipeline CI/CD utilizando GitHub Actions e CodeQL.

A estrutura permite automatizar a análise de segurança, executar testes e simular um deploy, contribuindo para um processo de desenvolvimento mais seguro e organizado.
