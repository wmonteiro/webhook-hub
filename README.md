# Webhook Hub

Serviço em PHP 8.3 + PostgreSQL para ingestão assíncrona de webhooks com:
- Validação de assinatura HMAC
- Idempotência garantida por restrição única no banco
- Fila transacional (`FOR UPDATE SKIP LOCKED`)
- Retentativas com *backoff* exponencial e Dead Letter Queue (DLQ)

## Como rodar (em desenvolvimento)
```bash
docker compose up -d