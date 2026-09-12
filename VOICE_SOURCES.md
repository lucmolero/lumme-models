# Fontes de vozes brasileiras

Inventário pesquisado em 12/09/2026. O Lumme baixa somente URLs HTTPS
versionadas e verifica SHA-256; não copia pesos de repositórios de terceiros.

## Referências brasileiras no GitHub

| Projeto | Uso | Decisão |
| --- | --- | --- |
| [Vozia](https://github.com/leoberbert/Vozia) | CLI MIT usando sherpa-onnx e Piper PT-BR | Referência de integração; pesos continuam no release oficial. |
| [text-to-speech-with-piper](https://github.com/jvictorpdl/text-to-speech-with-piper) | Fluxo local e testes com `pt_BR-faber-medium` | Referência de UX/benchmark; repositório em estudo, sem redistribuir pesos. |
| [tts-acessibilidade-pt-br](https://github.com/renatoork/tts-acessibilidade-pt-br) | Comparação Piper, Kokoro e XTTS para acessibilidade | Referência de avaliação; CPML do XTTS não entra no catálogo comercial. |

## Pacotes PT-BR auditáveis

Os pacotes abaixo são releases oficiais do sherpa-onnx e aparecem na página de
modelos PT-BR. O catálogo do Lumme pode ativá-los depois que o runtime VITS e o
resampling do Android forem habilitados; por enquanto, Kokoro continua sendo o
único runtime premium de produção.

| ID | Perfil | Tamanho | SHA-256 | Download |
| --- | --- | ---: | --- | --- |
| `vits-piper-pt_BR-cadu-medium-int8` | Cadu, médio, int8 | 21,135,464 | `78f1caf0a74cc6cb8dedaff87affd232ee653d5b0394d4cf4d2e97ecbfa5ff3d` | [release](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-pt_BR-cadu-medium-int8.tar.bz2) |
| `vits-piper-pt_BR-faber-medium-int8` | Faber, médio, int8 | 21,336,772 | `dbc8b1d7d729fd417ea78a350ed35696c928770ac93513d3f507bd4e88eee3fd` | [release](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-pt_BR-faber-medium-int8.tar.bz2) |
| `vits-piper-pt_BR-jeff-medium-int8` | Jeff, médio, int8 | 21,211,448 | `21a8883f9662c784dd5653fd9d5cb9aaae2551c70e16854e81ff4a9c96470e6a` | [release](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-pt_BR-jeff-medium-int8.tar.bz2) |
| `vits-piper-pt_BR-edresson-low-int8` | Edresson, leve, int8 | 21,198,064 | `9ec0b016cfab3778263406970b3ee0e2e30860b05046fa1e5cb6460edb7f8251` | [release](https://github.com/k2-fsa/sherpa-onnx/releases/download/tts-models/vits-piper-pt_BR-edresson-low-int8.tar.bz2) |

O catálogo oficial lista esses perfis PT-BR e fornece exemplos Kotlin/Android;
o arquivo [VOICES.md](https://github.com/rhasspy/piper/blob/master/VOICES.md)
documenta as vozes e seus arquivos de configuração. A compatibilidade e a
licença de cada voz devem ser verificadas antes de distribuição comercial.
