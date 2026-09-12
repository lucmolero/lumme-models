# Lumme model repository

Catálogo versionado de plugins de voz e conteúdo livre para o Lumme. O app
consome `catalog.json` por HTTPS e valida SHA-256 antes de ativar qualquer
modelo. Os pesos permanecem fora do APK e cada fornecedor mantém a licença.

Repositório público: https://github.com/lucmolero/lumme-models
Catálogo de produção: https://raw.githubusercontent.com/lucmolero/lumme-models/v1.0.8/catalog.json

## Publicação

1. Publique alterações neste repositório público em uma branch protegida.
2. Gere `catalog.json` com URLs HTTPS imutáveis (release/tag, nunca `main`) e
   SHA-256 calculado localmente.
3. Configure no app a URL raw do catálogo por build flavor. Sem rede, o
   catálogo embutido e a voz nativa do Android continuam funcionando.
4. Só adicione pesos cuja licença permita redistribuição; pesos sem licença
   clara ficam como referência, nunca como download automático.

O catálogo `v1.0.8` já está publicado. O app mantém os plugins embutidos e a
voz nativa mesmo quando a rede está indisponível.

## Vozes brasileiras encontradas

As referências principais são [RHVoice](https://github.com/RHVoice/RHVoice),
que tem runtime Android e português brasileiro, e
[Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M), que alimenta o plugin
premium sherpa-onnx. O catálogo não copia pesos de terceiros; cada pacote é
baixado por release imutável e validado antes da ativação. Piper foi excluído da
estratégia do produto.

## Conteúdo livre

`free-books.json` contém apenas metadados e links de fontes públicas; o usuário
sempre escolhe o download e deve verificar a licença territorial da obra.
