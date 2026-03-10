# 👥 Lista de Membros — Associação

Página institucional desenvolvida para uma associação, exibindo os membros ativos com suas informações de contato e área de atuação. Dados anonimizados para fins de portfólio.

---

## 📸 Sobre o projeto

Interface limpa e profissional no estilo de um diretório corporativo, com identidade visual da organização aplicada via CSS variables. Desenvolvida para uso interno da associação como referência rápida de contatos.

---

## ✨ Funcionalidades

- Navbar com logo e identidade visual da organização
- Hero com imagem de fundo e sobreposição
- Tabela responsiva com todos os membros
- Filtro de busca em tempo real por nome, empresa ou categoria
- Ícone de e-mail com animação de shake ao hover
- Layout adaptado para scroll horizontal em telas menores

---

## 🛠️ Tecnologias

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## 💡 Destaques técnicos

- Identidade visual configurada com **CSS custom properties** (`--brand-red`, `--brand-dark`), facilitando futuras trocas de tema
- Dados carregados via **array JavaScript** renderizado dinamicamente com `forEach` — sem dependência de backend
- Filtro implementado com busca no `textContent` completo da linha, cobrindo todos os campos de uma vez
