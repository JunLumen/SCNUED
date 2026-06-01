# 🧠 SCNUED: South China Normal University Emotional EEG Dataset

This repository documents SCNUED and provides the application materials. Raw BDF files are distributed only after approval.

SCNUED v1.0 is a low-channel raw EEG dataset for emotion recognition research collected by the Brain-Computer Interface and Hybrid Intelligence Laboratory, South China Normal University (华南师范大学脑机接口与混合智能实验室). The public release contains 15 healthy student participants, 2 BDF recording sessions per participant, and 30 raw BDF files. The participants include 8 males and 7 females, aged 18-21 years. All participants volunteered and provided written informed consent before data collection. Each participant contributed approximately 10 minutes of effective EEG recording. No preprocessed EEG, differential entropy features, model outputs, or derived signals are included.

## 📌 Dataset Summary

- Institution: South China Normal University
- Laboratory: Brain-Computer Interface and Hybrid Intelligence Laboratory, South China Normal University / 华南师范大学脑机接口与混合智能实验室
- Release version: v1.0
- Release date: 2026-06-01
- Participants: 15 healthy student volunteers; 8 males and 7 females; age range 18-21 years
- Files: 30 raw BDF files
- EEG channels: Fp2, O1, O2, C3, C4
- Sampling frequency: 250 Hz for EEG channels
- Unit: uV
- Device: five-channel portable EEG headband
- Access: application-based academic non-commercial use
- Contact: <chenjiajun@m.scnu.edu.cn>

## 📁 Data Organization

The release uses a simple subject-folder layout:

```text
SCNUED-v1.0/
  SCNUED-v1.0_manifest.tsv
  sub01/
    sub01_session1.bdf
    sub01_session2.bdf
  ...
  sub15/
    sub15_session1.bdf
    sub15_session2.bdf
```

The source folder is used as the subject identifier. Source filenames are consistent with their source folders in this release.

## 🎬 Acquisition Protocol

SCNUED uses a passive audiovisual emotion-induction paradigm for positive, neutral, and negative affective responses. Conductive gel was applied before recording, and acquisition started after stable EEG waveforms and blink responses were confirmed. Source video clips are described for reproducibility and are not redistributed.

Data acquisition flowchart: [PNG image](img/data_acquisition_flow.png) / [source PDF](img/data_acquisition_flow.pdf)

| No. | Emotion | Source clip |
| --- | --- | --- |
| 1 | Positive | Flirting Scholar |
| 2 | Positive | Just Another Pandora's Box |
| 3 | Neutral | Aerial China, Episode 1 |
| 4 | Neutral | Aerial China, Episode 2 |
| 5 | Negative | Back to 1942 |
| 6 | Negative | Tangshan Earthquake |

Each recording is represented as `session1` or `session2` in the release package. No event files are included in v1.0 because the BDF annotation channels do not contain validated nonnumeric event labels.

## 🔒 De-identification and QC

Release BDF files are raw signal files with header de-identification. The patient, recording, date, and time fields are rewritten with pseudonymous SCNUED values. The EEG data records are not modified; `SCNUED-v1.0_manifest.tsv` includes source/release SHA256 values and confirms that the post-header data region is identical for every file.

Known QC notes:

- All released BDF files contain the five EEG channels Fp2, O1, O2, C3, and C4 at 250 Hz.
- Participant-level age and sex tables are not released in v1.0; only aggregate demographics are provided.

## 📥 Access and License

SCNUED raw BDF files are distributed under the SCNUED Academic Non-commercial Data Use Agreement. To request access, complete the application form and agreement, then send them to <chenjiajun@m.scnu.edu.cn>.

Users must not redistribute the raw data, attempt participant re-identification, use the data for commercial or clinical deployment, or publish derived resources that enable reconstruction of participant-level raw EEG.

## 📝 Citation

Please cite the associated SCNUED paper and acknowledge SCNUED in publications using this dataset. The final bibliographic entry and DOI should be added here when available.

## 🙏 Acknowledgements

We gratefully acknowledge equipment support from South China Brain Control (Guangdong) Intelligent Technology Co., Ltd. (华南脑控（广东）智能科技有限公司).
