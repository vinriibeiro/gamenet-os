# Gamenet OS

Central de gestão e monitoramento para um provedor de internet. A ideia é ficar por cima dos sistemas que a operação já usa (SGP, Chatmix, rede) e reunir indicadores, cobrança e acompanhamento em um só lugar, sem substituí-los.

> **Status:** protótipo navegável + proposta. Não há integração real com nenhum sistema. **Todos os números e nomes exibidos são fictícios.**

**Demo:** https://vinriibeiro.github.io/gamenet-os/

## O que tem aqui

| Pasta | Conteúdo |
|---|---|
| `index.html` | Apresentação da proposta para a diretoria (problema, escopo, riscos, plano) |
| `prototipo/` | Protótipo navegável: 12 áreas, 4 perfis de acesso, cobrança com histórico e auditoria salvos no navegador, instalável como PWA |
| `landing/` | Landing page comercial: planos e consulta de cobertura por CEP com envio ao WhatsApp |
| `assets/` | Logos e ícone |

## Decisões de projeto

- **Sem build e sem dependências:** HTML, CSS e JavaScript puros. Abre em qualquer servidor estático e publica direto no GitHub Pages.
- **Dados simulados e determinísticos:** gerados por um gerador pseudoaleatório com semente fixa (`prototipo/data.js`), então a demo mostra sempre os mesmos números.
- **Perfis de acesso:** a mesma base de dados muda conforme o perfil (diretoria, cobrança, técnico etc.), simulando as permissões do sistema real.
- **Persistência local:** histórico de cobrança e auditoria ficam no `localStorage` do navegador; nada é enviado a servidor.
- **Integrações previstas somente leitura**, para não arriscar a operação existente.

## Rodar localmente

```bash
python -m http.server 8765
```

Abra http://localhost:8765 (apresentação), `/prototipo/` ou `/landing/`.

## Próximos passos (MVP)

- Next.js + TypeScript e PostgreSQL
- Fila de sincronização
- Conectores somente leitura para SGP, Chatmix, PABX e Zabbix, após confirmar o acesso com cada fornecedor

## Autor

Vinícius Ribeiro · [LinkedIn](https://www.linkedin.com/in/vinriibeiro/) · [GitHub](https://github.com/vinriibeiro)

Projeto desenvolvido com apoio de IA (Claude Code) na codificação; o produto, o escopo e as decisões são meus.
