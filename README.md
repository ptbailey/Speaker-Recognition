# Speaker Recognition
### Project Definition:   
Identifying which celebrity is speaking through deep neural networks. 

### Process:
1) Collected data from [VoxCeleb](http://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)[1], a database of celebrities' voices and images.
2) Extracted audio features referencing [Aaqib Saeed's code](http://aqibsaeed.github.io/2016-09-03-urban-sound-classification-part-1/) 
- **MFCC**: Mel-frequency cepstral coefficients
- **Melspectrogram**: Compute a Mel-scaled power spectrogram
- **Chorma-stft**: Compute a chromagram from a waveform or power spectrogram. "In music, the term chroma feature or chromagram closely relates to the twelve different pitch classes. Chroma-based features, which are also referred to as "pitch class profiles", are a powerful tool for analyzing music whose pitches can be meaningfully categorized and whose tuning approximates to the equal-tempered scale." (Wikipedia)
- **Spectral Contrast**: Compute spectral contrast. Spectral contrast is defined as the level difference between peaks and valleys in the spectrum
- **Tonnetz**: Computes the tonal centroid features (tonnetz)
3)



### Demo:
![](https://github.com/ptbailey/Speaker-Recognition/blob/master/demo.gif)



Citation:  
[1] A. Nagrani, J. S. Chung, A. Zisserman  
VoxCeleb: a large-scale speaker identification dataset   
INTERSPEECH, 2017
