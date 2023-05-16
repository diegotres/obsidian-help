Você pode usar modelos para inserir trechos de texto predefinidos em sua nota ativa.

## Defina sua pasta de modelo

1. No canto inferior esquerdo, clique em **Configurações** (ícone de engrenagem).
2. Em **Plugins principais > Modelos > Localização da pasta de modelos**, insira a pasta que contém seus modelos.

## Insira um modelo na nota ativa

**Importante:** Para inserir um modelo, você precisa primeiro [[#Set your template folder]].

1. Na faixa de opções, clique em **Inserir modelo**.
2. Selecione o modelo a ser inserido na posição do cursor na nota ativa.

Se sua pasta de modelo contiver apenas uma nota, Modelos a insere diretamente na nota ativa.

## Variáveis de modelo

Você pode adicionar informações dinâmicas aos seus modelos, usando _variáveis de modelo_. Quando você insere um modelo contendo uma variável de modelo, Modelos o substitui por seu valor correspondente.

| Variable    | Description                                     |
|-------------|-------------------------------------------------|
| `{{title}}` | Title of the active note.                       |
| `{{date}}`  | Today's date. **Default format:** `YYYY-MM-DD`. |
| `{{time}}`  | Current time. **Default format:** `HH:mm`.      |

Ambos `{{date}}` e `{{time}}` permitem que você altere o formato padrão usando _format string_.

Para definir uma string de formato, adicione dois pontos (`:`) seguidos por uma string de [tokens de formato Moment.js](https://momentjs.com/docs/#/displaying/format/), por exemplo `{{ data:AAAA-MM-DD}}`.

Você pode usar `{{date}}` e `{{time}}` intercambiavelmente com strings de formato, por exemplo `{{time:YYYY-MM-DD}}`.

Você pode alterar os formatos padrão de data e hora em **Configurações > Modelos > Formato de data** e **Configurações > Modelos > Formato de hora**.

> [!tip] Dica
> Você também pode usar as variáveis de template `{{date}}` e `{{time}}` nos plugins [[Notas abertas]] e [[Criador de notas únicas]].