# Black Friday Banlek 2026 — pacote de handoff para TI

Este pacote contém a camada visual/front-end da landing page, organizada para a equipe adaptar e integrar ao sistema da empresa. Ele foi montado a partir da branch mais recente do projeto e inclui somente as páginas e mídias usadas por elas.

## Arquivos

- `index.html` — página principal. HTML, CSS e JavaScript estão no mesmo arquivo.
- `termos/index.html` — termos de uso ligados no rodapé.
- `assets/` — imagens, logos, vídeo e fotos do ensaio referenciados pela página. Mantenha a estrutura e os caminhos relativos ao mover para o sistema da empresa.

## Rodar como página estática

Não há etapa de build nem dependências npm. Para visualizar localmente, sirva esta pasta com qualquer servidor HTTP estático. Exemplo:

```sh
python3 -m http.server 8765
```

Abra `http://localhost:8765/`.

## Interações já feitas no front

- Navegação por âncoras, menu do kit e FAQ.
- Calculadora ilustrativa de payback.
- Carrossel de imagens do Epics Select.
- Barra de compra móvel, animações e adaptação responsiva.
- Contagem regressiva para o encerramento da campanha, em 30/11/2026 às 23h59 (horário de Brasília).
- Página de termos separada em `/termos/`.

## Pontos de integração para a equipe

- No script ao final de `index.html`, `CHECKOUT_URL` está vazio. Conecte os CTAs ao checkout real.
- O link “Baixar artes de divulgação” está marcado com `data-todo="artes"` e ainda usa `href="#"`; conectar ao destino correto ou remover.
- A calculadora e as interações são front-end. Não há APIs, pagamentos, formulários de cadastro, analytics ou persistência de dados neste pacote.
- Revisar a data da campanha, preços, condições, sorteios, textos legais e destinos de navegação antes de colocar no ar no ambiente da empresa.
- Inter é carregada pelo Google Fonts; há fontes de sistema como fallback.
- Para adaptar em um CMS, preserve os IDs/âncoras usados na navegação e os caminhos das imagens, ou atualize os caminhos junto com o HTML.

Este pacote serve como entrega de design/front para integração. A equipe de TI deve conectar os serviços e fluxos reais antes da publicação no sistema da empresa.
