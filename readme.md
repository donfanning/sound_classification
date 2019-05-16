# Audio Classification
**Sounds** matter, and even though they do not lend themselves easily to quantifiable interpretation, the way sounds sound are powerful and worth exploring.  

### problem
The speech command dataset released under a Creative Commons-BY 4.0 license is found at https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html in the google AI blog, and is my source for audio classification.  The skeleton goal is to find an elegant way to transform cleaner and similarly sized audio files for accurate modeling, and the meat is to begin to expand upon that.

### data
The data is 64,729 wave files of different people saying the word that bears the name of the subdirectory, so 2,367 files of about one second duration of people saying "right", to 1,746 files of people saying "Marvin".  This inherent regularity

### notebooks
_preprocessing_ is an overview of audio file exploration which led me to choose the mel spectogram as sole modeling feature, since it is expressive and yields accurate modeling.  The librosa library is incredible for beginner audio analysis and here https://musicinformationretrieval.com/index.html is a recommended resource for audio analysis and although it is pregnant with possibilities for audio analysis that are unnecessary for CNN modeling, I show examples of raw waves, mel spectograms, onsets, and spectral analysis.  

_modeling_ is a code driven notebook that moves from file parsing, feature extraction, and data shaping through the model itself, which I export to _evaluation_ to evaluate its performance on wild data.  Once the mel spectogram shone as the feature to use, I ran several models and looked the most at two dimensional CNNs before realizing the 1D performed better in terms of speed and accuracy.  Both models require similar preprocessing and I include only what is needed for the 1D CNN to be fed.

_evaluation_ is set aside for applied evaluation of the model on wild data by setting up functions that run slightly different types of audio files.  The best test is me recording myself saying the words I know the model remembers, which it got correct every time, even adding some inflection to my voice and compressing the file, although it wasn't as sure shown by lower prediction probability.  , and then changing the inputs to be more abstract.  

### conclusion
The delightfully surprising efficiency of mel spectograms as the sole feature for this 1 dimensional convolutional neural network to predict 30 words accurately on this dataset of audio files allows me to classify whatever I want within said range.  Vastly fuller domain knowledge is necessary for clearer interpretations of my experiment and I am pleased that the model's ability to make distinctions can be a damp launchpad for further analysis.
