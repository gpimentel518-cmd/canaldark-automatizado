# 🎬 Dark Channel Bot — Pipeline Automático de Vídeos para YouTube

> Do tema ao upload: pipeline completo que gera, produz e publica vídeos para canais dark no YouTube sem intervenção manual.

---

## O problema que resolve

Canais dark (true crime, mistérios, horror) precisam de volume constante de publicação. Produzir vídeo por vídeo manualmente é lento e caro. Este bot automatiza 100% do pipeline de produção.

---

## Pipeline completo

```
Tema / palavra-chave
        ↓
① Geração de roteiro (LLM)
        ↓
② Narração em voz natural (TTS)
        ↓
③ Seleção de imagens e B-roll
        ↓
④ Montagem automática + legendas
        ↓
⑤ Thumbnail gerada com IA
        ↓
⑥ Upload + metadados SEO no YouTube
        ↓
⑦ Publicação agendada ✅
```

---

## Funcionalidades

- ✅ Roteiro completo gerado a partir de um tema ou título
- ✅ Narração com voz natural customizável (ElevenLabs / OpenAI TTS)
- ✅ Montagem automática com imagens e B-roll
- ✅ Legendas sincronizadas geradas automaticamente
- ✅ Thumbnail com texto e layout otimizado para CTR
- ✅ Upload direto na YouTube API com título, descrição e tags SEO
- ✅ Agendamento de publicação
- ✅ Relatório de vídeos publicados

---

## Stack

| Componente | Tecnologia |
|-----------|-----------|
| Orquestração | n8n · Python |
| Geração de roteiro | OpenAI GPT-4o |
| Text-to-Speech | ElevenLabs / OpenAI TTS |
| Edição de vídeo | MoviePy · FFmpeg |
| Thumbnail | Pillow |
| Publicação | YouTube Data API v3 |

---

## Estrutura do projeto

```
dark-channel-bot/
├── flows/
│   └── video_pipeline.json          # Orquestração n8n (exemplo)
├── prompts/
│   └── roteiro_dark.txt             # Prompt de estilo do canal
├── scripts/
│   ├── roteiro_generator.py         # Geração de roteiro com IA
│   ├── tts_generator.py             # Narração automática
│   ├── video_editor.py              # Montagem do vídeo
│   ├── thumbnail_creator.py         # Geração de thumbnail
│   └── youtube_uploader.py          # Upload e publicação
├── assets/
│   └── templates/                   # Templates de thumbnail
├── .env.example
└── README.md
```

---

## Configuração

```bash
# 1. Clone o repositório
git clone https://github.com/SEU-USUARIO/dark-channel-bot.git

# 2. Instale dependências
pip install -r requirements.txt
# FFmpeg deve estar instalado no sistema

# 3. Configure as variáveis de ambiente
cp .env.example .env

# 4. Autentique com a YouTube API
python scripts/youtube_uploader.py --auth

# 5. Teste com um tema
python scripts/roteiro_generator.py --tema "O caso mais misterioso do Brasil"
```

---

## Customização

O arquivo `prompts/roteiro_dark.txt` define o estilo, tom e estrutura. Adapte para o nicho do seu canal: true crime, horror, conspiração, etc.

---

## Resultado

- 🎬 Vídeo do roteiro ao upload em **~15 minutos**
- 📅 Canal publicando **diariamente** no piloto automático
- 💰 Custo por vídeo: **< R$ 2,00** em APIs

---

> ⚠️ Use de forma responsável e dentro dos Termos de Serviço do YouTube.

> 💼 Disponível para customização por nicho. [Entre em contato](mailto:SEU@EMAIL.COM)
