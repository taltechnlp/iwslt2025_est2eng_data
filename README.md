# Introduction

Training and dev data for [IWSLT 2025](https://iwslt.org/2025/) Estonian-English speech translation task.

# Downloading

Audio data is not included in the repository and has to be downloaded and unpacked separately:

    wget --continue --progress=dot:mega --tries=0 https://cs.taltech.ee/staff/tanel.alumae/data/iwslt2025_est2eng_data_audio.tar

    tar xvf iwslt2025_est2eng_data_audio.tar

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

