# Official ASF-YOLO
This is the source code for the paper "ASF-YOLO: A Novel YOLO Model with Attentional Scale Sequence Fusion for Cell Instance Segmentation" published on Image and Vision Computing (IMAVIS), of which I am the first author. The paper is available to download on [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0262885624001616) or [arXiv](https://arxiv.org/abs/2312.06458).

## Model
The model configuration (i.e., network construction) file is asf-yolo.yaml in the directory [./models/segment](https://github.com/mkang315/ASF-YOLO/blob/main/models/segment).

#### Training

The hyperparameter setting file is hyp.scratch-low.yaml in the directory [./data/hyps/](https://github.com/mkang315/ASF-YOLO/blob/main/data/hyps).

##### Installation
Install requirements.txt in a Python>=3.8.0 environment, including PyTorch>=1.8.
```
pip install -r requirements.txt  # install
```

##### Training CLI
```
python segment/train.py
```

#### Testing CLI

```
python segment/predict.py
```

## Evaluation
We trained and evaluated ASF-YOLO on the two [datasets](https://github.com/mkang315/ASF-YOLO/tree/main/datasets): the [2018 Data Science Bowl (DSB2018)](https://kaggle.com/competitions/data-science-bowl-2018) from Kaggle and the [Breast Cancer Cell (BCC) dataset](https://bioimage.ucsb.edu/research/bio-segmentation) from the Center for Bio-Image Informatics, University of California, Santa Barbara (UCSB CBI). The [yolov5l-seg.pt](https://github.com/mkang315/ASF-YOLO/blob/main/yolov5l-seg.pt) is the initial weight of the pretrained MS COCO dataset by [YOLOv5l](https://github.com/ultralytics/yolov5) and isn't the ASF-YOLO training weight on the evaluation datasets, which has been stated in the paper.

## Suggested Citation
Please cite our paper if you use code from this repository:
> Plain Text

- Elsevier Reference Style</br>
M. Kang, C.-M. Ting, F.F. Ting, R.C.-W. Phan, ASF-YOLO: a novel YOLO model with attentional scale sequence fusion for cell instance segmentation, Image Vis. Comput. 147 (2024) 105057.</br>

- IEEE Reference Style</br>
M. Kang, C.-M. Ting, F. F. Ting, and R. C.-W. Phan, "Asf-yolo: A novel yolo model with attentional scale sequence fusion for cell instance segmentation," *Image Vis. Comput.*, vol. 147, 105057, Jul. 2024.</br>

- Nature Reference Style</br>
Kang, M., Ting, C.-M., Ting, F. F. & Phan, R. C.-W. ASF-YOLO: a novel YOLO model with attentional scale sequence fusion for cell instance segmentation. *Image Vis. Comput.* **147** 105057 (2024).</br>

- Springer Reference Style</br>
Kang, M., Ting, C.-M., Ting, F.F., Phan, R.C.-W.: ASF-YOLO: a novel YOLO model with attentional scale sequence fusion for cell instance segmentation. Image Vis. Comput. **147**, 105057 (2024)</br>

> BibTeX Format</br>
```
\begin{thebibliography}{1}
\bibitem{1} M. Kang, C.-M. Ting, F.F. Ting, R.C.-W. Phan, ASF-YOLO: a novel YOLO model with attentional scale sequence fusion for cell instance segmentation, Image Vis. Comput. 147 (2024) 105057.
\end{thebibliography}
```
```
@article{Kang24Asfyolo,
  author = "Ming Kang and Chee-Ming Ting and Fung Fung Ting and Rapha{\"e}l C.-W. Phan",
  title = "ASF-YOLO: A novel yolo model with attentional scale sequence fusion for cell instance segmentation",
  journal = "Image Vis. Comput.",
  volume = "147",
  note = "p. 105057",
  month = "Jul.",
  year = "2024",
}
```
```
@article{Kang24Asfyolo,
  author = "Kang, Ming and Ting, Chee-Ming and Ting, Fung Fung and Phan, Rapha{\"e}l C.-W.",
  title = "ASF-YOLO: a novel YOLO model with attentional scale sequence fusion for cell instance segmentation",
  journal = "Image Vis. Comput.",
  volume = "147",
  pages = "105057",
  publisher = "Elsevier",
  address = "Amsterdam",
  year = "2024",
  doi= "10.1016/j.imavis.2024.105057",
  url = "https://doi.org/10.1016/j.imavis.2024.105057"
}
```
<sup>**NOTE:** Please remove some optional *BibTeX* fields, for example, `series`, `volume`, `address`, `url` and so on, while the *LaTeX* compiler produces an error. Author names may be manually modified if not automatically abbreviated by the compiler under the control of the .bst file if applicable which defines bibliography/reference style. `Kang24Asfyolo` could be `b1`, `bib1`, or `ref1` when references appear in numbered style in which they are cited. The quotation mark pair `""` in the field could be replaced by the brace `{}`. </sup>

## License
ASF-YOLO is released under the GNU Affero General Public License v3.0 (AGPL-3.0). Please see the [LICENSE](https://github.com/mkang315/ASF-YOLO/blob/main/LICENSE) file for more information.

## Copyright Notice
Many utility codes of our project base on the codes of [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5), [EIoU](https://github.com/arojsubedi/Focal-EIoU) and [Soft-NMS](https://github.com/bharatsingh430/soft-nms) repositories.
