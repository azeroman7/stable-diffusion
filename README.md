# Diffusion Models

This repository contains implementations of stable-diffusion (latent diffusion model) (text-to-image & image-to-image)

## Git clone
```bash
git clone https://github.com/azeroman7/stable-diffusion.git
```

## Install Environment via Anaconda (Recommended)
```bash
cd stable-diffusion
conda install pytorch torchvision -c pytorch

pip install diffusers==0.10.2
pip install huggingface_hub==0.10.0
pip install transformers==4.25.1
pip install invisible-watermark
```

## ckpt for stable-diffusion
```bash
--> download sd-v1-1.ckpt from https://huggingface.co/CompVis/stable-diffusion-v-1-1-original

mkdir -p models/ldm/stable-diffusion-v1/
cp ~/Downloads/sd-v1-1.ckpt models/ldm/stable-diffusion-v1/model.ckpt

```

## Run script --> see outputs folder for results
txt2img:
```bash
python scripts/txt2img.py --prompt "a photograph of an astronaut riding a horse" --plms

or ./run1.sh
```

img2img:
```bash
python scripts/img2img.py --prompt "A fantasy landscape, trending on artstation" --init-img data/bertrand-gabioud-CpuFzIsHYJ0.png --strength 0.5

or ./run2.sh
```

