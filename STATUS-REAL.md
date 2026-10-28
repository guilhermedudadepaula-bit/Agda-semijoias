# Estado real do AGDA Semijoias

Atualizado em 2026-10-28.

## Confirmado
- O repositório GitHub contém `index.html`, que é uma demonstração local com `localStorage`.
- O projeto Supabase `atrbkrrkwsebfgeslmok` tem as funções `tiny-readonly-test` (v3) e `tiny-import-products` (v1) ativas, ambas exigindo JWT.
- A função de importação foi revisada: ela exige perfil `owner` aprovado e deliberadamente não grava `stock_general`.

## Ainda não validado
- A importação real da Tiny ainda não foi executada com uma sessão autenticada da proprietária.
- A interface web ainda não está ligada à autenticação e às tabelas reais.
- Fluxos de aprovação, vendas, comissão e fechamento de maleta precisam de testes integrados antes de uso real.

## Próxima sequência segura
1. Integrar o cliente Supabase no frontend com apenas a chave publishable.
2. Implementar login/cadastro e autorização real por perfil.
3. Ligar produtos e maletas às tabelas e funções RPC já existentes.
4. Testar com dados de teste, conferir importação Tiny e estoque antes de publicar.

Nunca colocar `TINY_API_TOKEN`, `service_role` ou chaves secretas no navegador.