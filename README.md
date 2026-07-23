# UMADEB 57 — Site do Encontro Setorial

Site de divulgação em uma única página (`index.html`), pronto para publicar,
com espaço para os vídeos de cada cantor e cada preletor.

## Estrutura de pastas

```
umadeb57/
├── index.html                 -> o site (abrir este arquivo no navegador)
├── img/                        -> logos oficiais (AD Belém + UMADEB)
├── videos/
│   ├── preletores/
│   │   ├── anselmo-dantas/
│   │   ├── anderson-cavalcante/
│   │   └── isabella-garcia/
│   └── cantores/
│       ├── michelle-delfino/
│       ├── matheus-henrique/
│       └── marcos-rodrigues/
└── patrocinadores/             -> logos das empresas/comércios apoiadores
```

## Paleta de cores oficial (Manual de Identidade Visual UMADEB SP 2K26)

| Cor | Hex |
|---|---|
| Preto | `#181818` |
| Vinho | `#7E2A16` |
| Vermelho | `#F30103` |
| Bege | `#CEB49A` |
| Creme / off-white | `#ECE2E0` |

Todas as cores do site ficam no topo do `<style>`, dentro de `:root { ... }`
no `index.html` — dá pra ajustar qualquer tom por ali.

## Patrocinadores (carrossel automático no final da página)

Coloque as imagens dentro de `patrocinadores/`, numeradas em sequência:

```
patrocinadores/01.png
patrocinadores/02.jpg
patrocinadores/03.png
```

Aceita `.png`, `.jpg`, `.jpeg` ou `.webp`, em **qualquer tamanho ou
proporção** — o site encaixa a imagem inteira dentro de um card padrão,
sem cortar nem distorcer. O carrossel desliza sozinho e para se o mouse
passar por cima.

**Importante:** os números precisam ser seguidos (01, 02, 03...), sem
pular nenhum — o site carrega em ordem e para no primeiro número que não
encontrar. Para adicionar um novo patrocinador, salve a próxima imagem
com o próximo número da sequência. Se a pasta estiver vazia, essa seção
mostra "Patrocinadores em breve" automaticamente.

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