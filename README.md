# DisfluencySpeech
Resources for DisfluencySpeech.

The DisfluencySpeech Dataset is a single-speaker studio-quality labeled English speech dataset with paralanguage. A single speaker recreates nearly 10 hours of expressive utterances from the Switchboard-1 Telephone Speech Corpus (Switchboard), simulating realistic informal conversations. To aid the development of a text-to-speech (TTS) model that is able to predictively synthesise paralanguage from text without such components, we provide three different transcripts at different levels of information removal (removal of non-speech events, removal of non-sentence elements, and removal of false starts).

Read the paper [here](https://arxiv.org/abs/2406.08820).

Dataset can be found [here](https://huggingface.co/datasets/amaai-lab/DisfluencySpeech).

Benchmark models for the three transcripts can be found here: [transcript A](https://huggingface.co/amaai-lab/DisfluencySpeech_BenchmarkA), [transcript B](https://huggingface.co/amaai-lab/DisfluencySpeech_BenchmarkB), [transcript C](https://huggingface.co/amaai-lab/DisfluencySpeech_BenchmarkC).

# Dataset Details

All audio files are provided as 22,050 hz _.wav_ files. In the _metadata.csv_ file, 4 different transcripts for each file are provided, 
each at differing levels of information removal:

- _transcript_annotated_ is a full transcript retaining all non-speech event and disfluency annotations;
- _transcript_a_ contains all textual content recorded, including non-sentence elements and restarts.
- Only non-speech events such as laughter and sighs are removed from transcript;
- _transcript_b_ is _transcript_a_ but with filled pauses, explicit editing terms, and discourse markers removed.
- Coordinating conjunctions and asides are left in, as they are non-sentence elements as well, they are often used to convey meaning; and
- _transcript_c_ is _transcript_b_ but with false starts removed. This is the most minimal transcript.

The training set contains 90% of the data, the validation set contains 5% of the data, and the test set contains 5% of the data.

# Citation
If you use this dataset, please cite the paper in which it is presented:

```
@misc{wang2024disfluencyspeechsinglespeakerconversational,
      title={DisfluencySpeech -- Single-Speaker Conversational Speech Dataset with Paralanguage}, 
      author={Kyra Wang and Dorien Herremans},
      year={2024},
      eprint={2406.08820},
      archivePrefix={arXiv},
      primaryClass={eess.AS},
      url={https://arxiv.org/abs/2406.08820}, 
}
```
