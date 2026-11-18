# Happy

Interface web de um projeto que convida pessoas a visitar instituições de acolhimento infantil. A página inicial apresenta a proposta e leva a uma tela de mapa, com uma barra lateral para orientar a busca.

Este repositório contém um estudo de frontend do Happy, projeto da Rocketseat.

## Telas implementadas

| Rota | Conteúdo |
| --- | --- |
| `/` | Página inicial com a identidade do Happy, ilustração e acesso ao mapa |
| `/app` | Mapa com Leaflet, barra lateral e botão com ícone de adição |

Os textos das duas telas identificam a cidade como Três Lagoas, em Mato Grosso do Sul. O centro do mapa é definido separadamente por coordenadas fixas em [OrphanagesMap.tsx](src/pages/OrphanagesMap.tsx).

## O que esta versão contém

A navegação entre a página inicial e o mapa está implementada com React Router. O mapa usa React Leaflet e carrega os tiles do estilo `light-v10` do Mapbox.

O código ainda não inclui marcadores de instituições, consulta a uma API, página de detalhes ou formulário de cadastro. O botão de adição aparece na interface, mas não possui uma rota de cadastro implementada.

## Tecnologias

- React 16 e TypeScript 4.
- React Router 5 para as rotas.
- Leaflet 1.7 e React Leaflet 2 para o mapa.
- Sass para os estilos.
- React Icons para os ícones.
- Parcel 1 para desenvolvimento e build.

## Organização

```text
src/
  pages/
    Landing.tsx          Página inicial
    OrphanagesMap.tsx    Tela do mapa
  assets/
    images/              Logo, ilustração e marcador
    scss/                Estilos globais e das páginas
  routes.tsx             Rotas da aplicação
  App.tsx                Componente principal
  index.tsx              Montagem da aplicação no HTML
index.html               Entrada do Parcel
dist/                    Arquivos de build já versionados
```

## Configuração do mapa

A camada do Mapbox lê a variável `REACT_APP_MAPBOX_TOKEN`. Configure um token próprio no arquivo `.env` para carregar os tiles.

O componente também contém uma alternativa com tiles do OpenStreetMap, atualmente comentada.

## Comandos

Na raiz do repositório, instale as dependências com `npm install`. Os scripts disponíveis são:

| Comando | Uso |
| --- | --- |
| `npm start` | Iniciar o Parcel a partir de `index.html`, sem cache |
| `npm run build` | Gerar o build com caminhos relativos para os assets |

A aplicação mantém as bibliotecas registradas na época do desenvolvimento. Esta documentação foi escrita a partir do código, sem instalar dependências ou executar o projeto.

## Créditos

Conceito e identidade visual do Happy: Rocketseat. Os assets usados nas telas estão em [src/assets/images](src/assets/images).
