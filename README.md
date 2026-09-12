# Lumme model repository

Catálogo versionado de plugins de voz e conteúdo livre para o Lumme. O app
consome `catalog.json` por HTTPS e valida SHA-256 antes de ativar qualquer
modelo. Os pesos permanecem fora do APK e cada fornecedor mantém a licença.

## Publicação

1. Crie um repositório público (por exemplo `lumme-models`) e publique este
   diretório em uma branch protegida.
2. Gere `catalog.json` com URLs HTTPS imutáveis (release/tag, nunca `main`) e
   SHA-256 calculado localmente.
3. Configure no app a URL raw do catálogo por build flavor. Sem rede, o
   catálogo embutido e a voz nativa do Android continuam funcionando.
4. Só adicione pesos cuja licença permita redistribuição; pesos sem licença
   clara ficam como referência, nunca como download automático.

O remoto ainda não foi criado neste ambiente porque não há conta Git/token
disponível. Depois, a URL de produção será
`https://raw.githubusercontent.com/<org>/lumme-models/<tag>/catalog.json`.

## Conteúdo livre

`free-books.json` contém apenas metadados e links de fontes públicas; o usuário
sempre escolhe o download e deve verificar a licença territorial da obra.
