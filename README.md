# audio-diffusion-model-merge
Simple script to merge two Sample Generator (Dance Diffusion) models by a set ratio.<br>
Will save to file if out_file is set. Requires Torch.<br>
Models are required to be trained with the sample lengths.
Usage:
```
from merge_models import ratio_merge

ratio_merge(
    model_a='G:/models/dub_modern_long_4000_44100_131072.ckpt', 
    model_b='G:/models/dub_neuro_44100_131072.ckpt', 
    out_file='G:/models/dub_modern_neuro_44100_131072.ckpt', 
    fp_precision='FP16', 
    alpha=0.5
    )
```
