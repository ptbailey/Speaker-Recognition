# Speaker Recognition
### Project Definition:   
Identifying which celebrity is speaking through deep neural networks. Applications for this project include machines matching commands with individuals through their voices, such that in the future, the machines can anticipate personal commands.

### Process:
1) Collected data from [VoxCeleb](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)[1], a database of celebrities' voices and images.
2) Extracted audio features referencing [Aaqib Saeed's code](http://aqibsaeed.github.io/2016-09-03-urban-sound-classification-part-1/) 
- **MFCC**: Mel-frequency cepstral coefficients
- **Melspectrogram**: Compute a Mel-scaled power spectrogram
- **Chorma-stft**: Compute a chromagram from a waveform or power spectrogram. "In music, the term chroma feature or chromagram closely relates to the twelve different pitch classes. Chroma-based features, which are also referred to as "pitch class profiles", are a powerful tool for analyzing music whose pitches can be meaningfully categorized and whose tuning approximates to the equal-tempered scale." (Wikipedia)
- **Spectral Contrast**: Compute spectral contrast. Spectral contrast is defined as the level difference between peaks and valleys in the spectrum
- **Tonnetz**: Computes the tonal centroid features (tonnetz)
3) Store features in pandas dataframe and prepare data for modelling
4) Run models

### Visualization examples of mel and tonnetz features:
Miranda Cosgrove's Mel             |  Smokey Robinson's Mel
:-------------------------:|:-------------------------:
![](https://github.com/ptbailey/Speaker-Recognition/blob/master/MC%20mel.png)  |  ![](https://github.com/ptbailey/Speaker-Recognition/blob/master/SR%20mel.png)

Miranda Cosgrove's Tonnetz             |  Smokey Robinson's Tonnetz
:-------------------------:|:-------------------------:
![](https://github.com/ptbailey/Speaker-Recognition/blob/master/MC%20tonnetz.png) | ![](https://github.com/ptbailey/Speaker-Recognition/blob/master/SR%20tonnetz.png)

### Best Model:
The best model was an 18 layer - CNN model using selu activation function, yielding 0.73 F1-score.    

Error and Validation Plots:     
![](https://github.com/ptbailey/Speaker-Recognition/blob/master/Error:Validation%20plot.png)

ROC Curve for all celebrities:    
![](https://github.com/ptbailey/Speaker-Recognition/blob/master/ROC%20curve.png)

### Demo:
Challenged my audience to try and guess the celebrity from an audio clipped I played. I then ran my model to try and determine the person as well. My model won with 3 more correct guesses than the audience.

![](https://github.com/ptbailey/Speaker-Recognition/blob/master/demo.gif)



Citation:  
[1] A. Nagrani, J. S. Chung, A. Zisserman  
VoxCeleb: a large-scale speaker identification dataset   
INTERSPEECH, 2017
