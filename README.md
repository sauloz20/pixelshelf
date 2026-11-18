# PixelShelf

Protótipo de marketplace de produtos digitais com catálogo, categorias, busca e detalhes de produtos. Os produtos, criadores, preços e métricas exibidos são dados demonstrativos.

## Tecnologias e requisitos

React, JavaScript, CSS e Vite. Para desenvolver localmente são necessários Git, Node.js e npm.

## Executar

```sh
git clone https://github.com/sauloz20/pixelshelf.git
cd pixelshelf
npm ci
npm run dev
```

Abra o endereço exibido no terminal. O servidor de desenvolvimento está configurado para a porta 3000.

Para gerar a versão de produção:

```sh
npm run build
```

## Estrutura

```text
index.html             Entrada do Vite
src/main.jsx           Componentes, dados demonstrativos e interações
src/styles.css         Estilos da aplicação
public/                Arquivos públicos
docs/                  Briefings de produto e UX
TODO.md e plan.md      Planejamento do projeto
```

## Limitações

O catálogo usa dados definidos no código. Não há backend de marketplace ou processamento real de pagamentos neste repositório. Existem arquivos de bloqueio tanto para npm quanto para pnpm; o procedimento acima usa o `package-lock.json` com npm. O projeto declara versões `latest` em `package.json`; revise a estratégia de versões antes de atualizar dependências.
