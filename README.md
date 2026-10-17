# certiapp-content

Pacotes de conteúdo (certificações, guias de estudo e questões) do app **CertiApp**.

Este repositório é **público** e **gerado pelo editor do CertiApp**. Não edite os arquivos à mão: o
editor calcula o hash de cada pacote e o app recusa qualquer arquivo cujo hash não confira com o `index.json`.

## Estrutura

| Caminho | O que é |
|---|---|
| `index.json` | Índice lido pelo app: catálogo de empresas e certificações e, para cada pacote, versão, tamanho e SHA-256 |
| `packs/<id>.json` | Um pacote por certificação |

## Como o app usa

1. Baixa `index.json` por HTTPS.
2. Para cada pacote com versão mais nova que a que já tem, baixa `packs/<id>.json`.
3. Confere tamanho e SHA-256, valida o schema e só então instala. Qualquer falha descarta o download e o app continua com o conteúdo anterior.

As questões são originais, escritas a partir do outline oficial de cada exame.
