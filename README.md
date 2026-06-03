#  Sperm Whale Click Analyzer

A bioacoustic analysis tool for detecting, visualizing, and clustering sperm whale click patterns from hydrophone recordings — built to contribute to the broader effort of understanding cetacean communication.

---

## Motivation

Sperm whales possess the largest brain of any animal and communicate through complex click sequences called **codas**. Different whale clans have distinct dialects passed across generations — a form of culture. This project applies signal processing and unsupervised ML to analyze those patterns, with the goal of identifying structural regularities in their communication.

Inspired by [Project CETI](https://www.projectceti.org/) and the Watkins Marine Mammal Sound Database.

---

## What It Does

- Loads and preprocesses sperm whale hydrophone recordings (`.wav`)
- Reduces background ocean noise using adaptive thresholding
- Visualizes raw waveforms and spectrograms
- Detects individual click events and timestamps them
- Measures inter-click intervals (ICI) — a key feature in coda analysis
- Clusters similar click patterns using unsupervised ML

---

## Project Structure

```
whale_analyzer/
├── .venv/                      # Virtual environment
├── data/                       # Audio recordings (.wav)
│   ├── audio_1.wav             # 17.8s — 108 clicks
│   ├── audio_2.wav             # 10.0s — 40 clicks
│   └── audio_3.wav             # 44.0s — 128 clicks
├── whale_clicks.ipynb          # Spectrogram visualization
├── whale_exploration.ipynb     # Click detection & ICI analysis
├── .gitignore
└── README.md
```

---

## Getting Started

### Prerequisites
- Python 3.9+
- Git

### Installation

```bash
# Clone the repo
git clone https://github.com/dipesh-gupta03/whale-click-analyzer
cd whale-click-analyzer

# Create virtual environment
python -m venv .venv

# Activate (Windows)
.venv\Scripts\activate

# Activate (Mac/Linux)
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### Requirements
```
librosa
numpy
matplotlib
jupyter
scipy
scikit-learn
```

---

## Data Sources

Audio recordings sourced from:
- [Watkins Marine Mammal Sound Database](https://cis.whoi.edu/science/B/whalesounds/) — Woods Hole Oceanographic Institution
- [Macaulay Library](https://www.macaulaylibrary.org/) — Cornell Lab of Ornithology
- [Kaggle Bioacoustics Datasets](https://www.kaggle.com/)

All recordings used for research and educational purposes only.

---

## Current Progress

- ## Current Progress

- [x] Environment setup
- [x] Audio loading and playback
- [x] Waveform visualization
- [x] Noise reduction
- [x] Spectrogram generation
- [x] Automated click detection (276 clicks across 3 files)
- [x] Inter-click interval (ICI) measurement
- [x] ICI distribution comparison across recordings
- [ ] Unsupervised clustering of click patterns
- [ ] Feature extraction per click

## Background

Sperm whale clicks serve two distinct purposes:

**Echolocation clicks** — rapid, high-amplitude pulses used for hunting in deep water. Can reach 230 dB, the loudest sound produced by any animal.

**Codas** — patterned click sequences used for social communication. Each clan has recognizable coda repertoires passed down through generations, functioning similarly to dialects.

This project focuses primarily on coda detection and pattern analysis.

---

## Roadmap

- Integrate labeled coda data from Project CETI public releases
- Build supervised classifier for coda type identification
- Cross-clan comparison — detecting dialect differences between recordings
- Interactive visualization dashboard using Plotly

---

## References

- Whitehead, H. (2003). *Sperm Whales: Social Evolution in the Ocean*. University of Chicago Press.
- Rendell, L. & Whitehead, H. (2001). Culture in whales and dolphins. *Behavioral and Brain Sciences*.
- [Project CETI](https://www.projectceti.org/) — Cetacean Translation Initiative
- [Watkins Marine Mammal Sound Database](https://cis.whoi.edu/science/B/whalesounds/)

---

## Contributing

This is an active learning project. If you work in bioacoustics or marine ML and have thoughts on methodology — feel free to open an issue or reach out.

---

## License

MIT License — open for research and educational use.

---

*Built with curiosity about what 15 million years of ocean intelligence might sound like.*
