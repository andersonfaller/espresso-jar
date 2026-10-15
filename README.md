# espresso-jar
Which espresso pods are available in my kitchen's jar right now.

Publicado em [faller.one/espresso-jar](https://faller.one/espresso-jar).

## Como funciona

- `capsulas.json` é gerado pela planilha do Google (via script) e commitado aqui.
- `index.html` lê esse arquivo e monta o cardápio: só as cápsulas com `isAvailable: true` aparecem no pote; as demais ficam na seção "Em falta no momento".
- A data de "Atualizado há…" vem do cabeçalho `Last-Modified` do GitHub Pages — não precisa de campo extra no JSON.

## Campos do JSON

| Campo | Uso |
| --- | --- |
| `name`, `brand` | Nome e marca do café |
| `brandImageUrl` | Foto da embalagem (frente do card) |
| `capsuleImageUrl` | Foto da cápsula (verso do card — toque para virar) |
| `descriptionUrl` | Link "Ver detalhes" |
| `isAvailable` | `true` se tem no pote |
| `color` *(opcional)* | Cor da cápsula no pote e no card, ex.: `"#8a2a35"`. Sem ela, a cor é escolhida automaticamente. |

Campos de imagem vazios mostram uma ilustração da cápsula no lugar da foto.

`og.jpg` (prévia de links) e `apple-touch-icon.png` (ícone na tela inicial) são estáticos.
