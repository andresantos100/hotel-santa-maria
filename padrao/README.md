# Padrão Hotéis MA: arquivos

Guia completo (regras, benchmark, checklist): https://claude.ai/artifact/9Ym2Dyk84AH2QQRmU3KvYR

| Arquivo | O que é |
|---|---|
| `padrao-hoteis-ma.css` | Cores, fontes, espaços e todos os componentes `hm-`. Para um hotel novo, troque só `--marca`, `--marca-escura` e `--marca-clara` (há 5 combinações prontas no topo do arquivo). |
| `modelo.html` | Página completa com os campos `{{...}}` para preencher. Os blocos opcionais estão comentados. |

## Site novo em 6 passos

1. Crie a pasta do hotel e copie para ela `modelo.html` (renomeado para `index.html`) e `padrao-hoteis-ma.css`.
2. Busque por `{{` e preencha cada campo com os dados do formulário de coleta.
3. Troque as três cores de marca no topo do CSS.
4. Coloque as fotos reais em `fotos/` (WebP, até 180 KB cada) e troque cada `<div class="hm-foto">Texto</div>` por `<div class="hm-foto"><img src="fotos/x.webp" alt="..." loading="lazy"></div>`.
5. Preencha `HOTEL.whatsapp` no script do fim. Com ele preenchido, os botões viram WhatsApp e a consulta por datas aparece; vazio, os botões ligam para o telefone.
6. Siga o checklist "Antes de publicar" do guia e publique (GitHub + Vercel).

## Ordem fixa da página

Cabeçalho → Topo → Fatos rápidos (+ consulta) → Quartos → Comodidades → Fotos → [Avaliações] → [Perguntas] → [Atrações] → Localização e contato → Rodapé, mais a barra fixa no celular.

**WhatsApp sempre que possível** (regra revista em 25/11/2026): botão no cabeçalho, no topo, na consulta por datas, em cada cartão de quarto ("Consultar este quarto", com o nome do quarto na mensagem), no bloco de contato, no rodapé e na barra do celular. Cada botão usa `data-wa="mensagem"` e o script monta o link `wa.me` com a mensagem pronta. O que continua proibido são as faixas extras de chamada ("Está planejando sua viagem?"), que só repetem o botão sem dar informação nova.

## Exemplo pronto

`../hotel-santa-maria-versao2_claude.html`: o Hotel Santa Maria (Bacabal) no padrão.
