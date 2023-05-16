O compositor de notas permite mesclar duas notas ou extrair parte de uma nota em uma nova nota.

## Mesclar notas

Mesclar notas adiciona uma nota a outra e remove a primeira. O compositor de notas atualiza todos os links para fazer referência à nota mesclada.

Ao selecionar a nota para mesclar, você pode escolher entre os seguintes métodos:

- `Enter`: Adiciona a nota de origem no _end_ à nota de destino.
- `Shift+Enter`: Adiciona a nota de origem no _início_ da nota de destino.
- `Ctrl+Enter` (ou `Cmd+Enter` no macOS): Cria uma nova nota com o conteúdo da nota de origem.

Para mesclar a nota ativa com outra nota em seu cofre:

**Explorador de arquivos**

1. No explorador de arquivos, clique com o botão direito do mouse na nota que deseja mesclar.
2. Clique em **Mesclar arquivo inteiro com...**.
3. Selecione a nota que deseja mesclar.
4. Clique em **Mesclar** para confirmar.

**Paleta de comandos**

1. Abra a [[Paleta de comandos]].
2. Selecione **Note composer: Mesclar arquivo atual com outro arquivo...**.
3. Selecione a nota que deseja mesclar.
4. Clique em **Mesclar** para confirmar.

> [!tip] Dica
> Por padrão, o compositor de notas pede que você confirme ao mesclar notas. Se você desativar a confirmação e mesclar uma nota por engano, ainda poderá recuperá-la com o plugin [[Recuperação de arquivos]].

## Extrair nota

Ao selecionar a nota para extrair a seleção, você pode escolher entre os seguintes métodos:

- `Enter`: Adiciona o texto selecionado no _end_ à nota de destino.
- `Shift+Enter`: Adiciona o texto selecionado no _início_ da nota de destino.
- `Ctrl+Enter` (ou `Cmd+Enter` no macOS): Cria uma nova nota com o texto selecionado.

Para extrair texto em uma nova nota:

**Editor**

1. Na **Visualização de edição**, selecione o texto que deseja extrair.
2. Clique com o botão direito do mouse no texto selecionado.
3. Clique em **Extrair seleção atual...**.
4. Selecione a nota para a qual deseja extrair.

**Paleta de comandos**

1. Na **Visualização de edição**, selecione o texto que deseja extrair.
2. Abra a [[Paleta de comandos]].
3. Selecione **Note composer: Extract current selection...**.
4. Selecione a nota para a qual deseja extrair.

> [!tip] Dica
> Por padrão, o compositor de notas substitui o texto extraído por um link para a nota de destino. Nas configurações, você também pode alterar para [[Incorporando arquivos|embed]] a nota de destino ou não deixar nada para trás.

## Arquivo de modelo

Ao configurar um modelo, você pode personalizar o conteúdo antes de adicioná-lo à nova nota. Para usar um modelo, insira um **localização do arquivo de modelo** nas configurações do plug-in.

O modelo pode conter as seguintes variáveis:

| Variable          | Description                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `{{content}}`     | The content to merge, or the extracted text selection. If you don't include this variable, Note composer adds the content at the bottom of the template. |
| `{{fromTitle}}`   | Name of the source note.                                                                                                                                 |
| `{{newTitle}}`    | Name of the destination note. For example, to add the file name as a heading at the top of the file.                                                     |
| `{{date:FORMAT}}` | Creation date of the new note. For example, `{{date:YYYY-MM-DD}}`.                                                                                       |
