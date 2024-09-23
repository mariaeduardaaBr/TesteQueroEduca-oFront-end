ALGUMAS DIFICULDADES NO DESENVOLVIMENTO, NÃO TINHA TODOS OS RECURSOS INSTALADOS PARA O DESENVOLVIMENTO.

# TesteQueroEduca-oFront-end
## 📋 O Desafio

Seu objetivo é trabalhar em um projeto já iniciado, corrigindo detalhes de **CSS** e implementando funcionalidades em 
**JavaScript** com **Vue 3**. Abaixo estão as tarefas detalhadas:

### 🎨 CSS

- [ ] Ajustar o layout da página:
    - [ ] Fixar a sidebar na lateral esquerda da página 📏.
    - [ ] Definir a largura da sidebar em 220px 📏.
    - [ ] Ocultar a sidebar em telas menores 📱 _(abaixo de 1023px)_.
    - [ ] O conteúdo principal deve ocupar o espaço restante da largura da página 📏.
    - [ ] Realizar ajustes necessários no layout para otimizar a experiência do usuário 🎨.
- [ ] Ajustar a listagem de cards de ofertas:
    - [ ] Espaçamento de 16px entre os cards 📏.
    - [ ] Exibir 1 card por linha em telas pequenas 📱 _(até 639px)_.
    - [ ] Exibir 2 cards por linha em telas médias 📱 _(640px ~ 767px)_.
    - [ ] Exibir 3 cards por linha em telas grandes 📱 _(768px ~ 1023px)_.
    - [ ] Exibir 4 cards por linha em telas extra grandes 📱 _(1024px ~ 1535px)_.
    - [ ] Exibir 5 cards por linha em telas maiores 📱 _(1536px ou mais)
     
RESPOSTAS DESENVOLVIDAS DO CSS:
@tailwind base;
@tailwind components;
@tailwind utilities;

:focus {
    @apply ring-2 ring-primary-pure/80 ring-offset-2 ring-offset-white/80 outline-0 transition;
}

:focus:hover {
    @apply ring-offset-4
}
  /* Estilos gerais da página */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Sidebar */
.sidebar {
    position: fixed;
    width: 220px;
    height: 100%;
    background-color: #f4f4f4; /* Cor de fundo da sidebar */
    transition: transform 0.3s ease; /* Animação suave ao ocultar */
}

/* Ocultar a sidebar em telas menores */
@media (max-width: 1023px) {
    .sidebar {
        transform: translateX(-100%); /* Oculta a sidebar */
    }
}

/* Conteúdo principal */
.main-content {
    margin-left: 220px; /* Espaço para a sidebar */
    padding: 16px; /* Padding interno do conteúdo */
}

/* Ajustes para telas menores */
@media (max-width: 1023px) {
    .main-content {
        margin-left: 0; /* Remove a margem da sidebar */
    }
}

/* Listagem de cards de ofertas */
.cards-container {
    display: grid;
    gap: 16px; /* Espaçamento entre os cards */
}

/* Exibir 1 card por linha em telas pequenas */
@media (max-width: 639px) {
    .cards-container {
        grid-template-columns: 1fr; /* 1 card por linha */
    }
}

/* Exibir 2 cards por linha em telas médias */
@media (min-width: 640px) and (max-width: 767px) {
    .cards-container {
        grid-template-columns: repeat(2, 1fr); /* 2 cards por linha */
    }
}

/* Exibir 3 cards por linha em telas grandes */
@media (min-width: 768px) and (max-width: 1023px) {
    .cards-container {
        grid-template-columns: repeat(3, 1fr); /* 3 cards por linha */
    }
}

/* Exibir 4 cards por linha em telas extra grandes */
@media (min-width: 1024px) and (max-width: 1535px) {
    .cards-container {
        grid-template-columns: repeat(4, 1fr); /* 4 cards por linha */
    }
}

/* Exibir 5 cards por linha em telas maiores */
@media (min-width: 1536px) {
    .cards-container {
        grid-template-columns: repeat(5, 1fr); /* 5 cards por linha */
    }
}

.

