# ✅ Checklist — Jornada de Clientes

Checklist interativo para acompanhamento da jornada de novos clientes, com dois modos de visualização, sistema de modais e progresso salvo automaticamente. Dados anonimizados para fins de portfólio.

---

## ✨ Funcionalidades

- **Dois modos de jornada** — alternância entre "Jornada Padrão" e "Assessoria de Novo Produto" com fases e cores distintas
- **5 fases por modo** — cada jornada cobre do kickoff ao encerramento formal do projeto
- **Timeline visual** — fases organizadas em linha do tempo com numeração e cor por tipo
- **Modais com sub-itens** — botão ↗ abre detalhes de cada entregável sem perder o estado dos checkboxes
- **Progresso em tempo real** — barra e percentual atualizados a cada item marcado, contando apenas as fases visíveis do modo ativo
- **Salvamento automático** — progresso persistido via localStorage, mantido ao recarregar a página
- **DOM Portal** — sub-listas são movidas fisicamente para o modal e devolvidas ao fechar, preservando o estado

---

## 🗂️ Estrutura das Jornadas

**Jornada Padrão**
1. Setup & Kickoff
2. Levantamento de Requisitos
3. Implantação
4. Treinamento
5. Go-live & Encerramento

**Assessoria de Novo Produto**
1. Setup & Kickoff
2. Definição do Produto
3. Desenvolvimento
4. Lançamento
5. Pós-lançamento

---

## 🛠️ Tecnologias

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## 💡 Destaques técnicos

- **DOM Portal** — em vez de clonar os sub-itens para o modal, o elemento é movido com `appendChild` e devolvido com `originalParent.appendChild` ao fechar, garantindo que o estado dos checkboxes seja preservado sem precisar sincronizar nada
- **IDs gerados dinamicamente** — `generateUniqueIDs()` percorre todos os `.check-item` e atribui `data-id` únicos em tempo de execução, desacoplando o salvamento da estrutura do HTML
- **Modos com CSS classes** — a alternância entre jornadas é feita adicionando/removendo classes `.std` e `.adv` nos elementos, mantendo toda a lógica visual no CSS
- **Progresso inteligente** — `updateDashboard()` ignora fases com `.hidden` no cálculo, garantindo que o percentual reflita apenas os itens visíveis no modo ativo
- **setMode com forEach** — as fases são controladas em arrays, evitando repetição de código ao mostrar/esconder múltiplos elementos
