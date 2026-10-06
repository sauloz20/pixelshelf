# PixelShelf — plano de implementação

## Direção aprovada
Marketplace de ativos digitais para templates, recursos de design e ferramentas comerciais. A primeira versão é frontend-only, com interações locais para descoberta, filtragem, busca, carrossel e download simulado.

## Design
- **Movimento:** dashboard editorial minimalista com energia neo-brutalista suave: estrutura utilitária, bordas finas, números compactos e blocos de cor vibrante.
- **Princípios:** clareza de inventário; densidade confortável; contraste entre branco e roxo; interações rápidas e visíveis.
- **Paleta:** branco e cinzas frios mantêm a leitura do catálogo; roxo elétrico é a assinatura de marca; ciano sinaliza descoberta e ação.
- **Layout:** shell com sidebar fina no desktop e navegação inferior no mobile; conteúdo em coluna ampla com hero dividido e catálogo modular.
- **Assinaturas:** marca em monograma PS dentro de quadrado arredondado; gradiente roxo-ciano em destaque; micro-métricas e chips de categoria em todos os cards.
- **Interação:** filtros e busca respondem imediatamente; cards elevam 2px e trocam a borda para roxo; download abre um estado de sucesso local sem checkout real.
- **Animação:** entradas suaves de 180–260ms; gradiente do hero com deslocamento lento; carrossel manual com dots e botões, sem autoplay agressivo.
- **Tipografia:** Inter/system sans para UI e números; títulos grandes em peso 800, labels em 11–12px uppercase com tracking.
- **Essência:** o shelf curado para quem transforma ideias em ativos prontos para usar. Adjetivos: inventivo, direto, confiável.
- **Voz:** prática, otimista e específica. Exemplos: “Encontre o arquivo que destrava seu próximo projeto.” / “Baixe agora. Construa hoje.”
- **Wordmark:** “Pixel” em peso 800 e “Shelf” em peso 500 com um pequeno cursor pixelado como ponto do i; monograma PS como ícone.
- **Cor proprietária:** `#6D4AFF` (Pixel Purple).

## Estrutura
- `index.html`: entrada Vite e metadados.
- `src/main.jsx`: shell, dados demonstrativos, filtros, busca, carrossel e modal/detalhe.
- `src/styles.css`: tokens, layout responsivo, componentes e estados.
- `public/manus-routes.json`: manifesto da rota principal e detalhe dinâmico.
- `app.config.ts`: metadados do projeto.

## Implementação
A aplicação usa React + Vite sem dependência de backend. O catálogo é alimentado por dados locais e renderiza uma experiência de home; o detalhe abre em painel modal com preview, preço e CTA de download. A navegação lateral alterna entre Home, Explorar, Coleções e Criadores; busca e chips refinam os resultados.

## Expansão executada

A partir dos briefings estratégico e de UX, o protótipo agora inclui jornadas funcionais de descoberta, favoritos, carrinho, compra simulada, biblioteca pessoal e Creator Studio. A navegação ganhou Overview, Explore assets, Categories, Creators, Offers e My library; o topo ganhou atalhos de favoritos e carrinho; cards permitem salvar assets; o detalhe de produto passou a exibir sinais de confiança, licença, compatibilidade, formato, atualização e CTA de compra.

Também foram incluídos skeletons durante a busca, mensagens de pesquisa sem resultado com ações de recuperação, estados vazios para favoritos e biblioteca, feedbacks por toast, reduced motion, áreas clicáveis maiores e um fluxo de Creator Studio com etapas de perfil, publicação, analytics e atualizações. Os briefings originais ficam em `docs/brief-estrategico.txt` e `docs/brief-ux.txt` para rastreabilidade.
