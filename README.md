# Lumme model repository

Catálogo versionado de plugins de voz e conteúdo livre para o Lumme. O app
consome `catalog.json` por HTTPS e valida SHA-256 antes de ativar qualquer
modelo. Os pesos permanecem fora do APK e cada fornecedor mantém a licença.

Repositório público: https://github.com/lucmolero/lumme-models
Catálogo de produção: https://raw.githubusercontent.com/lucmolero/lumme-models/v1.0.4/catalog.json

## Publicação

1. Publique alterações neste repositório público em uma branch protegida.
2. Gere `catalog.json` com URLs HTTPS imutáveis (release/tag, nunca `main`) e
   SHA-256 calculado localmente.
3. Configure no app a URL raw do catálogo por build flavor. Sem rede, o
   catálogo embutido e a voz nativa do Android continuam funcionando.
4. Só adicione pesos cuja licença permita redistribuição; pesos sem licença
   clara ficam como referência, nunca como download automático.

O catálogo `v1.0.4` já está publicado. O app mantém os plugins embutidos e a
voz nativa mesmo quando a rede está indisponível.

## Vozes brasileiras encontradas

Projetos brasileiros como [Vozia](https://github.com/leoberbert/Vozia),
[text-to-speech-with-piper](https://github.com/jvictorpdl/text-to-speech-with-piper)
e [tts-acessibilidade-pt-br](https://github.com/renatoork/tts-acessibilidade-pt-br)
foram usados como referências de integração e avaliação. Eles apontam para
modelos Piper/Kokoro publicados nos canais oficiais; os repositórios não são
tratados como espelhos de pesos. A lista de vozes PT-BR (cadu, edresson, faber
e jeff) e os links versionados estão documentados em `VOICE_SOURCES.md`.

## Conteúdo livre

`free-books.json` contém apenas metadados e links de fontes públicas; o usuário
sempre escolhe o download e deve verificar a licença territorial da obra.
