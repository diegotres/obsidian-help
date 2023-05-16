O plug-in de pesquisa ajuda a encontrar arquivos em seu cofre.

Por padrão, você pode encontrar a Pesquisa na barra lateral esquerda (ícone de lupa). Você também pode abrir a Pesquisa pressionando `Ctrl+Shift+F` (ou `Cmd+Shift+F` no macOS).

- **Pesquisar texto selecionado**: Se você selecionar o texto no editor e abrir a Pesquisa com o atalho do teclado, a Pesquisa mostrará os resultados da pesquisa para o texto selecionado.
- **Pesquisar termos de pesquisa recentes**: abra a Pesquisa com um termo de pesquisa vazio para listar os termos de pesquisa recentes. Clique em qualquer um deles para usar o termo de pesquisa novamente.

## Termos de pesquisa

Um termo de pesquisa é a palavra ou frase que você insere no campo de pesquisa. Aprender a escrever termos de pesquisa de forma eficaz pode ajudá-lo a encontrar rapidamente o que procura, mesmo em grandes cofres. O Obsidian pesquisa apenas o conteúdo de notas e telas.

> [!tip] Pesquisando caminhos e nomes de arquivos
> Por padrão, você só pode pesquisar os caminhos e nomes de arquivos de notas e telas. Para procurar um caminho ou nome de arquivo de qualquer arquivo no vault, use o operador `path` ou `file`.

Cada palavra no termo de pesquisa é correspondida independentemente dentro de cada arquivo. Para procurar uma frase exata, coloque-a entre aspas, por exemplo `"star wars"`. Para pesquisar o texto citado dentro de uma frase exata, você pode _escapar_ das aspas adicionando uma barra invertida (`\`) na frente da citação, por exemplo `"eles disseram \"olá\" um ao outro"`.

Você pode controlar se deseja retornar arquivos que contenham _todas_ as palavras em seu termo de pesquisa ou _qualquer_ das palavras:

- `reunião de trabalho` retorna arquivos que contêm tanto `reunião` quanto `trabalho`.
- `meeting OR work` retorna arquivos que contêm `meeting` ou `work`.

Você pode até combinar os dois no mesmo termo de pesquisa.

- `reunião de trabalho OU encontro pessoal` retorna arquivos para reuniões de trabalho e encontros pessoais.

Você pode usar parênteses para controlar a prioridade de cada expressão.

- `reunião (trabalho OU encontro) pessoal` retorna arquivos que contêm `reunião`, `pessoal` e `trabalho` ou `encontro`.

Para excluir uma palavra dos resultados da pesquisa, adicione um hífen (`-`) na frente dela:

- `meeting -work` retorna arquivos que contêm `meeting`, mas não `work`.

> [!tip] Explique o termo de pesquisa
> Se precisar solucionar um termo de pesquisa complexo, você pode clicar em **Explicar termo de pesquisa** no painel Pesquisar para obter uma explicação do termo de pesquisa.

## Operadores de pesquisa

Os operadores de pesquisa permitem consultas de pesquisa mais refinadas para filtrar ainda mais seus resultados.

Alguns operadores até permitem que você adicione um termo de pesquisa aninhado entre parênteses, por exemplo: `task:(chamada OU email)`.

| Search operator | Description                                                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file:`         | Find text in filename. Matches any file in the vault.<p/>Example: `file:.jpg` or `file:202209`.                                                                                                                                                     |
| `path:`         | Find text in file path. Matches any file in the vault.<p/>Example: `path:"Daily notes/2022-07"`.                                                                                                                                                    |
| `content:`      | Find text in file content.<p/>Example: `content:"happy cat"`.                                                                                                                                                        |
| `match-case:`   | Case-sensitive match.<p/>Example: `match-case:HappyCat`.                                                                                                                                                             |
| `ignore-case:`  | Case-insensitive match.<p/>Example: `ignore-case:ikea`.                                                                                                                                                              |
| `tag:`          | Find tag in file.<p/>Example: `tag:#work`.<p/>**Note**: Since `tag:` ignores matches in code blocks and in non-Markdown content, it's often faster and more accurate than a normal full-text search for `#work`.     |
| `line:`         | Find matches on the same line.<p/>Example: `line:(mix flour)`.                                                                                                                                                       |
| `block:`        | Find matches in the same block.<p/>Example: `block:(dog cat)`.<p/>**Note**: Since `block:` requires Search to parse the Markdown content in every file, it can cause your search term to take longer time to finish. |
| `section:`      | Find matches in the same section (text between two headings).<p/>Example: `section:(dog cat)`.                                                                                                                         |
| `task:`         | Find matches in a [[Sintaxe de formatação básica#Task lists|task]] on a block-by-block basis.<p/>Example: `task:call`.                                                                                                          |
| `task-todo:`    | Find matches in an *uncompleted* [[Sintaxe de formatação básica#Task lists|task]] on a block-by-block basis.<p/>Example: `task-todo:call`.                                                                                      |
| `task-done:`    | Find matches in a *completed* [[Sintaxe de formatação básica#Task lists|task]] on a block-by-block basis.<p/>Example: `task-done:call`.                                                                                         |

## Use expressões regulares em termos de pesquisa

Uma expressão regular é um conjunto de caracteres que descreve um padrão de texto. Para usar expressões regulares em seu termo de pesquisa, coloque a expressão entre barras (`/`).

- `/\d{4}-\d{2}-\d{2}/` corresponde a uma data ISO 8601, como 2022-01-01.

Você pode até combinar expressões regulares com operadores de pesquisa:

- `path:/\d{4}-\d{2}-\d{2}/` retorna arquivos com uma data no caminho do arquivo.

Para obter mais informações sobre como escrever expressões regulares, consulte [Expressões regulares](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

> [!note] Nota
> As expressões regulares vêm em diferentes tipos que podem parecer diferentes umas das outras. Obsidian usa expressões regulares com sabor de JavaScript.

## Definir configurações de pesquisa

Para configurar a pesquisa, use as configurações na parte superior do painel de pesquisa:

| Setting                 | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| **Match case**          | Toggles case-sensitive matching.                                            |
| **Explain search term** | Breaks down the search terms and explains it in plain text.                 |
| **Collapse results**    | Toggles whether to show the search context.                                 |
| **Show more context**   | Expands the search result to show more text around the match.               |
| **Change sort order**   | Change the order of the search results.                                     |
| **Copy search results** | Convert and copy the search results as a Markdown list with optional links. |

## Incorpore os resultados da pesquisa em uma nota

Para incorporar os resultados da pesquisa em uma nota, adicione um bloco de código `query`:

<pre><code>```query
embed OR search
```</code></pre>

Por exemplo:

> [!note] Nota
> [[Introdução ao Obsidian Publish|Obsidian Publish]] não suporta resultados de pesquisa incorporados. Para ver o exemplo, abra a Ajuda do Obsidian localmente dentro do Obsidian.
```query
embed OR search
```
