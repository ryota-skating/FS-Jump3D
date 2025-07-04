[![arXiv](https://img.shields.io/badge/arXiv-2408.16638-B31B1B.svg)](http://arxiv.org/abs/2408.16638)
[![ACMMM 2024](https://img.shields.io/badge/ACMMM2024-10.1145/3689061.3689077-blue)](https://doi.org/10.1145/3689061.3689077)

# FS-Jump3D Dataset

This is the official repository for `FS-Jump3D` dataset.

`FS-Jump3D` dataset is the first figure skating jump dataset that includes both 3D pose data and video data from 12 viewpoints. The jump data were captured using the markerless motion-capture system ([Theia3D](https://www.theiamarkerless.ca/), Theia) by positioning 12 high-speed cameras ([Miqus Video](https://www.qualisys.com/cameras/miqus-video/), Qualisys) on the ice skating rink.

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/ryota-takedalab/FS-Jump3D/blob/main/figs/Theia3D_sample.gif" alt="Theia3D sample" height="200"/>
  <img src="https://github.com/ryota-takedalab/FS-Jump3D/blob/main/figs/qtm_ex.gif" alt="QTM sample" height="200"/>
</div>

## News

- **2025-06-12** | FS-Jump3D dataset has been integrated into the [AthletePose3D](https://github.com/calvinyeungck/AthletePose3D) dataset, a larger multi-sport 3D pose dataset developed by our research team. The work was presented at CVSports 2025 @ CVPR!
- **2025-02-14** | We found some filename errors in the JSON data we provided. The issue has been fixed, and the corrected files are now available for download.
- **2024-10-01** | We are pleased to announce that our paper, "[3D Pose-Based Temporal Action Segmentation for Figure Skating: A Fine-Grained and Jump Procedure-Aware Annotation Approach](https://arxiv.org/abs/2408.16638)," has been accepted for presentation at the 7th ACM International Workshop on Multimedia Content Analysis in Sports (MMSports '24).

## Download

| Data | Size | Download (zip) | FILE_ID |
| :---: | :---: | :---: | :---: |
| c3d | 302.6 MB | [GoogleDrive](https://drive.google.com/drive/folders/1Ki9dxLuo78XFnCun9LGwWFlzO-A0FxJT?usp=drive_link) | `12VqZmw-XyKyWnmEAWnnk_ZEU_1KGTig1` |
| json | 505.2 MB | [GoogleDrive](https://drive.google.com/drive/folders/17gQJR-qzF_JTs8JZgwZc1wuRKvkwnwVj?usp=drive_link) | `1Kh4chravgcSb3RZQ3k_WwSfClND0bcUO` |
| videos | 8.84 GB | [GoogleDrive](https://drive.google.com/drive/folders/1yvZMmK4hvrvK5ykqzkr1d-yVmImz-NNJ?usp=sharing) | `1NgdlJKN2VGV4ngHDGnRXUcV2M9Qdt30C` <br> `1HrJxot6Sxg9trYZnxF6tsWYdFq0q5ub_` <br> `1Exu1Ul6eHCCH6YzZJa4XTy9XbVMcX9Jj` <br> `1YMAUlsH7vnNvg-iwiENch0KrIzWa4gO-` |

You can download the dataset using the `FILE_ID` with the following curl command.
```zsh
curl "https://drive.usercontent.google.com/download?id=FILE_ID&confirm=xxx" -o output_filename
```

## How to Use the Dataset

### Using C3D Files

You can open and visualize the original C3D files with QTM (Qualisys Track Manager) software. QTM also allows you to export the data in various formats. For more details, please visit the [Qualisys Track Manager page](https://www.qualisys.com/software/qualisys-track-manager/).

### Using JSON files

The JSON files contain the same data as the original C3D files. To convert JSON files into the common 3D pose format, place the downloaded JSON files in the `data/json` directory and run the following command:
```zsh
python utils/format.py
```

Our implementation uses the Human3.6M keypoint rig, as described in the [MMPose documentation](https://mmpose.readthedocs.io/en/latest/dataset_zoo/3d_body_keypoint.html), to format JSON files. If you want to use a different keypoint rig, add it to `utils/rig.json` and format the JSON files with the following command:
```zsh
python utils/format.py --rig YOUR_NEW_RIG
```

## Visualization

We provide a sample script for visualizing 3D poses stored in `.npy` files in `utils/visualization.ipynb`.

The figure below shows an example of the visualization results generated by this script.
Since the implementation uses [Plotly](https://plotly.com/python/), you can change the viewpoint interactively using your mouse cursor.

<img src="https://github.com/ryota-takedalab/FS-Jump3D/blob/main/figs/vis_sample.gif" height="300"/>

## License

`FS-Jump3D` Dataset is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Citation

```
@inproceedings{MMSports2024_tanaka,
author = {Tanaka, Ryota and Suzuki, Tomohiro and Fujii, Keisuke},
title = {3D Pose-Based Temporal Action Segmentation for Figure Skating: A Fine-Grained and Jump Procedure-Aware Annotation Approach},
year = {2024},
isbn = {9798400711985},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3689061.3689077},
doi = {10.1145/3689061.3689077},
booktitle = {Proceedings of the 7th ACM International Workshop on Multimedia Content Analysis in Sports},
pages = {17–26},
numpages = {10},
keywords = {annotation, computer vision, datasets, human pose estimation, sports, temporal action segmentation},
location = {Melbourne VIC, Australia},
series = {MMSports '24}
}
```

## Acknowledgments

We would like to express our gratitude to Chukyo University for facilitating access to high-level players and for providing their skating rink for our on-ice motion capture sessions. We also extend our thanks to Archive Tips, Inc. for their expertise and assistance with everything from arranging motion capture equipment to setting it up.
