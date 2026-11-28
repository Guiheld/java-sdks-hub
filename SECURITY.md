# Política de Segurança

Este repositório é um **hub de planejamento e coordenação** — ele não distribui código nem
artefatos. As bibliotecas da família ficam nos repositórios de cada SDK, cada um com sua própria
política de segurança.

## Como reportar uma vulnerabilidade

- **Em uma das SDKs** (PNCP, BCB, …): reporte de forma **privada** no repositório correspondente,
  pelo recurso de _security advisory_ do GitHub, seguindo o `SECURITY.md` daquele repo. **Não** abra
  uma _issue_ pública.
- **Neste hub** (conteúdo do repositório, board ou templates): abra uma _issue_ ou reporte de forma
  privada aos mantenedores.

> As APIs cobertas pela família são públicas e somente leitura, e as SDKs não armazenam credenciais.
> Ainda assim, levamos a sério qualquer questão de segurança.
