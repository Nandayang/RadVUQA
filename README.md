# RadVUQA-Radiological Visual Understanding and Question Answering Dataset
This is the official site of the study "Beyond the Hype: A dispassionate look at vision-language models in medical scenario"

**[Read the paper](https://arxiv.org/abs/2408.08704)**

RadVUQA is a large-scale dataset for developing and evaluating vision–language models in medical imaging. It includes CT and MRI scans, segmentation masks, anatomical bounding boxes, and paired question–answer (QA) annotations.

---

## 📦 Dataset Download

Download the full dataset (ZIP, ~6 GB) from Google Drive:

- [RadVUQA Dataset on Google Drive](https://drive.google.com/file/d/1upeZgVuQl_YEVCm7K38fqkjLjMeGj3Gh/view?usp=drive_link)


---

## 🗂 Directory Structure
```text
RadVUQA/
├── CT_Release_V1/
│ ├── images/
│ ├── masks/
│ ├── boxed_V2/
│ ├── boxed_easy_V2/
│ ├── CT_Release_V1.json
│ └── QA_CT_Release_V1.json
│
├── CT_Release_winAD_V1/
│ ├── images/
│ ├── masks/
│ ├── boxed_V2/
│ ├── boxed_easy_V2/
│ ├── CT_Release_V1.json
│ └── QA_CT_Release_V1.json
│
├── MR_Release_V1/
│ ├── images/
│ ├── masks/
│ ├── boxed_V2/
│ ├── boxed_easy_V2/
│ ├── MR_Release_V1.json
│ └── QA_MR_Release_V1.json
│
└── OOD_test/
├── images/ (various imaging conditions)
└── QA/ (out-of-distribution QA pairs)

- **images/**: Raw CT/MRI slices in DICOM or PNG.  
- **masks/**: Segmentation masks for anatomical structures.  
- **boxed_V2/**: Standard bounding box annotations.  
- **boxed_easy_V2/**: Simplified bounding box annotations.  
- **`*_Release_V1.json`**: Metadata files listing image IDs and target coordinates.  
- **`QA_*_Release_V1.json`**: JSON files containing question–answer pairs.  
- **OOD_test/**: Out-of-distribution test set for robustness evaluation.
```
---

## 🚀 Usage

1. ** images and masks**  
   Use `images/` and `masks/` folders for raw images and corresponding masks.

2. **Apply bounding boxes**  
   Use `boxed_V2/` or `boxed_easy_V2/` for images with bounding boxes.

3. **Parse QA pairs**  
   Use `QA_*_Release_V1.json` for question–answer annotations linked to each image.

4. **Utilize metadata**  
   Reference `*_Release_V1.json` for image-level metadata and anatomical coordinates.

5. **Evaluate on OOD**  
   Test model generalization on `OOD_test/` with varied imaging conditions.

---

## 📝 Citation

If you use RadVUQA in your research, please cite the following papers:

1. Nan Y, Zhou H, Xing X, et al. _Beyond the Hype: A Dispassionate Look at Vision–Language Models in Medical Scenario_. **IEEE Trans. Neural Networks Learn. Syst.**, 2025.

2. Wasserthal J, Breit H C, Meyer M T, et al. _TotalSegmentator: robust segmentation of 104 anatomic structures in CT images_. **Radiology: Artificial Intelligence**, 2023, 5(5): e230024.

3. Akinci D’Antonoli T, Berger L K, Indrakanti A K, et al. _TotalSegmentator MRI: Robust Sequence-independent Segmentation of Multiple Anatomic Structures in MRI_. **Radiology**, 2025, 314(2): e241613.

---

## 📖 License

[CC BY 4.0]
