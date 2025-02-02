# SLU recipes for Fluent Speech Commands
This folder contains recipes for spoken language understanding (SLU) with [Fluent Speech Commands](fluent.ai/research/fluent-speech-commands/).

### Tokenizer recipe
(You don't need to run this because the other recipes download a tokenizer, but you can run this if you want to train a new tokenizer for Fluent Speech Commands.)

Run this to train the tokenizer:

```
cd Tokenizer
python train.py hparams/tokenizer_bpe51.yaml
```

### Direct recipe
The "direct" recipe maps the input speech to directly to semantics using a seq2seq model.
The encoder is pre-trained using the LibriSpeech seq2seq recipe.

```
cd direct
python train.py hparams/train.yaml
```

# Results

| Release | hyperparams file | Test Acc | Model link | GPUs |
|:-------------:|:---------------------------:| -----:| -----:| --------:|
| 21-06-03 | train.yaml | 99.60% | https://www.dropbox.com/sh/wal9ap0go9f66qw/AADBVlGs_E2pEU4vYJgEe3Fba?dl=0 | 1xV100 32GB |


# PreTrained Model + Easy-Inference
You can find the pre-trained model with an easy-inference function on [HuggingFace](https://huggingface.co/speechbrain/slu-direct-fluent-speech-commands-librispeech-asr).


# Training Time
About 15 minutes for each epoch with a TESLA V100.


# **About SpeechBrain**
- Website: https://speechbrain.github.io/
- Code: https://github.com/speechbrain/speechbrain/
- HuggingFace: https://huggingface.co/speechbrain/


# **Citing SpeechBrain**
Please, cite SpeechBrain if you use it for your research or business.

```bibtex
@misc{ravanelli2024opensourceconversationalaispeechbrain,
      title={Open-Source Conversational AI with SpeechBrain 1.0},
      author={Mirco Ravanelli and Titouan Parcollet and Adel Moumen and Sylvain de Langen and Cem Subakan and Peter Plantinga and Yingzhi Wang and Pooneh Mousavi and Luca Della Libera and Artem Ploujnikov and Francesco Paissan and Davide Borra and Salah Zaiem and Zeyu Zhao and Shucong Zhang and Georgios Karakasidis and Sung-Lin Yeh and Pierre Champion and Aku Rouhe and Rudolf Braun and Florian Mai and Juan Zuluaga-Gomez and Seyed Mahed Mousavi and Andreas Nautsch and Xuechen Liu and Sangeet Sagar and Jarod Duret and Salima Mdhaffar and Gaelle Laperriere and Mickael Rouvier and Renato De Mori and Yannick Esteve},
      year={2024},
      eprint={2407.00463},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2407.00463},
}
@misc{speechbrain,
  title={{SpeechBrain}: A General-Purpose Speech Toolkit},
  author={Mirco Ravanelli and Titouan Parcollet and Peter Plantinga and Aku Rouhe and Samuele Cornell and Loren Lugosch and Cem Subakan and Nauman Dawalatabad and Abdelwahab Heba and Jianyuan Zhong and Ju-Chieh Chou and Sung-Lin Yeh and Szu-Wei Fu and Chien-Feng Liao and Elena Rastorgueva and François Grondin and William Aris and Hwidong Na and Yan Gao and Renato De Mori and Yoshua Bengio},
  year={2021},
  eprint={2106.04624},
  archivePrefix={arXiv},
  primaryClass={eess.AS},
  note={arXiv:2106.04624}
}
```

