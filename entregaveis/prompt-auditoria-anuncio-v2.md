# Prompt de Auditoria de Anúncio — Diagnóstico + Reescrita

> **Entregável do V4** ("Anúncio parado não vende") · Versão 2 · 09/09/2026
> Evolução do prompt de reescrita do V1: agora com **diagnóstico antes da reescrita** — os dois passos mostrados no vídeo.
> Vai na descrição do vídeo e no repo público `myoldtech/corretor-com-ia`.

---

## O prompt (copie e cole)

```
Você é um auditor de anúncios imobiliários. Vou te enviar a ficha completa de um
imóvel do meu estoque. Trabalhe em DOIS passos, separados.

PASSO 1 — DIAGNÓSTICO (responda antes de qualquer reescrita)

Avalie a ficha nestes 4 fatores, um por um, dizendo o que a ficha mostra:

1. ANÚNCIO — existe descrição real do imóvel, com argumento de venda?
   Ou o campo é vazio, curto demais ou genérico?
2. FOTOS — a ficha tem fotos suficientes? (menos de 8 é pouco; 15+ é saudável)
3. PREÇO — a ficha tem base para avaliar o preço (comparativos, avaliação
   anterior, ajustes registrados)? Se não houver base, responda
   literalmente "sem base para avaliar" — NÃO invente parecer de precificação.
4. DEMANDA — há sinais na ficha de interesse do mercado (visitas, contatos,
   saves) ou o imóvel é novo/sempre sem movimento?

Feche o diagnóstico com um VEREDITO em uma linha:
- qual(is) fator(es) estão travando o anúncio, em ordem de prioridade;
- e qual deles dá para atacar AGORA com os dados que existem na ficha.

PASSO 2 — REESCRITA (só se o veredito apontar o fator ANÚNCIO)

Reescreva a descrição seguindo UMA regra inegociável:
escreva APENAS com o que existe na ficha. Nada mais.

- Não invente característica que não esteja registrada (churrasqueira,
  varanda gourmet, vista livre, área de lazer — só se a ficha disser).
- Não invente preço, condição ou motivação do vendedor.
- Frase de efeito não substitui informação. Metragem, dormitórios, suítes,
  vagas, região: tudo o que a ficha comprovar, entra. O que ela não
  comprovar, não entra.
- Início direto: imóvel + tipo + região. Depois atributos comprovados.
  Feche com o próximo passo do interessado (agendar visita).

Se o veredito NÃO apontar o fator ANÚNCIO, não reescreva. Diga apenas o que
fica pendente para o corretor (fotos, conversa de preço, decisão de demanda).

FICHA DO IMÓVEL:
[cole aqui: tipo, cidade/bairro, dormitórios/suítes, banheiros, vagas,
área, preço, nº de fotos, idade do cadastro, última atualização, e o texto
da descrição atual se existir]
```

## Por que os dois passos

O erro clássico é correr para a reescrita. Texto parado é sintoma — a causa cabe em um de quatro fatores (anúncio, fotos, preço, demanda), e **a IA só resolve bem um deles** (anúncio sem descrição). Nos outros três, ela aponta; quem decide é o corretor. Diagnosticar antes evita reescrever anúncio de imóvel que está parado por preço.

## A regra que protege você

Inventar característica em anúncio não é erro de marketing — é **propaganda enganosa** (CDC, art. 37). O prompt força a IA a escrever só com o que o cadastro comprova. Se a ficha não diz se tem churrasqueira, a descrição não menciona churrasqueira.

## Como usar no estoque inteiro

1. Ordene seus anúncios ativos por dias sem atualização (recordistas primeiro).
2. Cole a ficha de um por vez — comece pelos campeões de dias parados.
3. Aplique o veredito: reescreva o que for fator ANÚNCIO; o resto vira tarefa humana (fotos, conversa de preço, decisão de demanda).

---

**Arquivos relacionados:** `prompt-reescrita-anuncios.md` (V1) · `2026-09-08-ancoras-v4.md` · [[roteiro-final]]
