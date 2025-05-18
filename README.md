# Hindi Voice Cloning using Open-Source TTS Models

This repository contains experiments and findings from building a Hindi TTS voice cloning pipeline using open-source models like Nari-DIA 1.6B, Coqui XTTS, and Microsoft SpeechT5. The work focuses on evaluating zero-shot capabilities, fine-tuning using Hindi datasets, and addressing limitations in Hindi synthesis.

---

## 🔍 Models Explored

### 1. Nari-DIA 1.6B 
Original Repo for this model : https://github.com/nari-labs/dia.git
## 💻 Hardware and Inference Speed

Dia has been tested on only GPUs (pytorch 2.0+, CUDA 12.6). CPU support is to be added soon.
The initial run will take longer as the Descript Audio Codec also needs to be downloaded.

These are the speed we benchmarked in RTX 4090.

| precision | realtime factor w/ compile | realtime factor w/o compile | VRAM |
|:-:|:-:|:-:|:-:|
| `bfloat16` | x2.1 | x1.5 | ~10GB |
| `float16` | x2.2 | x1.3 | ~10GB |
| `float32` | x1 | x0.9 | ~13GB |

We will be adding a quantized version in the future.


- ✅ Tested Zero-shot in Hugging Face Space in Hindi synthesis
- English Voice Cloining by the Refrence Audio and Hindi Voice Cloning  using the Refrence Audio  Results at : [results/zeroshot_outputs/]
## Results Analysis 
-English Good
-Hindi Bad (Reson : Model is not trained in Hindi Language , providing the Romanized Scripts also  dont do the give Proper Results 

- ✅ Finetuning Attempted using:  
  - Dataset: `Rishavnine/SYSPIN_Hindi_Male_TTS_Small` HuggingFace Link : https://huggingface.co/datasets/Rishavnine/SYSPIN_Hindi_Male_TTS_Small
  - Platform: Kaggle (checkpoints saved)



