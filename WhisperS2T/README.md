- Initial setup (create a conda environment)
```bash
conda create -n stt_env python=3.10
conda activate stt_env
```

```bash
conda deactivate
```

- Install dependencies
```bash
conda install pytorch # if not already installed
conda install conda-forge::ffmpeg
pip install -U whisper-s2t
conda install -c conda-forge portaudio
pip install pyaudio
```

> If faced error with `pytorch`, edit `/Users/{$USER}/miniconda3/envs/stt_env/lib/python3.10/site-packages/whisper_s2t/speech_segmenter/frame_vad.py` line 96, `torch.concatenate` to `torch.cat`