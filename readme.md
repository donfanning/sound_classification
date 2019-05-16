# Audio Classification
**Sounds** matter, and even though they do not lend themselves easily to quantifiable interpretation, the way sounds sound are powerful and worth exploring.  

### directory organization
.
├── data
├── notebooks
├── README.md
└── slides.pdf

./data
├── speech_commands 
└── me

./notebooks
├── 1_preprocessing.ipynb
├── 2_modeling.ipynb
└── 3_evaluation.ipynb

### problem
The speech command dataset released under a Creative Commons-BY 4.0 license is found at https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html in the google AI blog, and is my source for audio classification.  The skeleton goal is to find an elegant way to transform cleaner and similarly sized audio files for accurate modeling, and the meat is to begin to expand upon that. 

### directory overview
Included in the **data** directory are the files used for code running and the audio files referenced as examples in the preprocessing and evaluation notebooks.  These are split between the speech commands dataset and the files I created or sourced from public domain.

**notebooks** _preprocessing_ is an overview of audio file exploration which led me to choose the mel spectogram as sole modeling feature, since it is expressive and yields accurate modeling.  _modeling_ is a code driven notebook that moves from file parsing, feature extraction, and data shaping through the model itself, which I export to _evaluation_ to evaluate its performance on wild data.

### conclusion
The delightfully surprising efficiency of mel spectograms as the sole feature for this 1 dimensional convolutional neural network to predict 30 words accurately on this dataset of audio files allows me to classify whatever I want within said range.  Vastly fuller domain knowledge is necessary for clearer interpretations of my experiment and I am pleased that the model's ability to make distinctions can be a damp launchpad for further analysis. 