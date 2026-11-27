# held-java-sdks — hub da família de SDKs Java

Hub de **planejamento e coordenação** das SDKs Java para APIs públicas brasileiras, publicadas sob o
groupId Maven `solutions.held`. **O código não fica aqui** — cada SDK vive no seu próprio repositório
(links abaixo). Este repositório existe para hospedar o **roadmap** e as **issues** que alimentam o
**kanban público** (GitHub Projects) da família.

## SDKs da família

| SDK                                         | Repositório (código)                                                        | Coordenadas (core)                  |
|---------------------------------------------|-----------------------------------------------------------------------------|-------------------------------------|
| **PNCP** — Consulta (contratações públicas) | [Guiheld/PNCP-JAVA-SDK](https://github.com/Guiheld/PNCP-JAVA-SDK)           | `solutions.held:pncp-java-sdk`      | 
| **BCB** — Dados econômicos (SGS/PTAX/Focus) | [Guiheld/BCB-DADOS-JAVA-SDK](https://github.com/Guiheld/BCB-DADOS-JAVA-SDK) | `solutions.held:bcb-dados-java-sdk` |

## Como está organizado

- `pncp/`, `bcb/` — **submódulos git** apontando para o repositório de cada SDK. O código vive lá; aqui
  fica só o ponteiro.
- [`ROADMAP.md`](ROADMAP.md) — pipeline de SDKs futuras (candidatas, com veredito de demanda e gap de Java).

## Padrão das SDKs

Todas seguem o mesmo blueprint (reator Maven multi-módulo, core + Spring Boot starter, Java 17,
dependência de runtime só Jackson, docs em pt-BR, Apache-2.0).

Futuramente será adicionado para o querido *Quarkus* porém ainda não há demanda suficiente para justificar o esforço de manutenção de mais um
    reator multi-módulo. A família é **read-only** (somente GET) e **sem autenticação** (exceto quando a API exigir, como no caso do Portal da Transparência).
