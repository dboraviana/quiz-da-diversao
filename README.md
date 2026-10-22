# Quiz da Diversão

Um jogo de perguntas e respostas responsivo, feito em HTML, CSS e JavaScript puro. Não precisa instalar dependências nem configurar servidor.

## Testar no computador
1. Baixe e extraia o ZIP.
2. Abra `index.html` no navegador.

## Publicar com GitHub Pages
1. Entre em https://github.com e crie um repositório público chamado `quiz-da-diversao`.
2. Envie `index.html`, `quiz.html`, `tabuada.html` e `questions.js` para a raiz do repositório (`README.md` também pode ser enviado).
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`, depois clique em **Save**.
6. Aguarde a publicação. O endereço será parecido com `https://SEU-USUARIO.github.io/quiz-da-diversao/`.

## Abrir no iPad
Abra o endereço publicado no Safari. Para criar um ícone na tela inicial:
1. Toque em **Compartilhar**.
2. Escolha **Adicionar à Tela de Início**.
3. Confirme o nome e toque em **Adicionar**.

## Personalizar as perguntas
A página inicial lista os jogos disponíveis. O primeiro é o **Quiz**. Antes de cada rodada, escolha a quantidade de perguntas (10, 20 ou 30). Os temas disponíveis ficam listados como referência, e as perguntas são sorteadas aleatoriamente entre todos eles, sem repetição na mesma rodada. No resultado, acertos, erros e perguntas não respondidas são contados separadamente. As perguntas ficam separadas da lógica do jogo no arquivo `questions.js`. Para adicionar ou editar uma pergunta, altere a lista `window.quizQuestions`, seguindo este formato:

```js
{
  id: "animal-cat",
  category: "Animais",
  emoji: "🐾",
  question: "Qual animal mia?",
  choices: ["Cachorro", "Gato", "Peixe", "Cavalo"],
  answer: 1,
  explanation: "O gato mia!"
}
```

Cada pergunta tem um `id` único, que poderá ajudar a identificar registros em uma futura tela de cadastro. `answer` é o índice da resposta correta começando em zero: `0` para a primeira opção, `1` para a segunda e assim por diante. Inclua quatro opções em `choices` e informe a categoria e o emoji dessa categoria.

Os temas são gerados automaticamente a partir das categorias cadastradas em `questions.js`; ao criar uma nova categoria, não é necessário adicionar um filtro manualmente.

## Jogo de tabuada
Na página inicial, escolha **Tabuada** para acessar o jogo. Você pode iniciar um treino fixo de 10 perguntas com adição, subtração, divisão ou multiplicação, nos níveis fácil, médio e intermediário, ou visualizar as tabuadas de multiplicação do 1 ao 10. Respostas erradas mostram uma explicação passo a passo.
