# 📟 Calculadora com Vue.js

Uma calculadora funcional desenvolvida com **Vue 3 + Vite**, utilizando componentização, reatividade e comunicação entre componentes.

Projeto desenvolvido para consolidar conceitos de arquitetura em aplicações SPA, gerenciamento de estado e lógica aplicada à interface.

---

## 🌐 Demo Online

Acesse o projeto publicado:
https://calculadora-com-vue-eight.vercel.app/

---

## 🚀 Tecnologias Utilizadas

* Vue 3 (Composition API)
* Vite
* JavaScript
* CSS customizado (Neumorphism Dark UI)
* Componentização

---

## 🧠 Conceitos Aplicados

✔ Reactive State (`reactive`)
✔ Props
✔ Emissão de eventos (`emit`)
✔ Comunicação entre componentes
✔ Manipulação de eventos (`@click`)
✔ Escuta de teclado físico (`keydown`)
✔ Ciclo de vida (`onMounted` / `onBeforeUnmount`)
✔ Separação de responsabilidades entre componentes
✔ Controle de fluxo de dados em aplicações reativas

---

## 🧩 Estrutura do Projeto

```
src/
│
├── components/
│   ├── Display.vue
│   └── Botoes.vue
│
├── App.vue
└── main.js
```

### 🔹 Display.vue

Responsável apenas por exibir o valor atual da calculadora.

### 🔹 Botoes.vue

Renderiza os botões e emite eventos para o componente pai.

### 🔹 App.vue

Gerencia o estado global e contém toda a lógica de cálculo.

---

## ⚙️ Funcionalidades

* Operações matemáticas básicas:

  * Soma (+)
  * Subtração (-)
  * Multiplicação (*)
  * Divisão (/)
* Limpar operação (C)
* Cálculo ao pressionar "="
* Suporte ao teclado físico:

  * Números
  * Operadores
  * Enter (=)
  * Backspace (limpar)

---

## 🎨 Interface

Interface em estilo **Dark Neumorphism**, com:

* Sombreamento interno e externo
* Feedback visual ao pressionar botões
* Layout centralizado simulando calculadora real

---

## 📋 Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

* Node.js (versão 18 ou superior)
* npm ou yarn

---

## 📦 Como Rodar o Projeto

```bash
npm install
npm run dev
```

Depois acesse:

```
http://localhost:5173
```

---

## 🛠 Scripts Disponíveis

| Comando         | Função                             |
| --------------- | ---------------------------------- |
| npm run dev     | Inicia ambiente de desenvolvimento |
| npm run build   | Gera build de produção             |
| npm run preview | Visualiza build local              |

---

## 📌 Objetivo do Projeto

Este projeto foi criado para:

* Explorar reatividade no Vue 3
* Praticar componentização real
* Simular fluxo de dados de aplicações SPA
* Reforçar lógica aplicada à interface
* Construir um projeto funcional para portfólio

---

## 🔮 Melhorias Futuras

* Suporte a números decimais
* Histórico de operações
* Alternância de tema (dark/light)
* Melhorias de acessibilidade
* Tratamento de divisão por zero
* Responsividade para mobile

---

## 👨‍💻 Autor

Desenvolvido por **Uillian De Freitas**
Projeto de prática e evolução como Desenvolvedor Front-End.
