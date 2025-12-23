# Diffusion Models

This repository contains implementations of motion-diffusion-model (text-to-motion)

## Git clone
```bash
git clone https://github.com/azeroman7/motion-diffusion-model.git
```

## Install Environment via Anaconda (Recommended)
```bash
cd motion-diffusion-model

sudo apt update
sudo apt install ffmpeg

conda env create -f environment.yml
conda activate mdm

python -m spacy download en_core_web_sm
pip install git+https://github.com/openai/CLIP.git
sudo apt install -y imagemagick
pip install moviepy
```
## Additional installation (body_models, etc.)
```bash
bash prepare/download_glove.sh

--> download t2m.zip from https://drive.google.com/uc?id=1O_GUHgjDbl2tgbyfSwZOUYXDACnk25Kb
--> download kit.zip from https://drive.google.com/uc?id=12liZW5iyvoybXD8eOw4VanTgsMtynCuU
unzip t2m.zip
unzip kit.zip

--> download smpl.zip from https://drive.google.com/uc?id=1INYlGA76ak_cKGzvpOV2Pe6RkYTlXTW2
unzip smpl.zip -d body_models
```

## Dataset & Model for Text to Motion
HumanML3D data is already copied in ./dataset/HumanML3D
[HumanML3D from https://github.com/EricGuo5513/HumanML3D]

```bash
--> download model "humanml_trans_enc_512.zip" from https://drive.google.com/file/d/1PE0PK8e5a5j-7-Xhs5YET5U5pGh0c821/view
# copy to ./save/humanml_trans_enc_512/model000200000.pt & args.json
unzip humanml_trans_enc_512.zip -d ./save
```

## Run script --> ./save/\*/\*/*.mp4
```bash
./run.sh
```
