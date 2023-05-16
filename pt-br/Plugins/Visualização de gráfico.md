A exibição Gráfico permite visualizar as relações entre as notas em seu cofre.

Para abrir a visualização de gráfico, clique em **Abrir visualização de gráfico** em [[Fita]].

- Os círculos representam notas, ou _nós_.
- Linhas representam [[Links internos]] entre dois nós.

Quanto mais nós referenciam um determinado nó, maior ele fica.

Para interagir com notas no gráfico:

- Passe o mouse sobre cada círculo para destacar as conexões dessa nota.
- Clique em uma nota no gráfico para abri-la.
- Clique com o botão direito do mouse em uma nota para abrir um menu de contexto com as ações disponíveis para essa nota.

Para navegar pelo gráfico:

- Aumente e diminua o zoom usando a roda de rolagem do mouse ou usando as teclas `+` e `-`.
- Mova o gráfico arrastando-o com o cursor do mouse ou usando as teclas de seta.

Você pode segurar Shift enquanto usa o teclado para acelerar os movimentos.

## Configurações

Para abrir as configurações do gráfico, clique no ícone de engrenagem no canto superior esquerdo da visualização do gráfico.

Clique em **Restaurar configurações padrão** no canto superior direito da caixa de configurações para redefinir as alterações feitas.

### Filtros

Esta seção controla quais nós mostrar no gráfico.

- **Pesquisar arquivos** permite filtrar notas com base em uma consulta de pesquisa. Para saber como você pode escrever consultas de pesquisa mais avançadas, consulte [[Busca]].
- **Tags** alterna se as tags devem ser exibidas no gráfico.
- **Anexos** alterna se os anexos devem ser exibidos no gráfico.
- **Apenas arquivos existentes** alterna entre mostrar notas que existem em seu cofre. Como uma nota não precisa existir para vincular a ela, isso pode ajudar a reduzir o limite de seu gráfico para notas que você realmente tem em seu cofre.
- **Órfãos** alterna entre mostrar notas sem links.

### Grupos

Crie grupos de notas para distingui-las umas das outras usando cores.

Para criar um novo grupo:

1. Clique em **Novo grupo**.
2. Na caixa de pesquisa, digite uma consulta de pesquisa para as notas que deseja adicionar ao grupo.
3. Clique no círculo colorido para dar uma cor ao grupo.

Para saber como você pode escrever consultas de pesquisa mais avançadas, consulte [[Busca]].

### Mostrar

Esta seção controla como visualizar nós e links no gráfico.

- **Setas** alterna entre mostrar a direção de cada link.
- **Text fade threshold** controla a transparência do texto para o nome de cada nota.
- **Tamanho do nó** controla o tamanho do círculo que representa cada nota.
- **Espessura do link** controla a largura da linha para cada link.
- **Animate** inicia uma [[#Iniciar uma animação de lapso de tempo|animação de lapso de tempo]].

### Forças

Esta seção controla as forças que agem em cada nó do gráfico.

- **Força central** controla a compactação do gráfico. Um valor mais alto cria um gráfico mais circular.
- **Força de repulsão** controla o quanto um nó empurra outros nós para longe dele.
- **Link force** controla a tração em cada link. Se o elo for um elástico, a força do elo controlará o quanto o elo está apertado ou solto.
- **Link distance** controla o comprimento das linhas entre cada nota.

## Iniciar uma animação de lapso de tempo

Notas e anexos aparecem em ordem cronológica com base no horário de criação.

![[Pasted image 10.png]]

## Gráfico local

Para abrir uma visualização de gráfico local, use o comando **Abrir gráfico local**. Enquanto a exibição de gráfico mostra todas as notas em seu cofre, uma exibição de gráfico local mostra as notas conectadas à nota ativa.

A exibição de gráfico local pode usar todas as [[#Configurações]] disponíveis para a exibição de gráfico global. Além disso, você pode alterar a profundidade do gráfico local. Cada nível de profundidade mostrará notas conectadas às notas reveladas na profundidade anterior. Para controlar a profundidade do gráfico local, use o controle deslizante na parte superior do painel Configurações do gráfico local.