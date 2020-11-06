# Russian Kaldi Profile

A [Rhasspy](https://github.com/rhasspy/rhasspy) profile for Italian (`ru`).

Includes:

* A [Kaldi nnet3](https://kaldi-asr.org/doc/dnn3.html) speech to text model
    * See files in `acoustic_model/`
    * Recipe created with [ipa2kaldi](https://github.com/rhasspy/ipa2kaldi)
    * Trained on:
        * [OpenSTT](https://github.com/snakers4/open_stt/)
            * `asr_public_phone_calls_2` (553 hours)
            * `public_youtube1120` (1,106 hours)
        * [Common Voice](https://commonvoice.mozilla.org) (105 hours)
        * [M-AILabs](https://www.caito.de/2019/01/the-m-ailabs-speech-dataset/) (46 hours)
        * [CSS10](https://www.kaggle.com/bryanpark/russian-single-speaker-speech-dataset) (21 hours)
        * [Voxforge](http://voxforge.org/ru) (24 hours)
* An [IPA](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet) pronunciation lexicon re-coded from [cmusphinx-ru-5.2](https://sourceforge.net/projects/cmusphinx/files/Acoustic%20and%20Language%20Models/Russian/)
    * See `base_dictionary.txt.gz`
* A [phonetisaurus](https://github.com/AdolfVonKleist/Phonetisaurus) grapheme to phoneme model for predicting word pronunciations
    * See `g2p.fst.gz`
    * Trained on `base_dictionary.txt.gz`
* A tri-gram [ARPA language model](https://cmusphinx.github.io/wiki/arpaformat/)
    * See `base_language_model.txt.gz`
    * Text from audio transcriptions, [Common Voice](https://github.com/mozilla/common-voice/tree/master/server/data/it), and [Universal Dependencies](https://universaldependencies.org/)
