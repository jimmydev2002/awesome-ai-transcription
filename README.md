# Awesome AI Transcription [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome AI-powered transcription tools, speech-to-text APIs, open-source models, libraries, datasets, and resources.

AI transcription has evolved rapidly — from research models to production-ready APIs and consumer tools. This list helps developers, content creators, researchers, and professionals find the right tool for their use case.

## Contents

- [SaaS Tools](#saas-tools)
- [Speech-to-Text APIs](#speech-to-text-apis)
- [Open-Source Models](#open-source-models)
- [Desktop & Mobile Apps](#desktop--mobile-apps)
- [Libraries & SDKs](#libraries--sdks)
- [Browser Extensions](#browser-extensions)
- [Self-Hosted Solutions](#self-hosted-solutions)
- [Subtitle & Caption Tools](#subtitle--caption-tools)
- [Meeting & Collaboration](#meeting--collaboration)
- [Podcast Transcription](#podcast-transcription)
- [Medical & Legal Transcription](#medical--legal-transcription)
- [Datasets](#datasets)
- [Benchmarks & Evaluation](#benchmarks--evaluation)
- [Research Papers](#research-papers)
- [Tutorials & Guides](#tutorials--guides)
- [Community](#community)

---

## SaaS Tools

Cloud-based transcription platforms that work in the browser.

| Tool | Languages | Key Features | Pricing |
|------|-----------|-------------|---------|
| [Vocova](https://vocova.app) | 100+ | URL import from 1000+ platforms, speaker diarization, bilingual export, SRT/VTT subtitles | Freemium |
| [Otter.ai](https://otter.ai) | English | Real-time transcription, meeting assistant, Zoom/Teams integration | Freemium |
| [TurboScribe](https://turboscribe.ai) | 98 | Unlimited transcription on paid plan, batch upload | Freemium |
| [Happy Scribe](https://www.happyscribe.com) | 120+ | Human + AI transcription, subtitle editor, API available | Freemium |
| [Sonix](https://sonix.ai) | 49 | Automated translation, multi-speaker detection, API | Paid |
| [Rev](https://www.rev.com) | English | Human + AI transcription, captions, high accuracy | Paid |
| [Descript](https://www.descript.com) | English | Audio/video editor with built-in transcription, filler word removal | Freemium |
| [Trint](https://trint.com) | 40+ | Collaborative editor, real-time transcription, API | Paid |
| [Notta](https://www.notta.ai) | 104 | Meeting recording, real-time transcription, AI summary | Freemium |
| [Riverside](https://riverside.fm) | 100+ | Recording + transcription, speaker detection, AI show notes | Freemium |
| [Transkriptor](https://transkriptor.com) | 100+ | Meeting bot, subtitle generation, multi-speaker | Paid |
| [AssemblyAI Playground](https://www.assemblyai.com/playground) | English | Free playground for testing AssemblyAI's API | Free |
| [Deepgram Playground](https://playground.deepgram.com) | 36 | Free playground for testing Deepgram's API | Free |
| [NovaScribe](https://novascribe.ai) | 100+ | Batch transcription, timestamp export | Freemium |

## Speech-to-Text APIs

APIs for developers building transcription into their applications.

### Cloud APIs

| API | Languages | Real-time | Key Features | Pricing Model |
|-----|-----------|-----------|-------------|---------------|
| [OpenAI Whisper API](https://platform.openai.com/docs/guides/speech-to-text) | 57 | No | Based on Whisper large-v2, simple REST API | Per minute |
| [AssemblyAI](https://www.assemblyai.com) | English, 17+ | Yes | Speaker diarization, sentiment analysis, topic detection, LeMUR | Per minute |
| [Deepgram](https://deepgram.com) | 36 | Yes | Nova-2 model, custom vocabulary, keyword boosting | Per minute |
| [Google Cloud Speech-to-Text](https://cloud.google.com/speech-to-text) | 125+ | Yes | V2 with Chirp model, medical dictation, multi-channel | Per minute |
| [Azure Speech Services](https://azure.microsoft.com/en-us/products/ai-services/speech-to-text) | 100+ | Yes | Custom models, pronunciation assessment, batch transcription | Per minute |
| [AWS Transcribe](https://aws.amazon.com/transcribe) | 100+ | Yes | Custom vocabulary, content redaction, toxicity detection | Per second |
| [Speechmatics](https://www.speechmatics.com) | 50+ | Yes | Ursa 2 model, translation, sentiment analysis | Per minute |
| [Rev AI](https://www.rev.com/api) | English, Spanish | Yes | Human-calibrated model, custom vocabulary | Per minute |
| [Gladia](https://www.gladia.io) | 99 | Yes | Whisper-based, speaker diarization, audio intelligence | Per minute |

### On-Premise / Private Cloud

| API | Languages | Key Features |
|-----|-----------|-------------|
| [Whisper.cpp Server](https://github.com/ggerganov/whisper.cpp) | 57 | C/C++ inference, runs on CPU, HTTP server mode |
| [faster-whisper Server](https://github.com/SYSTRAN/faster-whisper) | 57 | CTranslate2 backend, 4x faster than Whisper, lower memory |
| [Vosk Server](https://alphacephei.com/vosk) | 20+ | Lightweight, offline, Kaldi-based, works on Raspberry Pi |
| [Speechmatics On-Prem](https://www.speechmatics.com) | 50+ | Enterprise deployment, air-gapped environments |

## Open-Source Models

Pre-trained models you can run locally or fine-tune.

### Whisper Family

| Model | Parameters | Speed | Notes |
|-------|-----------|-------|-------|
| [Whisper](https://github.com/openai/whisper) | 39M–1.55B | 1x | Original OpenAI model, 57 languages |
| [Whisper large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo) | 809M | 8x faster than large-v3 | Best speed/accuracy tradeoff |
| [faster-whisper](https://github.com/SYSTRAN/faster-whisper) | Same | 4x faster | CTranslate2 backend, lower memory usage |
| [whisper.cpp](https://github.com/ggerganov/whisper.cpp) | Same | CPU-optimized | C/C++ port, runs on consumer hardware |
| [WhisperX](https://github.com/m-bain/whisperX) | Same | Fast | Word-level timestamps, speaker diarization via pyannote |
| [distil-whisper](https://github.com/huggingface/distil-whisper) | 756M | 6x faster | Distilled version, 1% WER degradation |
| [whisper-timestamped](https://github.com/linto-ai/whisper-timestamped) | Same | 1x | Accurate word-level timestamps |
| [Insanely Fast Whisper](https://github.com/Vaibhavs10/insanely-fast-whisper) | Same | 10x+ | Flash Attention 2 + batching, GPU-optimized |
| [buzz](https://github.com/chidiwilliams/buzz) | Same | 1x | Desktop GUI for Whisper, cross-platform |

### Other Models

| Model | Provider | Languages | Notes |
|-------|----------|-----------|-------|
| [Wav2Vec 2.0](https://huggingface.co/facebook/wav2vec2-large-960h) | Meta | English (multilingual variants available) | Self-supervised, fine-tunable |
| [HuBERT](https://huggingface.co/facebook/hubert-large-ls960-ft) | Meta | English | Hidden-unit BERT approach |
| [Conformer](https://github.com/NVIDIA/NeMo) | NVIDIA NeMo | 30+ | Production-grade, CTC + Transducer |
| [Moonshine](https://github.com/usefulsensors/moonshine) | Useful Sensors | English | Optimized for edge devices |
| [Parakeet](https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2) | NVIDIA | English | State-of-the-art English ASR |
| [Canary](https://huggingface.co/nvidia/canary-1b) | NVIDIA | 4 | Multilingual ASR + translation |
| [MMS](https://huggingface.co/facebook/mms-1b-all) | Meta | 1,100+ | Massively Multilingual Speech, covers low-resource languages |
| [SeamlessM4T](https://huggingface.co/facebook/seamless-m4t-v2-large) | Meta | 100+ | Speech-to-text + translation in one model |
| [Universal-1](https://www.assemblyai.com/blog/universal-1/) | AssemblyAI | English | Multilingual coming, SOTA on English benchmarks |

## Desktop & Mobile Apps

Native apps for transcription on desktop and mobile.

| App | Platform | Offline | Notes |
|-----|----------|---------|-------|
| [MacWhisper](https://goodsnooze.gumroad.com/l/macwhisper) | macOS | Yes | Native Mac app, Whisper-powered |
| [Buzz](https://github.com/chidiwilliams/buzz) | Windows, macOS, Linux | Yes | Open-source, Whisper GUI |
| [Whisper Transcription](https://apps.apple.com/app/whisper-transcription/id1668083311) | iOS | Yes | On-device transcription |
| [Live Transcribe](https://play.google.com/store/apps/details?id=com.google.audio.hearing.visualization.accessibility.scribe) | Android | No | Google's real-time transcription |
| [Aiko](https://sindresorhus.com/aiko) | macOS, iOS | Yes | On-device, by sindresorhus |
| [Superwhisper](https://superwhisper.com) | macOS | Yes | Voice-to-text input, dictation replacement |
| [Vibe](https://thewh1teagle.github.io/vibe/) | Windows, macOS, Linux | Yes | Open-source transcription app |

## Libraries & SDKs

Libraries for integrating transcription into your code.

### Python

- [openai-whisper](https://github.com/openai/whisper) - Official Whisper Python package.
- [faster-whisper](https://github.com/SYSTRAN/faster-whisper) - CTranslate2-based Whisper, 4x faster with lower memory.
- [whisperx](https://github.com/m-bain/whisperX) - Word-level timestamps and speaker diarization.
- [pyannote.audio](https://github.com/pyannote/pyannote-audio) - Speaker diarization and segmentation toolkit.
- [vosk-api](https://github.com/alphacep/vosk-api) - Offline speech recognition for 20+ languages.
- [nemo_toolkit](https://github.com/NVIDIA/NeMo) - NVIDIA's toolkit for ASR, NLP, and TTS.
- [speechbrain](https://github.com/speechbrain/speechbrain) - PyTorch-based speech toolkit for ASR, speaker ID, and more.
- [transformers](https://huggingface.co/docs/transformers/model_doc/whisper) - Hugging Face Whisper integration with pipeline API.
- [assemblyai](https://github.com/AssemblyAI/assemblyai-python-sdk) - Official AssemblyAI Python SDK.
- [deepgram-sdk](https://github.com/deepgram/deepgram-python-sdk) - Official Deepgram Python SDK.

### JavaScript / TypeScript

- [whisper-node](https://github.com/arietta-studio/whisper-node) - Whisper bindings for Node.js.
- [transformers.js](https://github.com/huggingface/transformers.js) - Run Whisper in the browser via WebAssembly.
- [@deepgram/sdk](https://github.com/deepgram/deepgram-js-sdk) - Official Deepgram JavaScript SDK.
- [assemblyai](https://github.com/AssemblyAI/assemblyai-node-sdk) - Official AssemblyAI Node.js SDK.
- [RecordRTC](https://github.com/muaz-khan/RecordRTC) - Browser audio/video recording for transcription pipelines.

### Other Languages

- [whisper.cpp](https://github.com/ggerganov/whisper.cpp) - C/C++ port with bindings for Go, Ruby, Java, Swift, and more.
- [whisper-rs](https://github.com/tazz4843/whisper-rs) - Rust bindings for whisper.cpp.
- [GoWhisper](https://github.com/ggerganov/whisper.cpp/tree/master/bindings/go) - Go bindings for whisper.cpp.

## Browser Extensions

- [Glasp](https://glasp.co) - YouTube transcript summarizer and highlighter.
- [YouTube Summary with ChatGPT](https://chromewebstore.google.com/detail/youtube-summary-with-chat/nmmicjeknamkfloonkhhcjmomieiodli) - Summarize YouTube videos using transcripts.
- [Transkriptor Chrome Extension](https://chromewebstore.google.com/detail/transkriptor/okkbmmnfbjclaeejhdgkhoamapopccpn) - Transcribe meetings and audio in the browser.

## Self-Hosted Solutions

Full solutions for running transcription on your own infrastructure.

- [Whisper Web](https://github.com/pluja/whishper) - Self-hosted speech-to-text with a web UI, Whisper-based.
- [Whisper API Server](https://github.com/innovatorved/whisper-openai-serverless-api) - Deploy Whisper as a REST API.
- [LocalAI](https://github.com/mudler/LocalAI) - OpenAI-compatible API that supports Whisper models.
- [wyoming-faster-whisper](https://github.com/rhasspy/wyoming-faster-whisper) - Wyoming protocol server for Home Assistant integration.
- [Scribe](https://github.com/JamesCobbledick/Scribe) - Self-hosted transcription with GPU support.

## Subtitle & Caption Tools

Tools focused on generating and editing subtitles.

- [Subtitle Edit](https://github.com/SubtitleEdit/subtitleedit) - Open-source subtitle editor with Whisper integration.
- [Aegisub](https://github.com/arch1t3cht/Aegisub) - Advanced subtitle editor (community fork).
- [autosubsync](https://github.com/smacke/autosubsync) - Automatically synchronize subtitles with audio.
- [ffsubsync](https://github.com/smacke/ffsubsync) - Auto-sync subtitles with video using audio fingerprinting.
- [Bazarr](https://github.com/morpheus65535/bazarr) - Companion app to Sonarr/Radarr for managing subtitles.
- [Subliminal](https://github.com/Diaoul/subliminal) - Python library for searching and downloading subtitles.
- [asbplayer](https://github.com/killergerbah/asbplayer) - Browser-based subtitle player for language learning.
- [Karaoke Captions](https://karaokecaptions.com/) - Browser-based word-by-word video captions with local Whisper transcription and MP4, SRT and VTT export.

## Meeting & Collaboration

Tools for transcribing meetings and collaborative work.

| Tool | Integration | Notes |
|------|------------|-------|
| [Otter.ai](https://otter.ai) | Zoom, Teams, Meet | Real-time meeting transcription |
| [Fireflies.ai](https://fireflies.ai) | Zoom, Teams, Meet, Webex | Meeting bot, AI notes, action items |
| [Grain](https://grain.com) | Zoom, Meet | Video highlight clips + transcription |
| [Fathom](https://fathom.video) | Zoom | Free meeting recorder and transcriber |
| [tl;dv](https://tldv.io) | Zoom, Meet | Meeting recordings with AI notes |
| [Krisp](https://krisp.ai) | Any app | Noise cancellation + meeting transcription |
| [MeetGeek](https://meetgeek.ai) | Zoom, Teams, Meet | Automated meeting notes |

## Podcast Transcription

Tools and services specifically for podcast transcription.

| Tool | Key Features |
|------|-------------|
| [Vocova](https://vocova.app) | Import from Spotify, Apple Podcasts, SoundCloud by URL; speaker labels; bilingual export |
| [Podcastle](https://podcastle.ai) | Recording + transcription + editing |
| [Castmagic](https://www.castmagic.io) | Transcription + AI-generated show notes, clips, social posts |
| [Podium](https://hello.podium.page) | Podcast to article conversion |
| [Podsqueeze](https://podsqueeze.com) | AI show notes, timestamps, blog posts from episodes |
| [Snipd](https://www.snipd.com) | AI-powered podcast highlights and transcripts |

## Medical & Legal Transcription

Specialized transcription for regulated industries.

| Tool | Industry | Compliance |
|------|----------|-----------|
| [Nuance DAX](https://www.nuance.com/healthcare/ambient-clinical-intelligence.html) | Healthcare | HIPAA |
| [DeepScribe](https://www.deepscribe.ai) | Healthcare | HIPAA |
| [Augnito](https://augnito.ai) | Healthcare | HIPAA, CE |
| [Athreon](https://athreon.com) | Legal | SOC 2 |
| [3Play Media](https://www.3playmedia.com) | Education, Legal | ADA, Section 508 |
| [Verbit](https://verbit.ai) | Legal, Education | SOC 2, HIPAA |

## Datasets

Datasets for training and evaluating speech recognition models.

| Dataset | Hours | Languages | Notes |
|---------|-------|-----------|-------|
| [LibriSpeech](https://www.openslr.org/12) | 1,000 | English | Derived from audiobooks, standard ASR benchmark |
| [Common Voice](https://commonvoice.mozilla.org) | 30,000+ | 100+ | Mozilla's crowdsourced, multilingual |
| [GigaSpeech](https://github.com/SpeechColab/GigaSpeech) | 10,000 | English | Audiobooks, podcasts, YouTube |
| [Multilingual LibriSpeech](https://www.openslr.org/94/) | 50,000+ | 8 | Multilingual audiobook dataset |
| [VoxPopuli](https://github.com/facebookresearch/voxpopuli) | 400,000+ | 23 | European Parliament recordings |
| [FLEURS](https://huggingface.co/datasets/google/fleurs) | 12 per lang | 102 | Few-shot evaluation benchmark |
| [Earnings-22](https://github.com/revdotcom/speech-datasets) | 119 | English | Earnings calls, challenging audio |
| [AMI Corpus](https://groups.inf.ed.ac.uk/ami/corpus/) | 100 | English | Meeting transcriptions with speaker labels |
| [SPGISpeech](https://datasets.kensho.com/datasets/spgispeech) | 5,000 | English | Financial transcriptions |
| [People's Speech](https://mlcommons.org/datasets/peoples-speech/) | 30,000 | English | Diverse accents and recording conditions |

## Benchmarks & Evaluation

Tools and metrics for evaluating transcription quality.

- [OpenASR Leaderboard](https://huggingface.co/spaces/hf-audio/open_asr_leaderboard) - Hugging Face ASR model comparison.
- [jiwer](https://github.com/jitsi/jiwer) - Python package for calculating WER, MER, WIL, and CER.
- [kaldialign](https://github.com/pzelasko/kaldialign) - Fast WER computation with alignment.
- [Whisper Normalizer](https://github.com/openai/whisper/blob/main/whisper/normalizers/) - Text normalization for fair WER comparison.
- [ESB Benchmark](https://huggingface.co/datasets/esb/datasets) - End-to-end Speech Benchmark for ASR evaluation.

## Research Papers

Foundational and recent papers in speech recognition.

- [Robust Speech Recognition via Large-Scale Weak Supervision](https://arxiv.org/abs/2212.04356) - Whisper (Radford et al., 2022)
- [Distil-Whisper: Robust Knowledge Distillation via Large-Scale Pseudo Labelling](https://arxiv.org/abs/2311.00430) - Gandhi et al., 2023
- [Scaling Speech Technology to 1,000+ Languages](https://arxiv.org/abs/2305.13516) - MMS (Pratap et al., 2023)
- [SeamlessM4T: Massively Multilingual & Multimodal Machine Translation](https://arxiv.org/abs/2308.11596) - Meta, 2023
- [wav2vec 2.0: A Framework for Self-Supervised Learning of Speech Representations](https://arxiv.org/abs/2006.11477) - Baevski et al., 2020
- [Conformer: Convolution-augmented Transformer for Speech Recognition](https://arxiv.org/abs/2005.08100) - Gulati et al., 2020
- [CTranslate2: Efficient Inference with Transformer Models](https://github.com/OpenNMT/CTranslate2) - OpenNMT
- [Whisper-AT: Noise-Robust Automatic Speech Recognizers are Also Strong Audio Event Taggers](https://arxiv.org/abs/2307.03183) - Gong et al., 2023

## Tutorials & Guides

- [OpenAI Whisper tutorial](https://platform.openai.com/docs/guides/speech-to-text) - Official guide for using Whisper API.
- [Fine-tuning Whisper with Hugging Face](https://huggingface.co/blog/fine-tune-whisper) - Step-by-step guide to fine-tuning Whisper for any language.
- [Building a real-time transcription app](https://www.assemblyai.com/docs/getting-started/transcribe-streaming-audio) - AssemblyAI streaming guide.
- [Deepgram getting started](https://developers.deepgram.com/docs/getting-started-with-pre-recorded-audio) - Transcribing pre-recorded audio with Deepgram.
- [Running Whisper locally](https://github.com/ggerganov/whisper.cpp#quick-start) - whisper.cpp quick start.
- [Speaker diarization with pyannote](https://github.com/pyannote/pyannote-audio#tldr) - pyannote.audio getting started.

## Community

- [r/speechrecognition](https://www.reddit.com/r/speechrecognition/) - Reddit community for speech recognition.
- [r/transcription](https://www.reddit.com/r/transcription/) - Reddit community for transcription professionals.
- [Hugging Face Audio Course](https://huggingface.co/learn/audio-course) - Free course covering ASR, TTS, and audio classification.
- [AssemblyAI Discord](https://discord.gg/assemblyai) - Community for developers using AssemblyAI.
- [Deepgram Community](https://community.deepgram.com) - Deepgram developer community.

---

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
