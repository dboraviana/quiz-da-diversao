# Quiz da Diversão

Um jogo de perguntas e respostas responsivo, feito em HTML, CSS e JavaScript puro. Não precisa instalar dependências nem configurar servidor.

## Testar no computador
1. Baixe e extraia o ZIP.
2. Abra `index.html` no navegador.

## Publicar com GitHub Pages
1. Entre em https://github.com e crie um repositório público chamado `quiz-da-diversao`.
2. Envie o arquivo `index.html` para a raiz do repositório (o `README.md` também pode ser enviado).
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
No `index.html`, procure `const allCards = [` perto do fim do arquivo. Cada cartão segue um destes formatos:

### Múltipla escolha
```js
{
  category: "Animais",
  emoji: "🐾",
  type: "choice",
  question: "Qual animal mia?",
  choices: ["Cachorro", "Gato", "Peixe", "Cavalo"],
  answer: 1,
  explanation: "O gato mia!"
}
```
`answer` é o índice da resposta correta começando em zero: `0` para a primeira opção, `1` para a segunda e assim por diante.

### Revelar resposta
```js
{
  category: "Ciência",
  emoji: "🔬",
  type: "reveal",
  question: "Qual estrela ilumina a Terra?",
  answerText: "O Sol",
  explanation: "O Sol é a estrela mais próxima da Terra."
}
```

Categorias iniciais: `Animais`, `Ciência`, `Mundo` e `Lógica`. Se criar outra categoria, adicione também um botão de filtro no HTML ou use `Todas`.
