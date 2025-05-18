# Hindi Voice Cloning using Open-Source TTS Models

This repository contains experiments and findings from building a Hindi TTS voice cloning pipeline using open-source models like Nari-DIA 1.6B, Coqui XTTS, and Microsoft SpeechT5. The work focuses on evaluating zero-shot capabilities, fine-tuning using Hindi datasets, and addressing limitations in Hindi synthesis.

---

## 🔍 Models Explored

### 1. Nari-DIA 1.6B 
Original Repo for this model : https://github.com/nari-labs/dia.git
 ✅ Tested Zero-shot Voice Cloning of Nari-Dia 1.6B using the Custom Voices   
# Audio at [results/zeroshot_outputs/]
## 🔊 Results Summary
| Model         | Type        | Hindi Quality | Notes                               | English Quality  |
|---------------|-------------|---------------|-------------------------------------|-----------------|
| Nari-DIA      | Zero-shot   | ❌ Poor        | Lacks Hindi phoneme training       |    Good         |
 

## ✅ Finetuning Attempted using:  
  - Finetune Refrence Repo : https://github.com/stlohrey/dia-finetuning.git
  - Dataset: `Rishavnine/SYSPIN_Hindi_Male_TTS_Small` HuggingFace Link : https://huggingface.co/datasets/Rishavnine/SYSPIN_Hindi_Male_TTS_Small
  - Platform: Kaggle 
  - Finetuning Scripts at The Finetuning
  - Checkpoints at results/finetuining-checkpoints
    
## 🔊 Results Summary

| Model         | Type        | Results       | Notes                                 |
|---------------|-------------|---------------|-------------------------------------- |
| Nari-DIA      | Finetuned   | ❓ Unknown     | Checkpoint corrupted during transfer |


Gradio url not Supported by the Kaggle So checkpoint transfer to the Colab Corrupted not working properly 


### 2. Coqui XTTS
- Original Repo for this model : https://github.com/coqui-ai/TTS.git
- Documentation information with Finetuning https://docs.coqui.ai/en/latest/models/xtts.html
- Colab link models-CoquiXTTS
  ## 🔊 Results Summary
- ✅ Tried running fine-tuning Colab.
- ❌ Colab Broken (Dependency issues unstable Broken Resources Everywhere)
- Not usable locally due to hardware limitations (24GB VRAM).

### 3. Microsoft SpeechT5  Results at results/Microsoft SpeechT5 results 
- ✅ Trained on Datasets : https://huggingface.co/datasets/SayantanJoker/SYSPIN_Hindi_Male_TTS
- ✅ Added support for Devanagari tokenizer manually 
- 🔁 Training: 1300 steps run.
- Colab link at models Microsoft SpeechT5
 ## 🔊 Results Summary  
| Model                 | Type        | Results       | Notes                                                     |
|-----------------------|-------------|---------------|---------------------------------------------------------- |
| Microsoft SpeechTS    | Finetuned   |  ❌ Poor     |  Custom tokenizer, weak output                             |




## Instead of adding the Custom Tokenizer added the Romanized Scripts (Colab link at the Models Microsoft SpeechT5)

## 🔊 Results Summary  
| Model                 | Type        | Results       | Notes                                                     |
|-----------------------|-------------|---------------|---------------------------------------------------------- |
| Microsoft SpeechTS    | Finetuned   |  ❓ Unknown     |  Romanized Support for the Token                        |
-Trained on the Same Hindi Datasets 
-Colab Link at models Microsoft SpeechT5

## 🔊 Results Summary  
## Using the Nepali Model as Checkpoints instead of Microsoft.SpeechT5 model as Checkpoints 
## 🔊 Results Summary  
| Model                 | Type        | Results       | Notes                                                     |
|-----------------------|-------------|---------------|---------------------------------------------------------- |
| Microsoft SpeechTS    | Finetuned   |  ❓ Unknown     | Nepali Checkpoints                                      |

Colab Link at models Microsoft SpeechT5



## 📁 Project Structure
- `models/`: Scripts + notes for each model used
- `scripts/`: Code for training & inference
- `Results/`: Audio samples of each model 
- `Checkpoints/`: Checkpoints or Every-Save of the Run model.
- `data/`: Hindi dataset Used for the Finetuning






 



