# UMADEB 57 — Site do Encontro Setorial

Site de divulgação em uma única página (`index.html`), pronto para publicar,
com espaço para os vídeos de cada cantor e cada preletor.

## Estrutura de pastas

```
umadeb57/
├── index.html                 -> o site (abrir este arquivo no navegador)
├── videos/
│   ├── preletores/
│   │   ├── anselmo-dantas/
│   │   ├── anderson-cavalcante/
│   │   └── isabella-garcia/
│   └── cantores/
│       ├── michelle-delfino/
│       ├── matheus-henrique/
│       └── marcos-rodrigues/
```

## Como adicionar os vídeos

Dentro da pasta de cada pessoa, coloque:

1. **`video.mp4`** — o vídeo que vai tocar no site (obrigatório).
2. **`capa.jpg`** — uma foto de capa (thumbnail) em formato paisagem, tipo 16:9
   (opcional). Enquanto não houver `capa.jpg`, o card mostra as iniciais da
   pessoa sobre um fundo roxo, no estilo do cartaz.

Não é preciso mexer em nenhum código. Assim que os arquivos estiverem com
esses **nomes exatos** dentro da pasta certa, eles aparecem automaticamente
no site (o card mostra "Vídeo em breve" enquanto o arquivo não existir).

Exemplo:
```
videos/preletores/anselmo-dantas/video.mp4
videos/preletores/anselmo-dantas/capa.jpg
```

## Como ver o site

**Opção mais simples:** dê duplo clique em `index.html` — ele abre no navegador
e já funciona, inclusive com os vídeos.

**Opção recomendada (evita qualquer bloqueio do navegador com vídeos locais):**
rode um servidor local na pasta do projeto. Com Python instalado:

```
cd umadeb57
python3 -m http.server 8000
```

Depois abra `http://localhost:8000` no navegador.

## Como publicar o site de verdade (com link para compartilhar)

Qualquer serviço de hospedagem de arquivos estáticos funciona, por exemplo:

- **Netlify** ou **Vercel**: arraste a pasta `umadeb57` inteira no painel do site.
- **GitHub Pages**: suba a pasta em um repositório e ative o Pages.

Atenção: arquivos de vídeo `.mp4` costumam ser grandes. Se o Encontro tiver
muitos vídeos em alta resolução, comprima antes de subir (recomendo manter
cada vídeo abaixo de 50–80 MB para carregar rápido no site).

## Ajustes rápidos

- **Contagem regressiva:** no `index.html`, procure por `eventDate` dentro do
  `<script>` e ajuste a data/hora se precisar.
- **Cores:** todas as cores do site estão definidas no topo do `<style>`,
  dentro de `:root { ... }` — dá pra trocar qualquer tom sem afetar o layout.
- **Endereço / mapa:** procure pela seção `#local` no `index.html` para trocar
  o endereço e o link do mapa.
- **Nomes da liderança / coordenação:** estão no rodapé (`<footer>`), fáceis
  de editar direto no HTML.

Qualquer dúvida, é só perguntar. 🔥
