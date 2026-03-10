# 📊 Status Report — Cronograma Executivo (Tema Claro e Escuro)

Dashboard de cronograma executivo em formato Gantt, desenvolvido para acompanhamento de projetos de BI com clientes. Dados anonimizados para fins de portfólio.

O projeto foi entregue em **duas versões visuais**, criadas propositalmente para que o cliente pudesse escolher qual enviar internamente — uma decisão de UX que vai além do código.

---

## 🎨 As duas versões

| | Tema Escuro | Tema Claro |
|---|---|---|
| **Fundo** | `#0f0f0f` | `#ffffff` |
| **Contexto ideal** | Apresentações executivas, ambientes com luz controlada | Impressão, e-mail, reuniões com projetor |
| **Destaque** | Alto contraste, pins com glow | Visual limpo e institucional |

---

## ✨ Funcionalidades

- Cronograma em formato **Gantt** com pins de status por sprint
- **3 estados visuais** com animação de pulse nos pins ativos: Concluído, Em andamento e A iniciar
- Coluna de tarefas fixada (sticky) durante scroll horizontal
- Caixa de alerta para pontos de atenção do projeto
- Layout responsivo com scroll horizontal em telas menores

---

## 🛠️ Tecnologias

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)

---

## 💡 Destaques técnicos

- **CSS Grid** — layout do Gantt feito com `grid-template-columns: 250px repeat(7, 1fr)`, sem nenhuma biblioteca externa
- **Sticky column** — a coluna de tarefas usa `position: sticky; left: 0; z-index: 2` para permanecer visível durante o scroll horizontal
- **Animação pulse** — o efeito de pulsação nos pins é feito com `::after` + `@keyframes`, usando `background: inherit` para herdar a cor do pin pai sem repetir valores
- **CSS custom properties** — toda a paleta de cores está em variáveis no `:root`, tornando a troca entre tema claro e escuro uma questão de trocar apenas os valores das variáveis
