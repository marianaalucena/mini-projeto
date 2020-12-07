+++
title = "Documentação arquitetural para o GIMP"
date = 2020-12-07
tags = []
categories = []
+++

***

Este documento descreve a arquitetura do projeto GIMP.

***

# Autores

Este documento foi produzido por Mariana Araújo Lucena.

- Matrícula: 115211305
- Contato: mariana.lucena@ccc.ufcg.edu.br
- Projeto documentado: https://github.com/GNOME/gimp

# Descrição Arquitetural -- GNOME/gimp

Este documento foi produzido para a disciplina de Arquitetura de Software da UFCG, e tem como objetivo descrever parte da arquitetura do projeto [GNOME/gimp](https://github.com/GNOME/gimp). Essa descrição foi baseada principalmente no modelo [C4](https://c4model.com/).

É importante destacar que não será descrita toda a arquitetura do GIMP. O foco aqui é a descrição de um serviço específico de análise do GIMP, que é parte fundamental do projeto.

## Descrição Geral sobre o GIMP

GIMP (acrônimo para GNU Image Manipulation Program) é um programa voltado, essencialmente, para edição e criação de imagens raster e, em menor escala, para desenho vetorial. O software é repleto de recursos, de fácil uso e uma boa alternativa gratuita ao mais conhecido dos editores, o gigante Adobe Photoshop.

## O Serviço de edição de fotos através dos filtros no GIMP

### Objetivo Geral

Os filtros permitem fazer efeitos complexos com poucos cliques, efeitos como de iluminação, distorção, entre outros. No menu “Filtros”, você tem acesso a mais de 140 tipos de filtros diferentes. Os filtros são divididos em 15 categorias para que você consiga achá-los mais facilmente. Essas categorias são: desfocar, realces, distorções, efeitos de sombra, efeitos de luz, ruído detectar borda, genéricos, combinar, filtros artísticos, mapear, renderizar, web, animação, alfa para logo, decoração.


### Contexto

É necessário executar o download do instalador do GIMP e abrir o arquivo de instalação. Depois da instalação, pode começar a usá-lo. Para a aplicação de filtros em uma imagem, é necessário fazer o upload da mesma para o programa, no menu superior selecionar a janela "Filtros" e após escolher o filtro. 

Abaixo está o diagrama de contexto.

<img class="center" border="15px" src="https://github.com/marianaalucena/mini-projeto/blob/main/imagens/contexto.jpg?raw=true" />



### Containers

Nesta seção eu espero duas coisas: o diagrama de containers e  texto descrevendo os containers. Detalhe no nível que achar necessário, mas é importante saber do que se trata cada container, suas tecnologias, APIs expostas, protocolos, onde são executados/implantados etc. Você pode criar um diagrama de implantação para dar mais detalhes sobre o ambiente em que os containers são implantados e executam. Essa parte de implantação pode ser uma subseção desta seção.

Importante, se um componente expor, por exemplo, uma API REST. Seria importante descrever os principais serviços. Talvez até com exemplos de payloads (jsons) para os serviços mais importantes. Ver seção endpoints [deste documento](https://docs.google.com/document/d/1OGPN7crENY5u9AiR_AE7Cb9rT92T-U-YppZL0m4TT2s/edit?usp=sharing).

Importante, se um container expuser, por exemplo, uma API REST, seria importante descrever os principais serviços. Talvez até com exemplos de payloads (jsons) para os serviços mais importantes. Ver seção endpoints [deste documento](https://docs.google.com/document/d/1OGPN7crENY5u9AiR_AE7Cb9rT92T-U-YppZL0m4TT2s/edit?usp=sharing).

Abaixo estão exemplos de diagramas de containers e de implantação.

![fig3](c4-containers.png)
![fig4](parlametria-container.png)
![fig5](c4-implantacao.png)
![fig6](parlametria-implantacao.png)

### Componentes

Nesta seção eu espero duas coisas: o diagrama de componentes e texto descrevendo os componentes. Detalhe no nível que achar necessário, mas é importante saber do que se trata cada componente, seus relacionamentos, tecnologias, APIs expostas, protocolos, estilos, padrões etc.

Abaixo um exemplo de diagrama de componente.

![fig7](c4-componentes.png)

### Código

<pre>
Nesta etapa não faremos diagramas que apresentam detalhes da
implementação. Faremos isso mais adiante.
</pre>

### Visão de Informação

Aqui você deve descrever as informações importantes que são coletadas, manipuladas, armazenadas e distribuídas pelo sistema. Você não precisa descrever todas as informações, somente uma parte que seja essencial para o sistema. Por exemplo, se eu estivesse tratando do instagram, faria algo relacionado aos posts.

Além da descrição gostaria de ver aqui um diagrama para descrever os estados (ex: máquina de estados) de uma informação de acordo com as ações do sistema.

# Contribuições Concretas

*Descreva* aqui os PRs enviados para o projeto e o status dos mesmos. Forneça os links dos PRs.
