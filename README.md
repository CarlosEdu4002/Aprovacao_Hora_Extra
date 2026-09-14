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

## Exemplos do Fluxo

**Imagem Ampla do FLuxo Completo** 
<img width="714" height="444" alt="c14db30a-2053-4a83-83c2-8c130195987f" src="https://github.com/user-attachments/assets/38afbbd8-c7dc-4460-9e6b-5fe4c9dce4c0" />

**Área1 (Coleta de resposta forms e envio de emails)**
<img width="1159" height="311" alt="5c65d8e1-4fdf-49c2-889e-caa5299270e9" src="https://github.com/user-attachments/assets/fc7704fd-3629-4c5e-b022-a8afbc714141" />

**Área2 (Coleta de resposta do aprovador via Webhook)**
<img width="1053" height="444" alt="d1fe636c-3e0f-4b2c-b02e-85fd5ce42600" src="https://github.com/user-attachments/assets/212efab4-46e8-48ff-981f-2bc3e5473a9f" />

**Área3 (Marcação da planilha no googlesheets)**
<img width="936" height="189" alt="0db83865-5277-40de-9112-f6dc570bd457" src="https://github.com/user-attachments/assets/e841359f-6cdb-4663-b2d5-8533a781e923" />

*Exemplos dos email enviados e da tela de confirmação do aceite e/ou recusa*

<img width="992" height="637" alt="50f67155-6902-4c1d-a011-ec0f2648d173" src="https://github.com/user-attachments/assets/dd1b6ae2-8e87-493d-bc11-20b52f8d3e8f" />
<img width="1032" height="688" alt="c9f37faf-7d35-4118-bc97-a0df1d224e87" src="https://github.com/user-attachments/assets/a6bd8c24-e749-44a5-a451-e6ecf6fdeeab" />


## Segurança

O arquivo está inativo e não contém credenciais, IDs de credenciais, e-mails reais, URLs internas, IDs reais de Data Tables ou ID real de planilha.
