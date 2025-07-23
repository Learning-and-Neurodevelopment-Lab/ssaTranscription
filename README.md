# Pipeline Overview

`ssaTranscribe` is an audio-to-text transcription pipeline built from open-source, self-hosted tools to transcribe original _Sesame Street_ episodes and support the expansion of the _Sesame Street_ Archive (SSA). Its capabilities include multilingual transcription, keyword detection, speaker diarization, and voice matching.

## Motivation (Jul. - Dec. 2025)
`ssaTranscribe` is an audio-to-text pipeline designed to generate full-episode transcriptions for 4,397 original _Sesame Street_ episodes, enabling new ways to analyze and manage the content behind the _Sesame Street_ Archive (SSA). The primary goal of `ssaTranscribe` is to support the SSA’s expansion from ~5,000 to 35,000 labeled images featuring four target object categories (`face`, `number`, `place`, `word`). Specifically, by surfacing descriptive language from episode dialogue, `ssaTranscribe` will help to curate visually imaginative, stylistically diverse scenes that reflect children's experiences of wonder, play, and interactive learning.

## Directory Structure

This directory tree outlines the top-level folders and essential files included in `ssaTranscribe`:

```plaintext
ssaTranscribe/
├── data/                                        # Input and output data directories
│   ├── raw/                                     # Original unprocessed audio files
│   └── processed/                               # Audio clips segmented and ready for ASR
├── models/                                      # Pretrained model weights
│   └── asr_model.pt                             # Whisper or other ASR model file
├── scripts/                                     # Core logic for each pipeline step
│   ├── transcriptionwithspeakersv1.py           # Main script for processing audio to text
│   ├── diarize.py                               # Performs speaker diarization
│   └── postprocess.py                           # Formats and cleans transcripts
├── configs/                                     # YAML configuration files
│   └── default.yaml                             # Default settings for pipeline runs
├── README.md                                    # Project overview and usage
├── requirements.txt                             # Python package dependencies
└── run_pipeline.sh                              # End-to-end pipeline entry point
```

## Data Flow

- Table of input and output file 'categories' and their formats (i.e., Outputs: Transcript = `.txt` and `.json`)
- Diagram of how data are received, preprocessed (if applicable), and processed

## Implementation

- Compute requirements
- Installation instructions (packages, models, etc.)
- Configuration instructions (config files, environment variables, parameters, dependencies)
- Execution instructions
