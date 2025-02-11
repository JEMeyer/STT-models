# Model card for Western Highland Chatino STT

Jump to section:

- [Model details](#model-details)
- [Intended use](#intended-use)
- [Performance Factors](#performance-factors)
- [Metrics](#metrics)
- [Training data](#training-data)
- [Evaluation data](#evaluation-data)
- [Ethical considerations](#ethical-considerations)
- [Caveats and recommendations](#caveats-and-recommendations)

## Model details

- Person or organization developing model: Originally trained by [Bülent Özden](https://twitter.com/bulentozden), a leader of [Common Voice Türkçe](https://twitter.com/CVTurkce).
- Model language: Western Highland Chatino / `ctp`
- Model date: 12th April, 2022
- Model type: `Speech-to-Text`
- Model version: `v1.0.0`
- Compatible with  STT version: `v1.3.0`
- License: CC-BY-SA 4.0
- Where to send questions or comments about the model: You can leave an issue on [`STT-model` issues](https://github.com/coqui-ai/STT-models/issues), open a new discussion on [`STT-model` discussions](https://github.com/coqui-ai/STT-models/discussions), or chat with us on [Gitter](https://gitter.im/coqui-ai/).

## Intended use

Speech-to-Text for [Western Highland Chatino](https://en.wikipedia.org/wiki/https://en.wikipedia.org/wiki/Highland_Chatino) on 16kHz, mono-channel audio.

## Performance Factors

Factors relevant to Speech-to-Text performance include but are not limited to speaker demographics, recording quality, and background noise. Read more about STT performance factors [here](https://stt.readthedocs.io/en/latest/DEPLOYMENT.html#how-will-a-model-perform-on-my-data).

## Metrics

STT models are usually evaluated in terms of their transcription accuracy, deployment Real-Time Factor, and model size on disk.

#### Transcription Accuracy

|Test Corpus|WER|CER|
|-----------|---|---|
|GORILLA |77.2\%|30.9\%|

#### Model Size

`model.tflite`: 46M

### Approaches to uncertainty and variability

Confidence scores and multiple paths from the decoding beam can be used to measure model uncertainty and provide multiple, variable transcripts for any processed audio.

## Training data

This model was trained on [GORILLA `ctp`](https://gorilla.linguistlist.org/code/ctp/)

### Citation

* Malgorzata E. Cavar, Damir Cavar, Hilaria Cruz (2016) "Endangered Language Documentation: Bootstrapping a Chatino Speech Corpus, Forced Aligner, ASR". Pages 4004-4011 Of N. Calzolari (et al. eds) *Proceedings of the Tenth International Conference on Language Resources and Evaluation* (LREC 2016) in Portorož, Slovenia, European Language Resources Association (ELRA), Paris, France. 

## Evaluation data

This model was evaluated on [GORILLA `ctp`](https://gorilla.linguistlist.org/code/ctp/)

## Ethical considerations

Deploying a Speech-to-Text model into any production setting has ethical implications. You should consider these implications before use.

### Demographic Bias

You should assume every machine learning model has demographic bias unless proven otherwise. For STT models, it is often the case that transcription accuracy is better for men than it is for women. If you are using this model in production, you should acknowledge this as a potential issue.

### Surveillance

Speech-to-Text may be mis-used to invade the privacy of others by recording and mining information from private conversations. This kind of individual privacy is protected by law in may countries. You should not assume consent to record and analyse private speech.

## Caveats and recommendations

Machine learning models (like this STT model) perform best on data that is similar to the data on which they were trained. Read about what to expect from an STT model with regard to your data [here](https://stt.readthedocs.io/en/latest/DEPLOYMENT.html#how-will-a-model-perform-on-my-data). 

In most applications, it is recommended that you [train your own language model](https://stt.readthedocs.io/en/latest/LANGUAGE_MODEL.html) to improve transcription accuracy on your speech data.