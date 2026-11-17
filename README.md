# AURUM Residences — demonstração imobiliária premium

Site estático em HTML, CSS e JavaScript, com identidade visual escura, catálogo demonstrativo e experiência arquitetônica 3D.

## Publicação no Cloudflare Pages

Este repositório está preparado para **Cloudflare Pages via integração com Git**.

1. No Cloudflare, abra **Workers & Pages → Create application → Pages → Connect to Git**.
2. Conecte o GitHub e selecione `phztrem12/projeto-imobili-ria`.
3. Configure:
   - **Production branch:** `main`
   - **Framework preset:** `None`
   - **Build command:** `exit 0`
   - **Build output directory:** `.`
4. Salve e inicie a implantação.

O arquivo de entrada é `index.html`; não há etapa de build.

## Antes de usar com uma imobiliária real

Edite as configurações no início do JavaScript em `index.html`:

- `CFG.wa`: número real do WhatsApp no formato internacional, somente números.
- `CFG.formEndpoint`: endpoint HTTPS que recebe os formulários, se houver CRM/backend.

Os imóveis, preços, equipe, endereço, indicadores e depoimentos são **dados fictícios de demonstração** e devem ser substituídos. O formulário abre o WhatsApp como alternativa enquanto não houver endpoint configurado.

## Observações técnicas

- Three.js cria a residência procedural e as partículas da transição.
- GSAP/ScrollTrigger controla a narrativa vinculada à rolagem.
- As fotografias do catálogo são carregadas do Unsplash.
- O projeto possui fallback visual para falha de WebGL e menu responsivo.
- Por ser um site estático, formulários não são armazenados em banco de dados sem integração adicional.
