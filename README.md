# Lumme model repository

Catálogo versionado de plugins de voz e livros públicos para o Lumme. O app
consome os manifestos por HTTPS, valida SHA-256 e mantém pesos/PDFs fora do APK.

Repositório: https://github.com/lucmolero/lumme-models
Catálogo de vozes: https://raw.githubusercontent.com/lucmolero/lumme-models/v1.0.13/catalog.json
Catálogo de livros: https://raw.githubusercontent.com/lucmolero/lumme-models/v1.0.13/free-books.json

## Publicação

Use releases/tags imutáveis, URLs HTTPS e hashes calculados localmente. O app
funciona sem rede com o catálogo embutido e a voz nativa Android. Livros são
somente descoberta até o usuário tocar em **Baixar e importar**.

## Vozes

O catálogo de produção contém Kokoro fp32 (studio, três perfis PT-BR) e
Supertonic 3 int8 (natural, dez estilos M1-M5/F1-F5). Piper foi excluído.

## Livros públicos

`free-books.json` inclui obras em domínio público com páginas PDF verificadas,
licença, fonte, tamanho e SHA-256. A Biblioteca mostra a origem e permite abrir
a fonte ou baixar/importar explicitamente.
