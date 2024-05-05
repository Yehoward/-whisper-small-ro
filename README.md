---
language:
- ro
license: apache-2.0
base_model: openai/whisper-small
tags:
- generated_from_trainer
datasets:
- Yehoward/iazar-date
metrics:
- wer
model-index:
- name: Whisper Small Ro - Iazar
  results:
  - task:
      name: Automatic Speech Recognition
      type: automatic-speech-recognition
    dataset:
      name: "Date audio colectate \xEEn cadrul proiectului TekWil"
      type: Yehoward/iazar-date
      args: 'split: test'
    metrics:
    - name: Wer
      type: wer
      value: 46.265060240963855
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# Whisper Small Ro - Iazar

This model is a fine-tuned version of [openai/whisper-small](https://huggingface.co/openai/whisper-small) on the Date audio colectate în cadrul proiectului TekWil dataset.
It achieves the following results on the evaluation set:
- Loss: 0.8207
- Wer: 46.2651

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 1e-05
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 50
- training_steps: 200
- mixed_precision_training: Native AMP

### Training results

| Training Loss | Epoch   | Step | Validation Loss | Wer     |
|:-------------:|:-------:|:----:|:---------------:|:-------:|
| 0.0005        | 66.6667 | 200  | 0.8207          | 46.2651 |


### Framework versions

- Transformers 4.40.1
- Pytorch 2.2.1+cu121
- Datasets 2.19.0
- Tokenizers 0.19.1
