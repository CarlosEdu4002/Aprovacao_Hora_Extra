# Workflow unificado de aprovação de hora extra no n8n

Exemplo público de um workflow único que reúne:

- coleta periódica de solicitações em uma origem de exemplo;
- prevenção de duplicidade e armazenamento em Data Tables;
- envio de e-mails com links de aprovação ou recusa;
- confirmação e registro da decisão por webhooks;
- sincronização incremental com uma aba do Google Sheets.

## Importação

1. No n8n, use **Import from File** e selecione `workflow-unificado-horas-extras.json`.
2. Abra a nota **Instruções • Configurar o exemplo** no canvas.
3. Substitua todos os placeholders listados abaixo.
4. Selecione suas credenciais SMTP e Google Service Account.
5. Execute manualmente cada um dos gatilhos e confira os dados antes de ativar o workflow.

## Placeholders

| Placeholder | Substituir por |
| --- | --- |
| `SUBSTITUA_PELO_ID_DA_DATA_TABLE` | ID da Data Table usada no exemplo |
| `SUBSTITUA_PELO_ID_DA_PLANILHA` | ID da planilha de destino |
| `https://api.exemplo.com/...` | URLs das APIs de origem |
| `https://SEU-N8N.EXEMPLO.COM` | URL pública HTTPS da instância n8n |
| endereços `@exemplo.com` | remetentes e destinatários reais |

A aba esperada é `SOLICITACOES`. A chave utilizada para evitar duplicidade é `Codigo`.

## Segurança

O arquivo está inativo e não contém credenciais, IDs de credenciais, e-mails reais, URLs internas, IDs reais de Data Tables ou ID real de planilha.
