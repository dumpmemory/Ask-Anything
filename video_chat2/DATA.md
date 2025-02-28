# Instruction Data

[![Dataset meta](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-VideoChat2%20IT-blue)](https://huggingface.co/datasets/OpenGVLab/VideoChat2-IT) 

![images](./asset/data.png)

## Annotations
A comprehensive dataset of **2M** data annotations is available in [JSON](https://huggingface.co/datasets/OpenGVLab/VideoChat2-IT) format. Due to the extensive size of the full data, we provide only JSON files [here](https://huggingface.co/datasets/OpenGVLab/VideoChat2-IT). For corresponding images and videos, please follow our instructions.

## Source data

### Image
For image datasets, we utilized [M3IT](https://huggingface.co/datasets/MMInstruction/M3IT), filtering out lower-quality data by:
- **Correcting typos**: Most sentences with incorrect punctuation usage were rectified.
- **Rephrasing incorrect answers**: Some responses generated by ChatGPT, such as "Sorry, ...", were incorrect. These were rephrased using GPT-4.

You can easily download the datasets we employed from [M3IT](https://huggingface.co/datasets/MMInstruction/M3IT).

### Video
:warning: **For the used videos of InternVid, EgoQA and YouCook2, please check [issues](https://github.com/OpenGVLab/Ask-Anything/issues/86#issuecomment-1882529070).**

We treated video datasets differently. Please download the original videos from the provided links:
- [VideoChat](https://github.com/OpenGVLab/InternVideo/tree/main/Data/instruction_data): Based on [InternVid](https://github.com/OpenGVLab/InternVideo/tree/main/Data/InternVid), we created additional instruction data and used GPT-4 to condense the existing data.
- [VideoChatGPT](https://github.com/mbzuai-oryx/Video-ChatGPT/tree/main/data): The original caption data was converted into conversation data based on the same VideoIDs.
- [Kinetics-710](https://github.com/OpenGVLab/UniFormerV2/blob/main/DATASET.md) & [SthSthV2](https://developer.qualcomm.com/software/ai-datasets/something-something): Option candidates were generated from [UMT](https://github.com/OpenGVLab/unmasked_teacher) top-20 predictions.
- [NExTQA](https://github.com/doc-doc/NExT-QA): Typos in the original sentences were corrected.
- [CLEVRER](https://clevrer.csail.mit.edu/): For single-option multiple-choice QAs, we used only those concerning color/material/shape. For multi-option multiple-choice QAs, we utilized all the data.
- [WebVid](https://maxbain.com/webvid-dataset/): Non-overlapping data was selected for captioning and [QA](https://antoyang.github.io/just-ask.html#webvidvqa).
- [YouCook2](https://youcook2.eecs.umich.edu/): Original videos were truncated based on the official dense captions.
- [TextVR](https://github.com/callsys/textvr): All data was used without modifications.
- [TGIF](https://github.com/YunseokJANG/tgif-qa): Only TGIF$_{frame}$ and TGIF$_{Transition}$ subsets were considered.
- [EgoQA](https://ego4d-data.org/): Some egocentric QAs were generated from Ego4D data.

For all datasets, task instructions were automatically generated using GPT-4.

