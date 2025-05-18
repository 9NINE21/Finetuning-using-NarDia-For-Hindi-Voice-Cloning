# Hindi Voice Cloning using Open-Source TTS Models

This repository contains experiments and findings from building a Hindi TTS voice cloning pipeline using open-source models like Nari-DIA 1.6B, Coqui XTTS, and Microsoft SpeechT5. The work focuses on evaluating zero-shot capabilities, fine-tuning using Hindi datasets, and addressing limitations in Hindi synthesis.

---

## 🔍 Models Explored

### 1. Nari-DIA 1.6B 
Original Repo for this model : https://github.com/nari-labs/dia.git
## 💻 Hardware and Inference Speed

Dia has been tested on only GPUs (pytorch 2.0+, CUDA 12.6). CPU support is to be added soon.
The initial run will take longer as the Descript Audio Codec also needs to be downloaded.

- ✅ Tested Zero-shot Voice Cloning of Nari-Dia 1.6B using the Custom Voices 
  
## Results Summary : Audio at [results/zeroshot_outputs/]
## 🔊 Results Summary
| Model         | Type        | Hindi Quality | Notes                               | English Quality |
|---------------|-------------|---------------|-------------------------------------|-----------------|
| Nari-DIA      | Zero-shot   | ❌ Poor        | Lacks Hindi phoneme training       |    Good         |
| 

- ✅ Finetuning Attempted using:  
  - Dataset: `Rishavnine/SYSPIN_Hindi_Male_TTS_Small` HuggingFace Link : https://huggingface.co/datasets/Rishavnine/SYSPIN_Hindi_Male_TTS_Small
  - Platform: Kaggle (checkpoints saved)



