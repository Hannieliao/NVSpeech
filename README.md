# Emilia-NV: A Non-Verbal Speech Dataset with Word-Level Annotation for Human-Like Speech Modeling

**[📄 Paper](https://arxiv.org/abs/2508.04195)** | **[🌐 Demos](https://nvspeech170k.github.io/)** | **[▶️ Demo Video](https://www.youtube.com/watch?v=lQpuwc8yRds)** | **[🤗 Dataset Access](https://huggingface.co/datasets/amphion/Emilia-NV)**

**Emilia-NV** introduces the first large-scale Mandarin corpus with fine-grained, word-level annotations of paralinguistic vocalizations—such as laughter, breathing, crying, and interjections like “uhm” and “oh”. Despite their importance for natural and expressive communication, these cues are rarely covered in existing resources, leaving them overlooked in ASR and TTS research. The corpus includes 48k human-annotated and 174k auto-labeled utterances (573hours).

Building on this foundation, **Emilia-NV** provides:
- 🗃️ A scalable annotation pipeline that enables large-scale automatic labeling of paralinguistic vocalizations.
- 🧠 Paralinguistic-aware ASR (NVASR) that jointly transcribes lexical content and non-verbal tokens.
- 🔊 Paralinguistic controllable TTS (CV2@Emilia-NV) that supports explicit, position-aware generation of paralinguistic vocalizations.

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

- **[2025-08-06]** 🎉 Initial release of Emilia-NV:
  - 📄 [arXiv preprint](https://arxiv.org/abs/2508.04195)
  - 🎧 [Demo page](https://nvspeech170k.github.io/)
  - 🤗 [Dataset](https://huggingface.co/datasets/amphion/Emilia-NV)

### 📅 Release Plan

* ✅ Auto-labeled Emilia-NV dataset (174k utterances)
* ✅ ASR and TTS inference demo with controllable NVV generation
* [ ] Paralinguistic-aware ASR model inference code
* [ ] Paralinguistic-aware ASR checkpoint (Mandarin and English)

---

## 📦 Dataset

### 📌 Emilia-NV

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

If you find Emilia-NV helpful, please cite:

```bibtex
@article{2025nvspeech,
  title     = {NVSpeech: An Integrated and Scalable Pipeline for Human-Like Speech Modeling with Paralinguistic Vocalizations},
  author    = {Huan Liao, Qinke Ni, Yuancheng Wang, Yiheng Lu, Haoyue Zhan, Pengyuan Xie, Qiang Zhang, Zhizheng Wu},
  journal   = {arXiv preprint arXiv:2508.04195},
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

