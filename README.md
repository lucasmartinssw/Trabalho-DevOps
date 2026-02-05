# 🚀 Projeto: Portfólio Profissional (Laboratório de CI/CD)

![CI/CD Status](https://github.com/lucasmartinssw/Trabalho-DevOps/actions/workflows/deploy.yml/badge.svg)

> **⚠️ AVISO IMPORTANTE:** Este projeto foi desenvolvido exclusivamente para fins educacionais como parte da disciplina de **DevOps**. O conteúdo do portfólio (experiências e projetos) é fictício, servindo apenas como base tecnológica para o estudo de pipelines de Integração e Entrega Contínua (CI/CD).

---

## 📋 Descrição do Projeto

Este repositório contém um portfólio profissional estático, construído com HTML5 e CSS3. O foco central deste trabalho é a implementação de uma infraestrutura de automação robusta utilizando **GitHub Actions**, simulando um ambiente de entrega de produto real para um servidor de produção.

### Principais Tecnologias
* **Front-end:** HTML5, CSS3, Font Awesome (Biblioteca de ícones).
* **DevOps/CI:** GitHub Actions, Matrix Strategy (Node.js 18 & 20), Shell Scripting.
* **CD/Deployment:** GitHub Pages.

---

## 🛠️ Estrutura do Repositório

Para garantir a integridade da pipeline, o projeto segue rigorosamente a estrutura de diretórios abaixo:

```text
meu-portfolio/
├── .github/workflows/  # Configurações da Pipeline (deploy.yml)
├── assets/
│   └── imagens/        # Pasta dedicada para mídia e fotos
├── index.html          # Ponto de entrada obrigatório na raiz
├── style.css           # Folha de estilos centralizada
└── README.md           # Documentação e badges
```


## ⚙️ Regras de Automação (Pipeline)
A pipeline configurada neste repositório assegura a qualidade através de etapas rigorosas:

1. Integração Contínua (CI)
* **Validada em cada Pull Request para a branch principal. O código é rejeitado se:**

* **Check de Arquivo: O arquivo index.html for movido ou renomeado.**

* **Linter: O código HTML apresentar má estruturação.**

* **Peso de Arquivos: Existir qualquer arquivo individual acima de 500KB (otimização de ativos).**

* **Segurança e Limpeza: Forem encontrados comentários como TODO, FIXME ou termos sensíveis como senha e password.**

* **Integridade de Links: Tags de link ou caminhos de imagem estiverem quebrados ou inválidos.**

* **Matrix Strategy: O Job de validação é executado simultaneamente em Node.js 18 e Node.js 20.**

2. Entrega Contínua (CD)
* **Uma vez que o código é aprovado e unido à branch main, o deploy é disparado automaticamente para o GitHub Pages sem intervenção manual.**

## 🚀 Link de Acesso
O portfólio oficial publicado pela pipeline pode ser visualizado aqui:

## 👉 VER PORTFÓLIO ONLINE

## 👥 Colaboradores
Desenvolvedor: Lucas Martins

Colaboradora Convidada: 09116428-collab (Revisão de DevOps)

## 🛠 Como testar falhas?
Para validar os gatilhos de erro da pipeline (ficando vermelha):

- Adicione um arquivo de imagem pesado (> 500KB).

- Insira um comentário `` no HTML.

- Renomeie o arquivo index.html para home.html.