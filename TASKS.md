# TASKS — devfala_page

Log cronológico — mais recente no topo.

## 2026-04-26

- [feito] **fbclid + gclid no UTM_KEYS** (`index.html` linhas 3156 e 3192) — adicionado `'fbclid','gclid'` ao array que controla captura na URL e injeção no link do checkout Voomp (`pay.voompcreators.com.br/13329/offer/ax4fkS`). Sem isso, o gateway recebia URL sem Click ID e o evento `Purchase` no Meta não atribuía ao anúncio.
