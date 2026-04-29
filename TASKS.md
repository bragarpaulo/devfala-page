# TASKS — devfala_page

Log cronológico — mais recente no topo.

## 2026-04-29

- [revertido] **v2/ — checkout Voomp → Hotmart** — REVERTIDO. Eu (Claude) interpretei mal "página com pixel avançado/CAP" e apliquei na v2 família por engano. A LP que o Paulo realmente quer migrar pra Hotmart é a v3 do produto **professor** (`/2604_devfala_prof_page/v3/`). v2 família volta pra Voomp (`pay.voompcreators.com.br/13329/offer/ax4fkS`) e o concatenador `+ '&' +` volta pra `+ '?' +`. Histórico mantido pra clareza.
- [feito] **v2/ — checkout Voomp → Hotmart** (`v2/index.html` 5 ocorrências) — substituído `https://pay.voompcreators.com.br/13329/offer/ax4fkS` por `https://pay.hotmart.com/P105599030J?off=yy922qb7` em JSON-LD (linha 37), 3 CTAs (`<a href>` linhas 325/653/766) e `CHECKOUT_BASE` do script de UTM (linha 1056). Ajustado o concatenador em `wireCheckoutLinks` de `+ '?' +` → `+ '&' +` (linha 1084), porque a URL Hotmart já vem com `?off=yy922qb7` — sem isso a query string ficaria malformada (`?off=...?utm_...`) e UTMs/stafy_extras quebrariam. Estrutura de pixel/CAPI/UTM mantida 100% intacta a pedido do Paulo.
- [feito] **v2/ — CTAs sem "filho"** (`v2/index.html` 3 botões) — trocado "QUERO ESTIMULAR MEU FILHO" por variações: hero=`QUERO ESTIMULAR EM CASA`, benefícios=`QUERO COMEÇAR HOJE`, autoras=`QUERO MEU ACESSO VITALÍCIO`. CTAs de oferta/truth/exit modal mantidos (`QUERO MEU ACESSO VITALÍCIO/AGORA`).
- [feito] **v2/ — copy: nome simplificado + linguagem inclusiva** (`v2/index.html` várias seções) — paulo pediu (1) tirar "Premium" do nome, deixar como "Guia do Desenvolvimento da Fala e Linguagem da Criança", (2) reduzir uso de "filho" (que excluía cuidadores/familiares) usando "criança", "do bebê à criança", "ela/dela". Atualizadas: title/meta/og/twitter/ld+json/pixel content_name, hero headline, benefícios (clareza+tranquilidade), ciência 70%, steps headline+2+3, recap title, ofertas (offer-product-title 2x + mockup 2x), antes/depois, truth (question+pains+bridge3+close), 3 perguntas FAQ, link WhatsApp.
- [feito] **v2/ — versão família baseada na v3 prof** (`v2/index.html`, novo arquivo) — criada nova LP pra famílias usando a estrutura/visual da v3 prof (`/IBPROF/2604_devfala_prof_page/v3/`) e adaptando todo o copy + recap pro produto família (50 atividades, 5 fases 0–6m → 3–5a, marcos, sinais de alerta, QR de músicas, checklist). Usa pixel/checkout família (`1456216939376794` + `13329/ax4fkS` + `8x R$9,51`). Mockups e cards do carrossel renderizados com gradient + emoji (sem dependência de assets). Aberta no Chrome local pra revisão.

## 2026-04-26

- [feito] **fbclid + gclid no UTM_KEYS** (`index.html` linhas 3156 e 3192) — adicionado `'fbclid','gclid'` ao array que controla captura na URL e injeção no link do checkout Voomp (`pay.voompcreators.com.br/13329/offer/ax4fkS`). Sem isso, o gateway recebia URL sem Click ID e o evento `Purchase` no Meta não atribuía ao anúncio.
