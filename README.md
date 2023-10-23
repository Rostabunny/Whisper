# Whisper
This is an installation guide for Whisper AI transcription.
Python 3.9.9 must be installed on your computer. It is easiest if this is the only version of Python that is installed. Download here: https://www.python.org/downloads/release/python-399/

When installing Python after download, you MUST select the option that says "PATH". If you do not, the pip command will not work, and the installation will not be able to process.

When Python has installed, open an elevated CLI, copy the below text, and right click on the command line. 
```
pip install setuptools-rust
pip install git+https://github.com/openai/whisper.git
```

This will install Whisper to your computer. 
Once whisper is installed, you may move on to the next steps of transcribing.

To create a transcription, open the CLI (elevated is prefered but not usually required) and make a prompt from the instructions below:

Whisper commands
First, locate to the folder where the audio source is. then, use the following prompt format:
>whisper --model 'x' --language en "filename_here"


Prompt breakdown:


>whisper
This is the initial command. Absolutely required.


--model
This will determine how much care the model takes on transcription. Note: larger model = longer wait time.
Options are (in size, small to large):
tiny.en
base.en
small.en
medium.en
large

Note: if transcribing a different language, remove the .en ending.


--language
This is not required for any models with .en endings. When using the large model, the process will be quicker if 'en' or other desired language is written. use prefix.

"filename_here"
this is the name of the file. copy and paste. .mp3, .wav, .mp4, and most other filetypes that include audio are supported.

High quality, slow prompt example:
whisper --model large --language en "20220417_121248.mp4"

Low quality, fast prompt example:
whisper --model tiny.en "20220417_121248.mp4"

Standard quality, medium speed prompt example:
whisper --model small --language english "20220417_121248.mp4"