# py-notebooks

Collection of python notebooks to share experiments with the open source community.

## Dreambooth
- tried 1024px dreambooth finetuning in colab, but got OOM error. Could only finetune 512px images.
- Had to disable checkpointing by setting checkpointing_steps=2000. greater than max_steps. previously,I didn't specify the checkpoint steps, and by default it was 500. I also had set 500 as the max_steps. So upon completion it reached the checkpoint steps, and then tried to save the optimizer state and model which was too big for gpu memory and crashed. 
- another problem is that training for 500 steps gave black images, 250 steps also gave blank images. atleast in 512 px finetuning. training upto 150steps gave good results. Training in 512px and generating images in 1024 px gave elongated faces for trained subject.
- tried to run 1024px dreambooth
- tried to run 1024px dreambooth on sdxl in kaggle. 50 step version worked. see `sdxl finetune dreambooth 1024 px 50 steps.ipynb`. using P100 GPU in kaggle notebooks does the trick.
- 