# audio-diffusion-model-merge
Simple script to merge two Sample Generator (Dance Diffusion) models by a set ratio.<br>
Will save to file if out_file is set. Requires Torch.<br>
Models are required to be trained with the same sample lengths, or data will be corrupted.
This is really just a snippet to use for reference, though if you'd like to import the script to your pipelines you can do so as well.
Usage:
```
from merge_models import ratio_merge

merged_model = ratio_merge(
    model_a='G:/models/dub_modern_long_4000_44100_131072.ckpt', 
    model_b='G:/models/dub_neuro_44100_131072.ckpt', 
    out_file='G:/models/dub_modern_neuro_44100_131072.ckpt', 
    fp_precision='FP16', 
    alpha=0.5
    )
```
