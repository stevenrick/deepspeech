# deepspeech
based on https://github.com/mozilla/DeepSpeech/releases/tag/v0.9.3

## Setup

- Download and install Docker Desktop for your OS - https://www.docker.com/get-started/
- Download and unzip Ffmpeg for Windows - https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip or for Mac - https://evermeet.cx/ffmpeg/ffmpeg-5.0.1.zip
- Make note of where you put `ffmpeg.exe` as you will need this later
- `Git clone` this repository or download and unzip it - https://github.com/stevenrick/deepspeech/archive/refs/heads/main.zip
- Download https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.pbmm and https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.scorer
- Put the .pbmm and .scorer files in the deepspeech folder you either cloned or unzipped earlier
- Create a new folder named `data` in the deepspeech folder

## Prepare your audio
- Whether working with video or other audio files it needs to be converted to be compatible with the ASR system
- Use the command under ## audio prep ## in `cmds.txt` to convert input to a compatible output from your terminal or command prompt
- Put those output files into your `data` folder

## Prepare docker
- Follow all but the last command (in order) under ## setup & run ## in `cmds.txt` from your terminal or command prompt
- Note these are tested and work on a Windows host machine with an Nvidia GPU / CUDA support - your milage may vary in other scenarios
- Note that `//path/to/deepspeech` needs to be replaced with the correct full path to the location of the deepspeech folder on the host machine

## Run the ASR system
- Run the last command under ## setup & run ## in `cmds.txt` to generate transcripts as .txt files from inside your docker container
- Note that `audio_input_file.wav` needs to be replaced with the correct name of the audio files in your data folder
