# Fontes de vozes brasileiras

Inventário pesquisado em 12/09/2026. O Lumme baixa somente URLs HTTPS
versionadas e verifica SHA-256; não copia pesos de repositórios de terceiros.

## Referências brasileiras no GitHub

| Projeto | Uso | Decisão |
| --- | --- | --- |
| [RHVoice](https://github.com/RHVoice/RHVoice) | Runtime Android local com português brasileiro | Melhor alternativa aberta para acessibilidade, mas exige auditoria das licenças separadas de idioma/voz. |
| [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) | Vozes `pf_dora`, `pm_alex` e `pm_santa` em pt-BR | Base premium escolhida; executada com sherpa-onnx no Android. |

## Decisão de distribuição

Piper não será distribuído nem usado no Lumme. O produto usa a voz nativa do
Android como caminho instantâneo e Kokoro fp32 como plugin premium opcional;
RHVoice permanece uma referência externa até a revisão de licenças dos dados.
