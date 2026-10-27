# Gamenet OS

Central de gestão e monitoramento para a Gamenet (provedor de internet). Fica por cima do SGP, do Chatmix e da rede, sem substituí-los.

- `index.html`: apresentação da proposta para a diretoria.
- `landing/`: landing page comercial (planos, cobertura por CEP com envio ao WhatsApp).
- `prototipo/`: protótipo navegável (12 áreas, 4 perfis de acesso, cobrança com histórico e auditoria salvos no navegador, PWA).

**Todos os números do protótipo são fictícios** e servem só para demonstração.

## Rodar localmente

```bash
python -m http.server 8765
```

Abra http://localhost:8765.

## Próximos passos (MVP)

Next.js + TypeScript, PostgreSQL, fila de sincronização, conectores somente leitura para SGP, Chatmix, PABX e Zabbix (após confirmar o acesso com cada fornecedor).
