# Scorecard "Como Avaliar a Sua IA de Triagem" — Teste em 3 Mensagens

> **Origem:** vídeo #3 — "Testei as IAs respondendo o mesmo lead no WhatsApp: qual agendaria a visita?"
> **Método:** 3 mensagens reais de lead → mesmo prompt de triagem → 3 IAs (ChatGPT, Gemini, Grok) → comparação critério a critério

## Por que 3 mensagens bastam

Você não avalia uma IA conversando com ela. Você avalia **com as mensagens que já chegam no seu WhatsApp** — as difíceis, não as fáceis. Este scorecard usa 3 padrões que toda imobiliária recebe:

1. **Portal** — "Oi! Vi o anúncio do apartamento na Rua das Acácias, ainda tá disponível?"
2. **Pet** — "Quanto é o aluguel do 2 quartos? Aceita pet? Tenho um cachorro pequeno"
3. **Frustrado** — "Já falei com 3 corretores e ninguém me responde. O último preço do apto da Vila é quanto? Tô cansado"

## O prompt

Use o [prompt de triagem do vídeo #2](prompt-triagem-leads-whatsapp.md) — o mesmo deste teste. Cole as 3 mensagens e compare as saídas com o scorecard abaixo.

## Scorecard — 5 critérios, 1 ponto cada

| # | Critério | Como testar | Aprova se... |
|---|----------|-------------|--------------|
| 1 | **Intenção correta** | Mensagem do portal ("ainda tá disponível?") | Classificar como **compra**, não "dúvida" |
| 2 | **Alerta humano** | Mensagem do frustrado (raiva + risco de perder o lead) | `alerta_humano: true` (booleano!) **+ motivo** |
| 3 | **Formato robusto** | Qualquer saída | JSON válido, `alerta_humano` como **booleano**, não string |
| 4 | **Acabamento** | Rascunho pronto p/ enviar | Acentos completos, sem preguiça de português |
| 5 | **Uma pergunta por mensagem** | Rascunho do pet | Máx. 1 pergunta — lead responde melhor a uma coisa só |

## Resultado real deste teste (executado em 03/09/2026)

| Critério | ChatGPT | Gemini | Grok |
|----------|---------|--------|------|
| Intenção | ✗ dúvida | ✓ compra | ✓ compra |
| Alerta humano | ✗ nem acendeu | ~ quebrou formato (string) | ✓ único correto |
| Formato | ✓ | ✗ string em vez de boolean | ✓ |
| Acabamento | ✗ acentos faltando | ✓ | ✓ |
| 1 pergunta/msg | ✓ | ✓ | ✓ |

**Placar: Grok 5 · Gemini 3 · ChatGPT 2** — mas o placar é o menos importante. **Nenhuma sozinha. Todas com você.** A pergunta certa é: *qual IA performa melhor na SUA tarefa, com o SEU prompt?*

## Como usar em 10 minutos

1. Copie o prompt de triagem (link acima)
2. Cole as 3 mensagens de teste (ou troque pelas suas 3 últimas reais)
3. Rode em 2–3 IAs
4. Marque o scorecard critério a critério
5. A que somar mais pontos **na sua tarefa real** é a sua IA de triagem

## Nota de honestidade

Teste pontual, 3 mensagens, 1 prompt, execução única — não é benchmark científico, é **método de decisão prática**. Repita com suas mensagens antes de escolher.
