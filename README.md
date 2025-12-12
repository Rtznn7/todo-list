Este projeto é uma lista de tarefas funcional, construída com HTML, CSS e JavaScript puro (Vanilla JS).
Ele permite criar, marcar como concluída e remover tarefas, além de salvar tudo no LocalStorage, para que nada se perca ao recarregar a página.

 Funcionalidades

Adicionar tarefas pressionando Enter

Marcar como concluídas usando checkbox

Remover tarefas clicando no botão "X"

Salvar automaticamente no LocalStorage

Interface simples e responsiva

Tema com cores configuráveis via CSS :root

 Como funciona internamente
 LocalStorage

O projeto usa duas funções fundamentais:

getBanco() → busca os dados salvos

setBanco(banco) → atualiza o LocalStorage

Isso mantém tudo salvo no navegador sem precisar de backend.

 Renderização dinâmica

A função atualizarTela() recria a lista inteira sempre que algo muda.
É simples, eficiente e evita bugs comuns de DOM mal manipulado.
 Eventos principais

keypress dentro de newItem

click dentro de todoList

Isso evita precisar adicionar evento em cada item individual.

Estrutura dos arquivos
/projeto
│── index.html
│── style.css
│── app.js
└── img.jpg   (imagem de fundo)

HTML

Estrutura limpa, apenas o essencial: título, lista e input para adicionar tarefas.

 CSS

Variáveis globais com :root

Layout centrado

Responsividade simples (baseada em vw)

Efeitos de hover

Imagem de fundo aplicada corretamente:

body {
    background: url("img.jpg");
    background-size: cover;
    background-position: center;
}


Se a imagem não aparecer, é porque o arquivo não está no mesmo diretório ou tem nome diferente.
Não adianta mexer no CSS se o arquivo não estiver no lugar certo.

 JavaScript

Código organizado em funções pequenas:

criarItem()

limparTarefas()

atualizarTela()

inserirItem()

removerItem()

atualizarItem()

clickItem()
