### Download the data

You can download KLive through the following links:

- link: [Google Drive](https://drive.google.com/file/d/1z6YkQGpp7BnmyEq5xh-Ou7jVH8s5br5I/view?usp=sharing)


# Dataset Description
The file structure of the three datasets is listed as follows:

  ```
      ./
    |-- live_id2aid.txt
    |-- test
    |   |-- 0_test_score_infer_output.log
    |   |-- 1_test_score_infer_output.log
    |   |-- 2_test_score_infer_output.log
    |   |-- 3_test_score_infer_output.log
    |   |-- 4_test_score_infer_output.log
    |   |-- 5_test_score_infer_output.log
    |   |-- 6_test_score_infer_output.log
    |   `-- 7_test_score_infer_output.log
    `-- train
        |-- 0_test_score_infer_output.log
        |-- 1_test_score_infer_output.log
        |-- 2_test_score_infer_output.log
        |-- 3_test_score_infer_output.log
        |-- 4_test_score_infer_output.log
        |-- 5_test_score_infer_output.log
        |-- 6_test_score_infer_output.log
        `-- 7_test_score_infer_output.log
  ```
### Description of the fields in ```live_id2aid.txt```

There are only one file ```live_id2aid.txt``` which contains the mapping relationship between live id and author id.
| Field Name: | Description | Type | Example |
|:---:|:---:|:---:|:---:|
| live_id | The ID of the living room. | int64 | 17792 |
| author_id | The ID of the author. | int64 | 9932 |

### Description of the fields in ```xx_test_score_infer_output.log```

There are eight files ```xx_test_score_infer_output.log``` in train or test folder which contains the frame-level lvtr label and corresponding multi-modal feature.
| Field Name: | Description | Type | Example |
|:---:|:---:|:---:|:---:|
| live_id | The ID of the living room. | int64 | 17792 |
| timestamp | The timestamp of this interaction in seconds. | int64 | 685138930 |
| lvtr | A continuous feedback signal indicating the long-view rate of current streaming frame. | float64 | 0.83838385 |
| image_feaure | The image feature of current streaming frame. | float64 list | [-0.0198211669921875, 0.06585693359375,...] |
| text_feaure | The textual feature of current streaming frame. | float64 list | [-0.0638892874121666, 0.0496613085269928,...] |

## Citation
If you find our work useful, please cite it as follows:

```
@INPROCEEDINGS{10687664,
  author={Deng, Jiaxin and Wang, Shiyao and Shen, Dong and Zhao, Liqin and Yang, Fan and Zhou, Guorui and Meng, Gaofeng},
  booktitle={2024 IEEE International Conference on Multimedia and Expo (ICME)}, 
  title={A Multimodal Transformer for Live Streaming Highlight Prediction}, 
  year={2024},
  volume={},
  number={},
  pages={1-6},
  keywords={Visualization;Codes;Fuses;Annotations;Streaming media;Predictive models;Transformers;Multimodal Transformer;Modality Temporal Alignment;Border-aware Pairwise Loss;Live Streaming Highlight Prediction},
  doi={10.1109/ICME57554.2024.10687664}}
```