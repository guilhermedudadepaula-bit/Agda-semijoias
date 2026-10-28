# AGDA Semijoias — retomada da integração

## Estado confirmado
- O protótipo `index.html` ainda usa `localStorage`; não é o sistema real.
- A integração com o Tiny deve ocorrer por funções seguras no Supabase, nunca expondo o token no navegador.
- A importação deve atualizar os dados dos produtos sem sobrescrever `stock_general`.

## Próximo passo
Validar a função `tiny-import-products` com uma sessão autenticada de proprietária e conferir os campos retornados pela API do Tiny antes de habilitar a operação no painel.

## Regra de segurança
Não publicar segredos no frontend. Se o token da Tiny foi compartilhado em mensagens ou código, rotacioná-lo no Tiny e atualizar o segredo `TINY_API_TOKEN` no Supabase.