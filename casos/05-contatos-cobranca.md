# Higienização de contatos de cobrança

## Contexto
A plataforma de cobrança precisava dos e-mails atualizados dos pagadores,
mas a base cadastral tinha e-mails inválidos, duplicados e placeholders.

## Solução
Robô que extrai as bases cadastrais, valida e consolida os contatos e
importa na plataforma, isolando os registros problemáticos.

```mermaid
flowchart LR
    A[Bases cadastrais] --> V[Validação]
    V -->|válidos| C[Consolidação por CPF]
    V -->|inválidos| E[Relatório de erros]
    C --> I[Importação na plataforma]
    I -->|linha rejeitada| X[Remove a linha e tenta de novo]
    X --> I
```

## Decisões técnicas
- **Validação em camadas:** regex de formato + lista de domínios permitidos +
  bloqueio de placeholders
- **Consolidação:** vários e-mails do mesmo CPF viram um campo único
- **Importação autocorretiva:** quando a plataforma rejeita o arquivo, o robô
  lê o número da linha no retorno, move o registro para a base de erros e
  reenvia até a importação passar

## Stack
Python · pandas · Selenium · regex

## Resultado
- Execução 3× por semana via agendador
