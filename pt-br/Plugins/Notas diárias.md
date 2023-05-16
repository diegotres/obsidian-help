Notas diárias abre uma nota com base na data de hoje ou a cria se não existir. Use notas diárias para criar diários, listas de tarefas ou registros diários para coisas que você descobriu durante o dia.

Para abrir a nota diária de hoje:

- Clique em **Abrir nota diária de hoje** (calendário com ícone de marca de seleção) na [[Fita|ribbon]].
- Executar **Abrir nota diária de hoje** da [[Paleta de comandos]].
- [[Teclas de atalho personalizadas#Configurando teclas de atalho|Usar uma tecla de atalho]] para o comando **Abrir nota diária de hoje**.

Por padrão, o Obsidian cria uma nova nota vazia com o nome da data de hoje no formato AAAA-MM-DD.

> [!dica]
> Se preferir ter suas anotações diárias em uma pasta separada, você pode definir o **Novo local do arquivo** nas opções do plug-in para alterar onde o Obsidian cria novas anotações diárias.

## Crie uma nota diária a partir do modelo

Se suas anotações diárias tiverem a mesma estrutura, você pode usar um [[Modelos|template]] para adicionar conteúdo predefinido às suas anotações diárias ao criá-las.

1. Crie uma nova nota chamada "Modelo diário" com o seguinte texto (ou o que fizer sentido para você!):
   ```md
   # {{date:YYYY-MM-DD}}

   ## Tarefas

   - [ ]
   ```

2. Abra **Configurações**.
3. Na barra lateral, clique em **Notas diárias** em **Opções de plug-in**.
4. Na caixa de texto ao lado de **Localização do arquivo de modelo**, selecione a nota "Modelo diário".

Obsidian usa o modelo na próxima vez que você criar uma nova nota diária.
