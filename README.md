# Introduction

Training and dev data for [IWSLT 2025](https://iwslt.org/2025/) Estonian-English speech translation task.

Training data contains 581647 utterances (1258 hours) and development set 1601 utterances (3.6 hours). Training data originates from the [TalTech Estonian Speech Dataset 1.0](https://cs.taltech.ee/staff/tanel.alumae/data/est-pub-asr-data/) which is a manually transcribed dataset of mostly broadcast data created for training ASR models. All the speech data consists of long-form
speech and has been manually transcribed and timealigned with speech at an utterance level. In the dataset provided here, the long-form recordings have been split up into utterances. The transcripts have been automatically translated to English using Google Translate. Development data contains data from government and municipal press conferences, TV news and TV talkshows and has been manually translated to English. Both original Estonian transcriptions as well as English translations are provided for all utterances.

# Data format

Annotation is given in tsv file, with the fields audio, Estonian, English. E.g.:
    
    $ head -5 train.tsv
    audio   Estonian        English
    tosine_mang_x211_normak_15042010/tosine_mang_x211_normak_15042010_0000_3.057_7.790.flac Ja nüüd läheme meie viimase ettekande juurde selles sessioonis. And now we go to our last presentation in this session.
    tosine_mang_x211_normak_15042010/tosine_mang_x211_normak_15042010_0001_7.790_13.010.flac        Kui esimene ettekanne rääkis sellest, et, et    If the first presentation talked about that, that
    tosine_mang_x211_normak_15042010/tosine_mang_x211_normak_15042010_0002_13.010_19.638.flac       milleks on vaja juhtida ja mis suunas on vaja juhtida, ja teine keskendus pigem sellele,
    et kuidas       what it is necessary to lead and in what direction it is necessary to lead, and the other focused more on how                                                           
    tosine_mang_x211_normak_15042010/tosine_mang_x211_normak_15042010_0003_19.638_22.655.flac       on võimalik üldse riiklikul tasandil neid protsesse juhtida, siis       is it possible to manage these processes at the national level, then

The field `audio` refers to an audio file in the audio subdirectory (which has to be downloaded). The field `Estonian` is the original Estonian transcription and `English` its translation.

# Downloading audio

Audio data is around 90 GB in size (16 kHz flac files) and is thus not included in the repository and has to be downloaded and unpacked separately:

    wget --continue --progress=dot:mega --tries=0 https://cs.taltech.ee/staff/tanel.alumae/data/iwslt2025_est2eng_data_audio.tar

    tar xvf iwslt2025_est2eng_data_audio.tar

This should create the "audio" subdirectory with a lot of subdirectories, which correspond to individual long recordings from which the utterances are taken.

# Citing

Data and some systems based on this data are described [this paper](https://aclanthology.org/2024.loresmt-1.17/).

    @inproceedings{sildam-etal-2024-finetuning,
        title = "Finetuning End-to-End Models for {E}stonian Conversational Spoken Language Translation",
        author = {Sildam, Tiia  and
          Velve, Andra  and
          Alum{\"a}e, Tanel},
        booktitle = "Proceedings of the Seventh Workshop on Technologies for Machine Translation of Low-Resource Languages (LoResMT 2024)",
        year = "2024",
        address = "Bangkok, Thailand",
        url = "https://aclanthology.org/2024.loresmt-1.17/",
        doi = "10.18653/v1/2024.loresmt-1.17",
        pages = "166--174"
    }

