# FS-Jump3D Dataset

This is the official repository for `FS-Jump3D` dataset.

`FS-Jump3D` dataset is the first figure skating jump dataset that includes both 3D pose data and video data from 12 viewpoints. The jump data were captured using the markerless motion-capture system (Theia3D, Theia) by positioning 12 high-speed cameras (Miqus Video, Qualisys) on the ice skating rink.

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/ryota-takedalab/FS-Jump3D/blob/main/figs/Theia3D_sample.gif" alt="Theia3D sample" height="200"/>
  <img src="https://github.com/ryota-takedalab/FS-Jump3D/blob/main/figs/qtm_ex.gif" alt="QTM sample" height="200"/>
</div>

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

We will add this section soon.

## License

`FS-Jump3D` Dataset is licensed under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Acknowledgments

We would like to express our gratitude to Chukyo University for facilitating access to high-level players and for providing their skating rink for our on-ice motion capture sessions. We also extend our thanks to Archive Tips, Inc. for their expertise and assistance with everything from arranging motion capture equipment to setting it up.
