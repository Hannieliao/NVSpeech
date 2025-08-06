# NVSpeech: An Integrated and Scalable Pipeline for Human-Like Speech Modeling with Paralinguistic Vocalizations

**[📄 Paper](https://arxiv.org/abs/xxxx.xxxxx)** | **[🌐 Demos](https://nvspeech170k.github.io/)** | **[🤗 Dataset Access](https://huggingface.co/datasets/Hannie0813/NVSpeech170k)**

**NVSpeech** is the **first large-scale, open-source pipeline** that jointly recognizes and synthesizes **paralinguistic vocalizations** — such as *laughter*, *breathing*, *crying*, and expressive interjections like *"uhm"* and *"oh"* — which are often overlooked in conventional ASR and TTS systems.

Unlike prior pipelines that focus purely on lexical content, **NVSpeech** models *how* people speak, not just *what* they say. It unifies:
- 🗃️ Dataset construction with rich annotations
- 🧠 ASR with inline decoding of non-verbal cues
- 🔊 TTS with fine-grained, position-aware vocalization control

This enables expressive, human-like speech modeling at both recognition and synthesis levels.


## ✨ Highlights

- 🧑‍🏫 **18 fine-grained paralinguistic categories**, including NVVs and lexicalized interjections  
- 🎧 **48,430 manually labeled** utterances & **174,179 auto-labeled** utterances (~573 hours)  
- 🗣️ **Paralinguistic-aware ASR**: Inline decoding like `You're so funny [Laughter]`  
- 🔊 **Controllable TTS**: Insert cues at arbitrary positions with natural rendering  
- 💡 Open-source pipeline for paralinguistic-aware ASR and controllable speech synthesis
- 🌏 **Mandarin-first design**, with demonstrated **cross-lingual applicability** to English

---

## 📊 Pipeline Overview

![NVSpeech Pipeline](https://github.com/NVSpeech170k/nvspeech170k.github.io/blob/main/asr-pipeline.png)

---

## 🗞 News

- **[2025-08-06]** 🎉 Initial release of NVSpeech:
  - 📄 [arXiv preprint](https://arxiv.org/abs/XXXX.XXXXX)
  - 🎧 [Demo page](https://nvspeech170k.github.io/)
  - 🤗 [Dataset](https://huggingface.co/datasets/Hannie0813/NVSpeech170k)

### 📅 Release Plan

* ✅ Auto-labeled NVSpeech170k dataset (174k utterances)
* ✅ ASR and TTS inference demo with controllable NVV generation
* [ ] Paralinguistic-aware ASR model inference code
* [ ] Paralinguistic-aware ASR checkpoint (Mandarin and English)

---

## 📦 Dataset

### 📌 NVSpeech170k

* 174,179 auto-labeled utterances
* 573 total hours
  ➡️ Automatically labeled using our ASR model.

### 🏷️ Paralinguistic Tag Categories

<details>
<summary><strong>📋 Click to expand: 18 fine-grained paralinguistic tags</strong></summary>

<br>

| Category              | Description                                                |
| --------------------- | ---------------------------------------------------------- |
| `Breathing`           | Audible inhalation or exhalation (e.g., sigh, deep breath) |
| `Crying`              | Soft or loud weeping sounds                                |
| `Laughter`            | Laughter of varying intensity                              |
| `Cough`               | Single or repetitive coughing sounds                       |
| `Sigh`                | Audible exhale expressing fatigue, sadness, or relief      |
| `Uhm`                 | A brief, voiced hesitation marker           |
| `Shh`                 | Hushing sound indicating quiet                             |
| `Dissatisfaction-hnn` | Low-pitched hum expressing discontent                      |
| `Surprise-ah`         | Sharp exclamation expressing surprise (`ah`)               |
| `Surprise-oh`         | Surprised tone using "oh"                                  |
| `Surprise-yo`         | Casual surprise tone using "yo"                            |
| `Surprise-wa`         | Exclamation tone using "wa"                                |
| `Question-ah`         | Questioning tone on "ah"                                   |
| `Question-oh`         | Inquisitive "oh" tone                                      |
| `Question-ei`         | Interrogative tone using "ei"                              |
| `Question-yi`         | Rising "yi" used in questions                              |
| `Question-en`         | Questioning "en" often in casual speech                    |
| `Confirmation-en`     | Affirmative tone using "en" (like "mm-hmm" in English)     |

</details>

---

## 🔤 Paralinguistic-Aware ASR

This ASR model decodes inline paralinguistic cues as textual tokens:

```text
Input:  [Audio clip]
Output: "I don't know (Uhm) maybe (Sigh) we should wait."
```

---

## 🔊 Controllable TTS

Our controllable TTS module enables **context-aware insertion** of paralinguistic vocalizations at **arbitrary token positions**, producing **natural and expressive speech**.

```text
Input Text:   "I don't know (Uhm) maybe (Sigh) we should wait."
Output Audio: [Synthesized speech with aligned non-verbal expressions]
```
---

## 📜 Citation

If you find NVSpeech helpful, please cite:

```bibtex
@article{2025nvspeech,
  title     = {NVSpeech: An Integrated and Scalable Pipeline for Human-Like Speech Modeling with Paralinguistic Vocalizations},
  author    = {Name and Collaborators},
  journal   = {arXiv preprint arXiv:XXXX.XXXXX},
  year      = {2025}
}
```

---

## 🙏 Acknowledgement

Our codebase is built upon the awesome [PANNs](https://github.com/qiuqiangkong/audioset_tagging_cnn), [Sensevoice](https://github.com/FunAudioLLM/SenseVoice), [Qwen-Audio](https://github.com/QwenLM/Qwen-Audio), [CosyVoice](https://github.com/FunAudioLLM/CosyVoice), [Whisper](https://github.com/openai/whisper) and [Paraformer](https://github.com/modelscope/FunASR/wiki/paraformer) repositories.  

---

## 📬 Contact

For questions, please open an [issue](https://github.com/Hannieliao/NVSpeech/issues)
---

## 🪪 License

This repository is licensed under **CC BY-NC-SA 4.0**.

