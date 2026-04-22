# Instruções persistentes do projeto

## Início de conversa nova

Sempre que uma conversa começar **sem contexto ou instrução específica do Paulo** (ex: saudação "oi"/"bom dia", "voltei", "o que temos", ou silêncio após carregar o projeto — sem task definida), **apresente proativamente o que tá pendente antes de perguntar o que fazer.**

**Como levantar pendências:**
1. Leia `TASKS.md` na raiz do projeto — entradas com status `[pedido]` ou `[em-progresso]` são pendentes.
2. Se existir `docs/ROADMAP-NEXT.md` (ou similar), identifique a próxima onda/atividade ainda não iniciada.
3. Verifique também outros projetos adjacentes em `/Users/pauloricardobraga/Documents/Cursor/*` — Paulo trabalha em vários (LeadHub + landings BIANCA/FACIALBR/FSC/IBPROF). Mencione pendências deles também.

**Formato do resumo:**

```
Bom dia/boa tarde! Retomando:

Pendências curtas (fora de onda):
- [Projeto X] item Y
- [Projeto Z] item W

Próxima atividade do roadmap:
- [Projeto X] Onda N — <nome> (~esforço)

Qual quer atacar primeiro?
```

Se não houver pendência alguma, ainda assim mencione explicitamente ("sem pendências curtas; próxima onda seria X, esperando aval") — nunca assuma que é pra começar algo sozinho.

**Quando NÃO aplicar:**
- Paulo já direciona: "fix o bug no X", "continua a Onda 5", "deploy isso aqui" → executar direto.
- Conversa continua visivelmente de onde parou (mesma sessão, contexto carregado).

## Fluxo de execução de tarefas

- **Correção pontual / ajuste interno** (bug, UI tweak, rename, copy change, config) → executar direto sem perguntar. Segue o fluxo padrão do projeto (typecheck + testes + commit + push + deploy quando aplicável).
- **Sem task específica do Paulo** → perguntar qual atividade do roadmap/TASKS.md ele quer iniciar. Nunca começar onda grande sem aval.

## Log de atividades

Registrar toda tarefa pedida em `TASKS.md` na raiz do projeto (inclusive canceladas/recusadas), formato cronológico — mais recente no topo.
