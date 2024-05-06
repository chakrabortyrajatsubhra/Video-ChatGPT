# Video-ChatGPT :movie_camera: :speech_balloon:

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


## License :scroll:
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.


