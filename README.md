# Automações de Processos — Portfólio

Automações que desenvolvi em produção numa entidade de previdência e saúde
suplementar (2023–2026), cobrindo cadastro de beneficiários, cobrança,
tesouraria e controladoria.

> O código-fonte pertence à empresa e não é publicado. Cada caso descreve
> problema, arquitetura e decisões técnicas. As técnicas são demonstradas
> com código completo nos meus projetos pessoais, linkados em cada caso.

## Casos

| # | Automação | Área | Stack principal | Destaque técnico |
|---|-----------|------|-----------------|------------------|
| 1 | [Sincronização de cadastro com operadora de saúde](casos/01-sincronizacao-cadastro.md) | Cadastro | Python, API REST, Oracle | Travas contra movimentações em massa |
| 2 | [Biblioteca RPA compartilhada](casos/02-biblioteca-rpa.md) | Plataforma | Python, Selenium, Azure Key Vault | Base de 7+ robôs em produção |
| 3 | [Extração de extratos de fundos em PDF](casos/03-extratos-pdf.md) | Controladoria | PyPDF, openpyxl | Fórmulas Excel ajustadas automaticamente |
| 4 | [Cadeia de cancelamento de boletos](casos/04-cancelamento-boletos.md) | Tesouraria | RPA desktop + web, VBA | Orquestra 3 sistemas |
| 5 | [Higienização de contatos de cobrança](casos/05-contatos-cobranca.md) | Cobrança | pandas, Selenium, regex | Reenvio automático isolando a linha rejeitada |

## Competências demonstradas

- **Integração:** APIs REST, OAuth, consulta de status até a conclusão, paginação
- **Dados:** reconciliação de bases grandes, de-para, validação de CPF/e-mail
- **RPA:** Selenium, PyAutoGUI, OCR (Tesseract + OpenCV)
- **Confiabilidade:** timeouts, idempotência, travas contra dados parciais,
  log em banco, alertas
- **Infra:** Oracle (SQLAlchemy), Azure Key Vault, ambientes dev/hml/prod
