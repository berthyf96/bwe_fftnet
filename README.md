# bwe_fftnet
Implementation of Bandwidth Expansion Using Perceptually-Motivated Loss (ICASSP 2019). The network is a three-way split summation FFTNet, trained on a waveform-based loss and spectrogram-based perceptual loss.

Our paper describing this work as well as listening samples can be heard at our project page: https://pixl.cs.princeton.edu/pubs/Feng_2019_LBE/

**BibTeX:**

```
@inproceedings{feng2019bwe,
  title={Learning Bandwidth Expansion Using Perceptually-Motivated Loss},
  author={Feng, Berthy and Jin, Zeyu and Su, Jiaqi and Finkelstein, Adam},
  booktitle={ICASSP 2019-2019 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={606--610},
  year={2019},
  organization={IEEE}
}
```

## Getting started
This project was tested using Python 3.6 and CUDA 7.3.0. Requirements include:
* TensorFlow (tested on v1.4.1)
* NumPy
* LibROSA (tested on v0.6.2)

**Data:**
You can make your own training set by starting with wideband audio files. Prepare narrowband versions by loading wideband audio and resampling to your desired narrowband sampling rate (you can use `librosa.core.resample` to do this). Resample these back to the wideband sampling rate and save them as the target wideband sampling rate. 

## Train/test
All data preparation, training, and testing code is in `train_test.ipynb`. To train/test on your own audio files, simply prepare your own data directory in the same format as the provided `data/` folder.

## Miscellaneous
If you're interested in an RNN version, check out https://github.com/berthyf96/audio_sr. But this repo is not being maintained.
