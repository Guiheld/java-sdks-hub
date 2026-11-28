# SDKs Java `solutions.held` — hub da família

Hub de **planejamento e coordenação** das SDKs Java para APIs públicas brasileiras, publicadas sob o
groupId Maven `solutions.held`. **O código não fica aqui** — cada SDK vive no seu próprio repositório.
Este repositório hospeda o **roadmap** (o board abaixo) e as **issues** que alimentam o **kanban público**.

> 📋 **Board / roadmap:** https://github.com/users/Guiheld/projects/4

## SDKs da família

| SDK | Repositório (código) | Coordenadas (core) |
|---|---|---|
| **PNCP** — contratações públicas | [Guiheld/PNCP-JAVA-SDK](https://github.com/Guiheld/PNCP-JAVA-SDK) | `solutions.held:pncp-java-sdk` |
| **BCB** — dados econômicos (SGS/PTAX/Focus) | [Guiheld/BCB-DADOS-JAVA-SDK](https://github.com/Guiheld/BCB-DADOS-JAVA-SDK) | `solutions.held:bcb-dados-java-sdk` |

As próximas candidatas (SICONFI, IBGE, …) estão no [board](https://github.com/users/Guiheld/projects/4),
na coluna **Research**.

## Como está organizado

- `pncp/`, `bcb/` — **submódulos git** apontando para o repositório de cada SDK. O código vive lá;
  aqui fica só o ponteiro. Para clonar com tudo: `git clone --recursive`, ou, num clone já feito,
  `git submodule update --init`.
- As **issues** e o **board** (acima) guardam o roadmap: candidatas, prioridade e ciclo de vida de cada SDK.

## Padrão das SDKs

Todas seguem o mesmo blueprint: reator Maven multi-módulo (core + Spring Boot starter), Java 17,
dependência de runtime só Jackson, docs em pt-BR, Apache-2.0. A família é **read-only** (somente GET)
e **sem autenticação** (exceto quando a API exigir, como no Portal da Transparência).

Suporte a *Quarkus* pode ser adicionado no futuro, mas ainda não há demanda que justifique manter mais
um reator multi-módulo.

## Contribuindo

Quer propor uma nova SDK ou colaborar? Abra uma issue pelo template **"Proposta de nova SDK"** ou
comente numa candidata do [board](https://github.com/users/Guiheld/projects/4). Issues marcadas com
`good first issue` e `help wanted` são bons pontos de entrada.

## Licença

[Apache-2.0](LICENSE).
