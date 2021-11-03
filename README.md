# Speech-Recognition-with-Python

## Install SpeechRecognition Package
In the miniconda command shell

pip install SpeechRecognition (lastest version as of Nov 2021 is 3.8.1, conda has 3.7.1) 

In the jupyter notebook
import speech_recognition as sr (check if package can be imported)

sr.__version__ (verify the version)

## Create a Recognizer instance
r = sr.Recognizer()

recognize_bing(): Microsoft Bing Speech

recognize_google(): Google Web Speech API

recognize_google_cloud(): Google Cloud Speech - requires installation of the google-cloud-speech package

recognize_houndify(): Houndify by SoundHound

recognize_ibm(): IBM Speech to Text

recognize_sphinx(): CMU Sphinx - requires installing PocketSphinx

recognize_wit(): Wit.ai

## Supported File Types
Currently, SpeechRecognition supports the following file formats:

WAV: must be in PCM/LPCM format

AIFF

AIFF-C

FLAC: must be native FLAC format; OGG-FLAC is not supported

## Capture Data from a File
example = sr.AudioFile('./example.wav')
with example as source:
    audio1 = r.record(source, duration=35)
    audio2 = r.record(source, duration=35)
    audio3 = r.record(source, duration=35)
    audio4 = r.record(source, duration=35)

## Check the type of audio1
type(audio1)

## recognize the speech in the audio
r.recognize_google(audio1)

r.recognize_google(audio2)

r.recognize_google(audio3)

r.recognize_google(audio4)





