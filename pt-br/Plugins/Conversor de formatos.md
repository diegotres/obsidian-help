O conversor de formato permite converter o Markdown de outros aplicativos para o formato Obsidian.

> [!warning] Aviso
> Conversor de formato converte todo o seu cofre com base em suas configurações. Faça backup de suas anotações antes de realizar a conversão.

Para converter todas as notas em seu cofre:

1. Na faixa de opções, clique em **Abrir conversor de formato** (ícone de uns e zeros).
2. Ative os formatos que deseja converter.
3. Clique em **Iniciar conversão**.

Para mais informações, consulte [[Sintaxe de formatação básica]].

## Formatos suportados

| Application   | From                  | To                                                              |
|---------------|-----------------------|-----------------------------------------------------------------|
| Roam Research | `#tag` and `#[[tag]]` | `[[tag]]`                                                       |
| Roam Research | `^^highlight^^`       | `==highlight==`                                                 |
| Roam Research | `{{[[TODO]]}}`        | `[ ]`                                                           |
| Bear          | `::highlight::`       | `==highlight==`                                                 |
| Zettelkasten  | `[[UID]]`             | `[[UID File Name]]` (full link)                                 |
| Zettelkasten  | `[[UID]]`             | <code>\[\[UID File Name&#124;File Name\]\]</code> (pretty link) |

