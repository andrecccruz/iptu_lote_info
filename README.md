# iptu_lote

Consulta em lote de débitos de IPTU direto nos portais das prefeituras.

Você envia uma planilha com as inscrições imobiliárias e recebe de volta uma planilha
padronizada com a situação de cada imóvel e o detalhamento dos débitos — sem consultar
inscrição por inscrição no site da prefeitura.

## Municípios atendidos

- Paulista-PE
- Recife-PE
- Jaboatão dos Guararapes-PE
- Ipojuca-PE
- Rio de Janeiro-RJ
- Salvador-BA *(em desenvolvimento)*

## O que vem na planilha

- **Resumo** — uma linha por inscrição: situação da consulta, contribuinte, endereço e
  total em aberto;
- **Detalhe** — uma linha por débito: exercício, tributo, vencimento e valores
  (original, correção, multa, juros);
- **Metadados** — data da consulta e totais do lote.

Cada inscrição recebe uma situação clara:

| Situação | Significado |
|---|---|
| `OK` | Consulta concluída |
| `OK_CONFERIR` | Concluída, com observação a revisar |
| `ERRO_DADO` | Inscrição inválida ou inexistente no portal |
| `FALHA_*` | Portal indisponível no momento — consulta refeita automaticamente |

## Como funciona

1. Você envia a planilha com as inscrições (e o município, quando houver mais de um).
2. As consultas são feitas nos portais oficiais das prefeituras.
3. Você recebe a planilha preenchida.

A cobrança é **por consulta realizada**.

## Sobre este repositório

Este repositório é apenas informativo. O código-fonte é proprietário e não está
disponível publicamente.

Os dados consultados são públicos nos portais das prefeituras e são tratados apenas
para a finalidade contratada, conforme a LGPD.
