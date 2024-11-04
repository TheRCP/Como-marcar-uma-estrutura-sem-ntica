## Criar Uma Estrutura Semântica.

### A natureza do HTML

Os criadores do [HTML](#) eram cientistas que pretendiam um meio padronizado para partilhar documentos de física de particulas. Eles estavam muito pouco interessados na exacta forma visual com que os documentos eram apresentados no ecrã de um computador. Na realidade, o [HTML](#) foi originalmente concebido para forçar uma clara separação entre a estrutura dos documentos e o desenho gráfico. A intenção era criar uma *World Wide Web* (uma teia de amplitude mundial) de páginas que poderiam ser vistas em qualquer sistema e navegador disponível, incluíndo os navegadores que "lêem" o texto da página web para os utilizadores com deficiência da visão assim como serem interpretadas assertivamente por sistemas automáticos de pesquisa e motores de análise.

Os inventores da Web nunca imaginaram o potencial gráfico e de apresentação da mesma, e como tal, o [HTML](#) não foi concebido originalmente com as questões de apresentação em mente. Eles estavam tão preocupados em tornar os documentos web amigáveis às máquinas (*machine-friendly*) que produziram documentos que apenas as máquinas (ou os físicos de particulas) conseguiam ler. Colocando o seu enfoque apenas na lógica estrutural dos documentos ignoraram a necessidade da lógica visual da concepção gráfica e da tipografia. Esta falta de ênfase visual na web foi a principal causadora de uma espécie de stresse dos *designers* web que procuram avidamente que o aspecto das páginas fique exactamente igual ao que idealizaram. Toda esta pressão levou os fabricantes de navegadores web a ignorar os padrões próprios do [HTML](#) e a adicionarem funções ou extensões ao [HTML](#) permitindo funcionalidades visuais e de formatação que apenas são interpretáveis nos seus navegadores.

Por exemplo, muitos *designers* gráficos evitam a utilização das *tags* padrão indicadoras de cabeçalho em [HTML](#) (`<h1>`, ... `<h6>`) porque lhes falta, a estes elementos, delicadeza: em muitos navegadores Web estas *tags* fazem os cabeçalhos parecer absurdamente grandes (`<h1>`, `<h2>`) ou ridiculamente pequenos (`<h4>`, `<h5>`, `<h6>`). mas as *tags* de cabeçalho em [HTML](#) não foram criadas tendo em conta a concepção gráfica. O seu único propósito é estabelecer uma hierarquia de importância de cabeçalhos, por forma a que, quer os leitores humanos quer os motores de pesquisa automáticos, possam observar um documento e, de uma forma simples, determinar a estrutura da informação nele existente. Apenas acidentalmente os fabricantes de navegadores criam uma hierarquia visual para os cabeçalhos [HTML](#) através da atribuição de diferentes tipos de tamanho e níveis de impressão para cada elemento cabeçalho, embora estes tipos de tamanho tendam a ser algo limitativos dentro da linguagem [HTML](#).

---

### Utilizar cabeçalhos para estruturar conteúdos

Considerando a natureza da Web, e não esquecendo o movimento de transformação da Web de um papel de meio estrutural para um meio visual, é, no entanto, importante que o conteúdo web seja concebido com uma estrutura adequada. Com um melhor suporte das folhas de estilo em cascata nas recentes versões de navegadores web, os criadores podem alterar o aspecto dos elementos estruturais de forma a ir ao encontro das suas preferências visuais e de concepção.

**Exemplo**

Visualize o conteúdo da estrutura de uma das suas páginas Web acedendo a [http://validator.w3.org/detailed.html](http://validator.w3.org/detailed.html) - link externo. Introduza o URL da página Web na caixa de edição, seleccione a caixa de verificação *Show Outline*, e pressione no botão *Validate this page*. Por agora, ignore quaisquer erros de [HTML](#) que possam ser assinalados e desloque-se para baixo para ver o *outline* da página analisada. Verá uma breve síntese do conteúdo estruturado da sua página web conforme definida pelas *tags* de cabeçalho (`<h1>` - `<h6>`). Se o resultado não lhe parece ser um verdadeiro *outline* (linhas estruturais principais) da página, é porque as *tags* de cabeçalho não estão a ser correctamente utilizadas (ou então é porque não existe quaisquer *tags* de cabeçalho).

O leitor de ecrã e outras tecnologias de apoio utilizadas têm a capacidade de navegar pelas páginas web através da estrutura. Significa isto que o utilizador pode ler ou saltar directamente para elementos de nível máximo (`<h1>`), ou elementos de nível seguinte (`<h2>`), elementos de terceiro nível (`<h3>`), e assim para todos os outros. Ao ver ou ouvir estes elementos destacados dever-se-á ficar com uma boa ideia dos conteúdos e da estrutura da página.

As páginas devem ser estruturadas de uma maneira hierárquica, com o primeiro nível de cabeçalho (`<h1>`) a ser atribuído ao elemento/conteúdo mais importante (usualmente corresponde ao título ou cabeçalho da página), depois seguir-se-á o segundo nível (`<h2>` - geralmente é atribuído aos cabeçalhos das secções mais importantes), e descemos ao terceiro nível de cabeçalhos (geralmente sub-secções de `<h2>`), e assim sucessivamente. Tecnicamente, os níveis mais baixos de cabeçalhos devem estar contidos em cabeçalhos de nível imediatamente superior. O *outline* que se segue mostra uma hierarquia típica que poderá existir numa página web. De facto, ela representa a hierarquia da secção principal desta página, com diferentes graus de cabeçalhos para representar níveis altos e baixos correspondentes à hierarquia do conteúdo. Pode pressionar em qualquer um dos itens cabeçalho para saltar para a correspondente secção desta página.

- [Cabeçalho 1](#n0)
  - [(1) Cabeçalho 2](#n1)
  - [(2) Cabeçalho 2](#n2)
  - [(3) Cabeçalho 2](#n3)
  - [(4) Cabeçalho 2](#n4)

---

### Utilizar correctamente cabeçalhos

**Não faça uso de texto formatado, tais como tamanhos de fonte ou negrito para dar uma aparência de cabeçalhos - utilize as *tags* de cabeçalho (`<h1>` - `<h6>`) para todo o conteúdo cabeçalho.** As tecnologias de apoio e também os navegadores Web servem-se do código de marcação da página para determinar a estrutura. Os elementos com impressões mais fortes ou mostrados com tamanhos de fonte grandes não são interpretados como elementos estruturais.

**Idealmente, não use cabeçalhos apenas para conseguir um efeito diferente.** Assim, se pretende destacar ou dar ênfase a um determinado elemento do seu conteúdo que não seja um cabeçalho (tal como fizemos com a frase anterior), não faça uso de *tags* de cabeçalho para conseguir a aparência visual pretendida. Em vez disso, use as *tags* para tamanho de fonte, negrito ou itálico. Actualmente, deve usar estilos para obter resultados visuais. Se pretende dar ênfase a algo deve, tecnicamente, usar a *tag* `<strong>` em vez de `<bold>` e a *tag* `<em>` em vez de `<i>`. *Bold* e *Italic* (`<i>`), ambas assentam numa lógica de ênfase visual, ao passo que *Strong* e *emphasis* (`<em>`) sugerem uma ênfase semântica. Visualmente, `<b>` e `<strong>`, e `<em>` e `<i>` têm exactamente o mesmo aspecto, devem usar as *tags* [HTML](#) mais apropriadas. No *Dreamweaver*, pode seleccionar "Editar > Preferências > Gerais" e seleccionar "Use `<strong>` e `<em>` em vez de `<b>` e `<i>`".

---

### Utilizar correctamente listas

As listas [HTML](#) - `<ul>`, `<ol>`, e `<dl>` - são compostas também por uma estrutura hierárquica de conteúdos. Cada uma delas tem regras, as quais estão de acordo com a sua função. As listas não ordenadas (`<ul>`) devem ser usadas quando não exista ordem sequêncial ou de importância. As listas ordenadas (`<ol>`) sugerem uma progressão ou sequência. As listas de definição (`<dl>`) devem ser usadas explicitamente para uma apresentação de uma estrutura de definições. Tal como nos cabeçalhos, as listas devem ser usadas correctamente e servir apenas os propósitos semânticos para os quais foram criadas. As listas não ordenadas e ordenadas devem sempre conter itens de lista. As listas de definição devem sempre ter descrições de definição. As listas vazias são consideradas um erro em [HTML](#). As listas nunca deverão ser usadas para propósitos meramente de indentação ou outros tipos de apresentações.

---

Tutorial Original [WebAIM](http://www.webaim.org/techniques/semanticstructure/) com o título: [Creating Semantic Structure](http://www.webaim.org/techniques/semanticstructure/).  
Tradução portuguesa: Jorge Fernandes