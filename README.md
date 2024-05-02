---
language:
- ro
license: apache-2.0
base_model: openai/whisper-small
tags:
- generated_from_trainer
datasets:
- mozilla-foundation/common_voice_11_0
metrics:
- wer
model-index:
- name: Whisper Small Ro - IAzari
  results:
  - task:
      name: Automatic Speech Recognition
      type: automatic-speech-recognition
    dataset:
      name: Common Voice 11.0 Ro
      type: mozilla-foundation/common_voice_11_0
      config: ro
      split: None
      args: 'config: ro, split: test'
    metrics:
    - name: Wer
      type: wer
      value: 20.807789397764154
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# Whisper Small Ro - IAzari

Modelul dat este o ajustare a modelului [openai/whisper-small](https://huggingface.co/openai/whisper-small) cu datele Common Voice  11.0 Ro.
Rezultate:
- Pierderi: 0.2959
- (RCG) Rata Cuvintelor Greșite: 20.8078

## Descrierea

Este un model intenționat pentru transcrierea graiului Moldovenesc în text.


## Training procedure

### Hiperparametrii de antrenare

Hiperparametri utilizați la antrenare:
- learning_rate: 1e-05
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 200
- training_steps: 1000
- mixed_precision_training: Native AMP

### Rezultate de antrenare

| Pierderi în antrenare | Epoci | Pași | Pierderi în validare | RCG     |
|:---------------------:|:-----:|:----:|:--------------------:|:-------:|
| 0.0562                | 2.99  | 500  | 0.2754               | 21.7093 |
| 0.0056                | 5.99  | 1000 | 0.2959               | 20.8078 |


### Versiunile cadrului

- Transformers 4.39.3
- Pytorch 2.2.1+cu121
- Datasets 2.18.0
- Tokenizers 0.15.2
