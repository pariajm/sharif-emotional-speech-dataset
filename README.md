[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)](https://github.com/ellerbrock/open-source-badges/) 

# <a href='https://arxiv.org/pdf/1906.01155.pdf'>ShEMO: a large-scale validated database for Persian speech emotion detection</a><br>

## Abstract
<div align="justify"> This paper introduces a large-scale, validated database for Persian called Sharif Emotional Speech Database (ShEMO). The database includes 3000 semi-natural utterances, equivalent to 3 hours and 25 minutes of speech data extracted from online radio plays. The ShEMO covers speech samples of 87 native-Persian speakers for five basic emotions including <i>anger</i>, <i>fear</i>, <i>happiness</i>, <i>sadness</i> and <i>surprise</i>, as well as neutral state. Twelve annotators label the underlying emotional state of utterances and majority voting is used to decide on the final labels. According to the kappa measure, 
the inter-annotator agreement is 64% which is interpreted as "substantial agreement". We also present benchmark results based on common classification methods in speech emotion detection task. According to the experiments, support vector machine achieves the best results for both gender-independent (58.2%) and gender-dependent models (female=59.4%, male=57.6%). The ShEMO is available for academic purposes free of charge to provide a baseline for further research on Persian emotional speech.

## Download Dataset 
To download female utterances (zip file):
```bash
wget -O female.zip "https://www.dropbox.com/s/42okby6c40w3j2x/female.zip?dl=0"
```
 
To download male utterances (zip file):
```bash
wget -O male.zip "https://www.dropbox.com/s/5ebs8hq1zm0qkp6/male.zip?dl=0"
```

To download labels & transcripts (json file):
```bash
wget https://github.com/pariajm/sharif-emotional-speech-dataset/raw/master/shemo.json
```
 
## Models Trained or Fine-tuned on ShEMO
Credits to [Mehrdad Farahani](https://github.com/m3hrdadfi/soxan)
 - [Speech emotion detection in Persian (fa) using wav2vec 2.0](https://huggingface.co/m3hrdadfi/wav2vec2-xlsr-persian-speech-emotion-recognition)
 - [Speech emotion detection in Persian (fa) using HuBERT](https://huggingface.co/m3hrdadfi/hubert-base-persian-speech-emotion-recognition)
 - [Speech geneder detection in Persian (fa) using HuBERT](https://huggingface.co/m3hrdadfi/hubert-base-persian-speech-gender-recognition)
 - [Automatic speech recognition in Persian (fa) using XLSR-53](https://huggingface.co/m3hrdadfi/wav2vec2-large-xlsr-persian-shemo)
 
## Overview of ShEMO

 Feature                     | Status   
-------------                | ----------
**access**                   | open source
**language**                 | Persian (fa)
**modality**                 | speech
**duration**                 | 3 hours and 25 minutes
**#utterances**              | 3000
**#speakers**                | 87 (31 females, 56 males)
**#emotions**                | 5 basic emotions (anger, fear, happiness, sadness and surprise) and neutral state
**orthographic transcripts** | available
**phonetic transcripts**     | available

Read our paper on <a href='https://link.springer.com/article/10.1007/s10579-018-9427-x'>Springer</a> or [arxiv](https://arxiv.org/pdf/1906.01155.pdf)

## Description of Filenames
The characters used in the filenames and their corresponding meaning:
- **A**: angry
- **F**: female speaker (if used at the beginning of the label e.g.`F14A09`) or fearful (if used in the middle of the label e.g. `M02F01`)
- **H** : happy
- **M** : male speaker
- **N** : neutral
- **S** : sad
- **W** : surprised

e.g. `F03S02` **F** means the speaker is **female**, **03** denotes **the speaker code**, **S** refers to the underlying emotion of the utterance which is **sadness**, **02** means this is the **second utterance for this speaker in sad emotion**.

## Data Instances
Here is a sample of data instances:
```json
{
 "id": "F21N37", 
 "gender": "female", 
 "emotion": "neutral", 
 "transcript": "مگه من به تو نگفته بودم که باید راجع به دورانت سکوت کنی؟", 
 "ipa": "mӕge mæn be to nægofte budӕm ke bɑyæd rɑdʒeʔ be dorɑnt sokut koni"
 }
```
 
## دادگان گفتار احساسی شریف (شمو) 
برای دریافت مقاله <a href='https://arxiv.org/pdf/1906.01155.pdf'>اینجا</a> کلیک کنید

## Citation
If you use this dataset, please cite the following paper:
~~~~
@Article{MohamadNezami2019,
author  = {Mohamad Nezami, Omid and Jamshid Lou, Paria and Karami, Mansoureh},
title = {ShEMO: a large-scale validated database for Persian speech emotion detection},
journal = {Language Resources and Evaluation},
year  = {2019},
volume  = {53},
number  = {1},
pages = {1--16},
issn  = {1574-0218},
doi = {10.1007/s10579-018-9427-x},
url = {https://doi.org/10.1007/s10579-018-9427-x}
}
~~~~

### Contact
Paria Jamshid Lou <paria.jamshid-lou@hdr.mq.edu.au>
