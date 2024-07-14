ASR with Speaker Diarization
This project involves automatic speech recognition (ASR) with speaker diarization. The provided Jupyter Notebook demonstrates how to extract and analyze audio from a video, perform speaker diarization, and save audio chunks segmented by speakers.

Features
Download and convert video to audio (WAV format).
Perform speaker diarization using NVIDIA NeMo toolkit.
Extract and save audio segments per speaker.
Display and play audio chunks for each identified speaker.
Prerequisites
Google Colab or Local Jupyter Notebook: You can run the notebook either locally or on Google Colab.
Python 3.x: Ensure Python 3.x is installed.
Setup and Installation
Google Colab
Open Google Colab: Go to Google Colab.
Import Notebook: File -> Upload Notebook -> "GITHUB" tab -> copy/paste GitHub URL of this notebook.
Set up GPU: Runtime -> Change runtime type -> select "GPU" for hardware accelerator.
Install Dependencies: Run the installation cell provided in the notebook to set up all required packages.
Local Setup
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/your-repository.git
cd your-repository
Create and Activate a Virtual Environment

bash
Copy code
python -m venv venv
source venv/bin/activate # On Windows use `venv\Scripts\activate`
Install Dependencies

Install the dependencies manually or use the following commands:

bash
Copy code
pip install wget text-unidecode torchaudio pytube
pip install git+https://github.com/NVIDIA/NeMo.git@r2.0.0rc0#egg=nemo_toolkit[asr]
Ensure ffmpeg and sox are installed (usually handled by package managers like apt-get on Linux).

Usage
Prepare the Audio File: Provide the path to the audio file or a video URL. The notebook supports both directly specifying an audio file and downloading audio from a YouTube video.

Run the Notebook: Execute the cells in the notebook. The process includes:

Downloading and converting video to audio.
Setting up configurations for speaker diarization.
Performing speaker diarization to segment the audio by speakers.
Extracting and saving audio chunks for each speaker.
Playing the audio chunks for verification.
Interact with Results:

Audio Segmentation: View and play audio segments for each identified speaker.
File Output: Segmented audio files will be saved in the output directory.
Configuration
Domain Type: Set DOMAIN_TYPE to either "meeting" or "telephonic" based on the type of audio file.
Audio File Path: Update the audio_input_path variable to point to your audio file.
Example
python
Copy code
video_url = input("Enter the video URL: ")
wav_file = video_to_wav(video_url)
print(f"WAV file saved as: {wav_file}")
Provide the path to an audio file or YouTube video URL, and the notebook will handle the rest, including downloading, converting, diarizing, and segmenting the audio.

Troubleshooting
File Not Found: Ensure the provided audio file path is correct and the file exists.
Dependencies: Ensure all required packages are installed and compatible.
