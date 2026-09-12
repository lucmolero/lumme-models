# Matriz de plugins de voz

Pesquisa global em 12/09/2026. A classificação combina qualidade percebida,
suporte a português, execução offline no Android, tamanho e licença. Um projeto
popular não entra automaticamente no catálogo: o peso e a licença do modelo
também precisam ser distribuíveis.

| Projeto | GitHub | Português | Android/offline | Licença e decisão |
| --- | --- | --- | --- | --- |
| Kokoro 82M + sherpa-onnx | [hexgrad/Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) / [k2-fsa/sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) | PT-BR no pacote multilíngue | ONNX, CPU, rápido | Apache-2.0; **produção agora**. |
| RHVoice | [RHVoice/RHVoice](https://github.com/RHVoice/RHVoice) | Português brasileiro (`letícia-f123`) | Runtime Android nativo, footprint pequeno | GPL-2.0 no core e licenças separadas para dados/voz; **não empacotar sem auditoria jurídica completa**. |
| OpenVoice V2 | [myshell-ai/OpenVoice](https://github.com/myshell-ai/OpenVoice) | Não há PT-BR nativo documentado | PyTorch, pesado para o APK | MIT, mas **Lab/servidor**; não é runtime Android imediato. |
| Chatterbox Multilingual | [resemble-ai/chatterbox](https://github.com/resemble-ai/chatterbox) | Multilíngue, validar `pt` por checkpoint | ~500M, PyTorch | MIT no código/pesos publicados; **Lab/servidor** até haver ONNX/benchmark Android. |
| XTTS v2 | [coqui-ai/TTS](https://github.com/coqui-ai/TTS) | Português incluído | Grande, PyTorch | CPML não comercial; **não distribuir no Lumme comercial** sem licença. |
| Fish Speech S2 | [fishaudio/fish-speech](https://github.com/fishaudio/fish-speech) | Multilíngue | 4B, exige GPU/servidor | Fish Audio Research License exige licença comercial; **não baixar no app**. |
| F5-TTS | [SWivid/F5-TTS](https://github.com/SWivid/F5-TTS) | Checkpoints comunitários variam | Grande, PyTorch | Pesos frequentemente CC-BY-NC; **Lab de avaliação**, não catálogo comercial. |
| StyleTTS2 | [yl4579/StyleTTS2](https://github.com/yl4579/StyleTTS2) | Base principal em inglês | Desktop/CPU, sem pacote Android oficial | Código MIT, pesos com restrições de dataset; **pesquisa**, não PT-BR de produção. |
| MeloTTS | [myshell-ai/MeloTTS](https://github.com/myshell-ai/MeloTTS) | Lista oficial não inclui PT-BR | CPU, mas Python | MIT; **não priorizar** até existir checkpoint PT-BR verificável. |
| Pocket TTS | [kyutai-labs/pocket-tts](https://github.com/kyutai-labs/pocket-tts) | Validar idiomas do checkpoint | CPU, Python | MIT; **pesquisa**, sem runtime Android/PT-BR pronto. |

## Política do Lumme

1. Voz nativa Android é o fallback instantâneo e padrão.
2. Kokoro é o primeiro plugin premium offline porque já possui runtime sherpa,
   pacote fp32, hash fixo e caminho de ativação atômica. O fp32 é deliberado:
   há relatos de artefatos e menor eficiência do int8 em Android/ARM.
3. RHVoice fica como alternativa de acessibilidade/integrador externo, não como
   download do Lumme, até que as licenças dos dados e da voz estejam completas.
4. Modelos de clonagem ou de servidor aparecem no Lab somente como “avançado”
   quando o uso e a licença estiverem claros; nunca como download automático.
5. O catálogo usa apenas releases/tag imutáveis, HTTPS, SHA-256 e arquivos
   obrigatórios declarados. O app rejeita metadados incompletos.
