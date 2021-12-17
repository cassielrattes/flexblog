# CSS FLEXBOX - [ORIGAMID](https://www.origamid.com/)

> # FLEX CONTAINER
>
> O Flex Container é a tag que envolve os itens flex, ao indicar display: flex, essa tag passa a ser um Flex Container

<br/>

- **[display:](https://codepen.io/origamid/pen/XRRVrG)** Define o elemento como um flex container tornando os seus filhos flex-itens.

- **[flex-direction:](https://codepen.io/origamid/pen/qmrdgL)** Define a direção dos flex itens. Por padrão ele é row (linha), por isso quando o display: flex; é adicionado, os elementos ficam em linha, um do lado do outro. A mudança de row para column geralmente acontece quando estamos definindo os estilos em media queries para o mobile. Assim você garante que o conteúdo seja apresentado em coluna única.

- **[flex-wrap:](https://codepen.io/origamid/pen/qmrOOw)** Define se os itens devem quebrar ou não a linha. Por padrão eles não quebram linha, isso faz com que os flex itens sejam compactados além do limite do conteúdo. Essa é geralmente uma propriedade que é quase sempre definida como flex-wrap:wrap; Pois assim quando um do flex itens atinge o limite do conteúdo, o último item passa para a coluna debaixo e assim por diante.

- **[flex-flow:](https://codepen.io/origamid/pen/WjppjL)** É um atalho para as propriedades flex-direction e flex-wrap. Você não verá muito o seu uso, pois geralmente quando mudamos o flex-direction para column, mantemos o padrão do flex-wrap que é nowrap. E quando mudamos o flex-wrap para wrap, mantemos o padrão do flex-direction que é row.

- **[justify-content:](https://codepen.io/origamid/pen/XRMMyK)** Alinha os itens flex no container de acordo com a direção. A propriedade só funciona se os itens atuais não ocuparem todo o container. Isso significa que ao definir flex: 1; ou algo similar nos itens, a propriedade não terá mais função. Excelente propriedade para ser usada em casos que você deseja alinhar um item na ponta esquerda e outro na direita, como em um simples header com marca e navegação.

- **[align-items:](https://codepen.io/origamid/pen/pPePeb)** Alinha os flex itens de acordo com o eixo do container. O alinhamento é diferente para quando os itens estão em colunas ou linhas. Essa propriedade permite o tão sonhado alinhamento central no eixo vertical, algo que antes só era possível com diferentes hacks.

- **[align-content:](https://codepen.io/origamid/pen/ybMbZo)** Alinha as linhas do container em relação ao eixo vertical. A propriedade só funciona se existir mais de uma linha de flex-itens. Para isso o flex-wrap precisa ser wrap. Além disso o efeito dela apenas será visualizado caso o container seja maior que a soma das linhas dos itens. Isso significa que se você não definir height para o container, a propriedade não influencia no layout.

<br/>

> # FLEX-ITEM
>
> Os Flex Itens são os filhos do Flex Container, lembrando que uma tag se torna um flex container a partir do momento que você definir display: flex. É possível que uma Flex Item seja também um Flex Container, basta definir display: flex nele. Assim os filhos desse item também serão flex itens.

<br/>

- **[flex-grow:](https://codepen.io/origamid/pen/ybMEpV)** Define a habilidade de um flex item crescer. Por padrão o valor é zero, assim os flex itens ocupam um tamanho máximo relacionado o conteúdo interno deles ou ao width definido. Ao definir 1 para todos os Flex Itens, eles tentarão ter a mesma largura e vão ocupar 100% do container. Digo tentarão pois caso um elemento possua um conteúdo muito largo, ele irá respeitar o mesmo. Se você tiver uma linha com quatro itens, onde três são flex-grow: 1 e um flex-grow: 2 tentará ocupar 2 vezes mais espeço extra do que os outros elementos. OBS: justify-content não funciona em items com flex-grow definido.

- **[flex-basis:](https://codepen.io/origamid/pen/vmxVzP)** Indica o tamanho inicial do flex item antes da distribuição do espaço restante. Quando definimos o flex-grow: 1; e possuímos auto no basis, o valor restante para ocupar o container é distribuído ao redor do conteúdo do flex-item.

- **[flex-shrink:](https://codepen.io/origamid/pen/KmmaWv)** Define a capacidade de redução de tamanho do item.

- **[flex:](https://codepen.io/origamid/pen/OmmWKg)** Atalho para as propriedades flex-grow, flex-shrink e flex-basis. Geralmente você verá a propriedade flex nos flex itens ao invés de cada um dos valores separados. Para melhor consistência entre os browsers, é recomendado utilizar a propriedade flex ao invés de cada propriedade separada. No exmplo é possível ver as mesmas configurações do exemplo do flex-basis porém agora utilizando apenas a propriedade flex.

- **[order:](https://codepen.io/origamid/pen/VbbPEY)** Modifica a ordem dos flex itens. Sempre do menor para o maior, assim order: 1, aparece na frente de order: 5.

- **[align-self:](https://codepen.io/origamid/pen/Vbbpvj)** O align-self serve para definirmos o alinhamento específico de um único flex item dentro do nosso container. Caso um valor seja atribuído, ele passara por cima do que for atribuído no align-items do container. Vale lembrar que o alinhamento acontece tanto em linha quanto em colunas. Por exemplo o flex-start quando os itens estão em linhas, alinha o item ao topo da sua linha. Quando em colunas, alinha o item ao início (esquerda) da coluna.
