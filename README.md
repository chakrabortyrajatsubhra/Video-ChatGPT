# Oryx Video-ChatGPT :movie_camera: :speech_balloon:

<p align="center">
    <img src="https://i.imgur.com/waxVImv.png" alt="Oryx Video-ChatGPT">
</p>

### Video-ChatGPT: Towards Detailed Video Understanding via Large Vision and Language Models



## Installation :wrench:

We recommend setting up a conda environment for the project:
```shell
conda create --name=video_chatgpt python=3.10
conda activate video_chatgpt

git clone https://github.com/mbzuai-oryx/Video-ChatGPT.git
cd Video-ChatGPT
pip install -r requirements.txt

export PYTHONPATH="./:$PYTHONPATH"
```
Additionally, install [FlashAttention](https://github.com/HazyResearch/flash-attention) for training,
```shell
pip install ninja

git clone https://github.com/HazyResearch/flash-attention.git
cd flash-attention
git checkout v1.0.7
python setup.py install
```

---

## Running Demo Offline :cd:

To run the demo offline, please refer to the instructions in [offline_demo.md](docs/offline_demo.md).

---

## Training :train:

For training instructions, check out [train_video_chatgpt.md](docs/train_video_chatgpt.md).

---

## Video Instruction Dataset :open_file_folder:

We are releasing our 100,000 high-quality video instruction dataset that was used for training our Video-ChatGPT model. You can download the dataset from 
[here](https://mbzuaiac-my.sharepoint.com/:u:/g/personal/hanoona_bangalath_mbzuai_ac_ae/EWxYslvDeX1PijKWM_WxTkkBDXDDD350YnUQOkbcL8V7Xg?e=Lq9itD). 
More details on our human-assisted and semi-automatic annotation framework for generating the data are available at [VideoInstructionDataset.md](data/README.md).

---

## Quantitative Evaluation :bar_chart:
Our paper introduces a new Quantitative Evaluation Framework for Video-based Conversational Models. To explore our benchmarks and understand the framework in greater detail, 
please visit our dedicated website: [https://mbzuai-oryx.github.io/Video-ChatGPT](https://mbzuai-oryx.github.io/Video-ChatGPT).

For detailed instructions on performing quantitative evaluation, please refer to [QuantitativeEvaluation.md](quantitative_evaluation/README.md).

**Video-based Generative Performance Benchmarking**  and **Zero-Shot Question-Answer Evaluation** tables are provided for a detailed performance overview. 

### Zero-Shot Question-Answer Evaluation

| **Model** | **MSVD-QA** |  | **MSRVTT-QA** |  | **TGIF-QA** |  | **Activity Net-QA** |  |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| | **Accuracy** | **Score** | **Accuracy** | **Score** | **Accuracy** | **Score** | **Accuracy** | **Score** |
| FrozenBiLM | 32.2 | -- | 16.8 | -- | 41.0 | -- | 24.7 | -- |
| Video Chat | 56.3 | 2.8 | 45.0 | 2.5 | 34.4 | 2.3 | 26.5 | 2.2 |
| LLaMA Adapter | 54.9 | 3.1 | 43.8 | 2.7 | - | - | 34.2 | 2.7 |
| Video LLaMA | 51.6 | 2.5 | 29.6 | 1.8 | - | - | 12.4 | 1.1 |
| Video-ChatGPT | **64.9** | **3.3** | **49.3** | **2.8** | **51.4** | **3.0** | **35.2** | **2.7** |


---

### Video-based Generative Performance Benchmarking

| **Evaluation Aspect** | **Video Chat** | **LLaMA Adapter** | **Video LLaMA** | **Video-ChatGPT** |
| --- |:--------------:|:-----------------:|:--------------:|:-----------------:|
| Correctness of Information |      2.23      |       2.03        |      1.96      |       **2.40**        |
| Detail Orientation |      2.50      |       2.32        |      2.18      |       **2.52**        |
| Contextual Understanding |      2.53      |       2.30        |      2.16      |       **2.62**        |
| Temporal Understanding |      1.94      |       **1.98**        |      1.82      |       **1.98**        |
| Consistency |      2.24      |       2.15        |      1.79      |       **2.37**        |

---

## Qualitative Analysis :mag:
A Comprehensive Evaluation of Video-ChatGPT's Performance across Multiple Tasks.

### Video Reasoning Tasks :movie_camera:
![sample1](docs/demo_samples/video_reasoning-min.png)

---
### Creative and Generative Tasks :paintbrush:
![sample5](docs/demo_samples/creative_and_generative-min.png)

---
### Spatial Understanding :globe_with_meridians:
![sample8](docs/demo_samples/spatial_understanding-min.png)

---
### Video Understanding and Conversational Tasks :speech_balloon:
![sample10](docs/demo_samples/video_understanding_and_conversation-min.png)

---
### Action Recognition :runner:
![sample22](docs/demo_samples/action_recognition-min.png)

---
### Question Answering Tasks :question:
![sample14](docs/demo_samples/question_answering-min.png)

---
### Temporal Understanding :hourglass_flowing_sand:
![sample18](docs/demo_samples/temporal_understanding-min.png)

---

## Acknowledgements :pray:

+ [LLaMA](https://github.com/facebookresearch/llama): A great attempt towards open and efficient LLMs!
+ [Vicuna](https://github.com/lm-sys/FastChat): Has the amazing language capabilities!
+ [LLaVA](https://github.com/haotian-liu/LLaVA): our architecture is inspired from LLaVA.
+ Thanks to our colleagues at MBZUAI for their essential contribution to the video annotation task, 
including Salman Khan, Fahad Khan, Abdelrahman Shaker, Shahina Kunhimon, Muhammad Uzair, Sanoojan Baliah, Malitha Gunawardhana, Akhtar Munir, 
Vishal Thengane, Vignagajan Vigneswaran, Jiale Cao, Nian Liu, Muhammad Ali, Gayal Kurrupu, Roba Al Majzoub, 
Jameel Hassan, Hanan Ghani, Muzammal Naseer, Akshay Dudhane, Jean Lahoud, Awais Rauf, Sahal Shaji, Bokang Jia,
without which this project would not be possible.

If you're using Video-ChatGPT in your research or applications, please cite using this BibTeX:
```bibtex
    @article{Maaz2023VideoChatGPT,
        title={Video-ChatGPT: Towards Detailed Video Understanding via Large Vision and Language Models},
        author={Muhammad Maaz, Hanoona Rasheed, Salman Khan and Fahad Khan},
        journal={ArXiv 2306.05424},
        year={2023}
    }
```

## License :scroll:
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.


Looking forward to your feedback, contributions, and stars! :star2:
Please raise any issues or questions [here](https://github.com/mbzuai-oryx/Video-ChatGPT/issues). 


---
[<img src="docs/images/IVAL_logo.png" width="200" height="100">](https://www.ival-mbzuai.com)
[<img src="docs/images/Oryx_logo.png" width="100" height="100">](https://github.com/mbzuai-oryx)
[<img src="docs/images/MBZUAI_logo.png" width="360" height="85">](https://mbzuai.ac.ae)
