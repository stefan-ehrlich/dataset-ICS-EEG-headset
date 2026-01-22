# dataset-ICS-EEG-headset

**Dataset: EEG recordings acquired with a practical customized EEG headset**

This repository contains EEG data recorded with a **customized, practical EEG headset** designed for unobtrusive and fast preparation EEG acquisition, particularly suited for studies involving participants with special needs.

The headset/device is described in:

> **Ehrlich, S., Alves-Pinto, A., Lampe, R., & Cheng, G. (2017).**  
> *A simple and practical sensorimotor EEG device for recording in patients with special needs.*  
> Neurotechnix 2017. 

The dataset contains EEG recordings for **three different task protocols**:

- **ErrP protocol** (eliciting error-related potentials)
- **Motor Imagery (MI)**
- **Serial Reaction Time Task (SRTT)**


---

## Repository structure

```text
dataset-ICS-EEG-headset/
├── data_cursor
    ├── s01/                      
    ├── s02/
    ├── ...                  
├── data_mi
    ├── s01/                      
    ├── s02/
    ├── ...   
├── data_srtt
    ├── s01/                      
    ├── s02/
    ├── ...   
└── README.md
```
## Task descriptions (brief)

### Task I – ErrP protocol (error-related potentials)
**Purpose:** provide EEG recordings eliciting error-related potentials (ErrP), enabling trial-based comparison of error vs. correct conditions and training of ErrP detection models.

**Design:** A protocol containing correct and erroneous outcomes/events is used to evoke error perception in the participant. Trials are annotated with event markers, enabling ERP analysis and single-trial classification.

**Folder:** `data_cursor`


### Task II – Motor imagery (MI)
**Purpose:** provide data suitable for motor imagery decoding (e.g., left vs. right hand motor imagery), typically used in BCI pipelines for sensorimotor rhythm modulation.

**Design:** Participants perform motor imagery trials (imagined movement rather than overt movement), allowing analysis of mu/beta modulations and training of MI classifiers.

**Folder:** `data_mi`


### Task III – Serial Reaction Time Task (SRTT)
**Purpose:** measure sensorimotor-related EEG activity during a repeated stimulus–response key-press task and provide data suitable for analyzing sensorimotor rhythms and ERD/ERS effects.

**Design:** In each trial, one out of multiple visual targets is presented and the participant responds via a key-press (right-hand response in the original validation study). Trials are time-locked to the motor response, making the data suitable for ERD/ERS or time–frequency analysis. 

**Folder:** `data_srtt`

---

## About the dataset

### Intended use
This dataset supports research in:
- EEG acquisition with fast-setup and practical wearable systems
- sensorimotor rhythms and ERD/ERS analysis
- motor imagery decoding / passive BCI
- ErrP detection and classification
- benchmarking preprocessing pipelines under realistic recording constraints

### Modalities and measures (overview)
Depending on the task, the dataset includes:
- **EEG recordings** acquired with the customized headset
- optional **EOG channel** for capturing eye movements / artifact reduction :contentReference[oaicite:1]{index=1}
- event markers/time references for trial segmentation
- task metadata depending on protocol

The headset is based on re-purposed **Emotiv EPOC** electronics integrated into a headphones-like design and provides: :contentReference[oaicite:2]{index=2}
- semi-dry saline felt-pad sensors
- electrodes positioned according to the 10–20 system over sensorimotor areas
- fast preparation time (≈ 5 min) and stable recording over typical session durations

For exact data formats, channel montage, sampling rate, and event codes, consult the dataset documentation provided in this repository.

## Citation

If you use this data, please cite:

```bibtex
@inproceedings{ehrlich2017practicaleegdevice,
  title     = {A simple and practical sensorimotor EEG device for recording in patients with special needs},
  author    = {Ehrlich, Stefan and Alves-Pinto, Ana and Lampe, Renee and Cheng, Gordon},
  booktitle = {Neurotechnix 2017},
  year      = {2017}
}
```
