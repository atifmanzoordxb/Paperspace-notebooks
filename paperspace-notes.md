
cyberes/gradient-base-py3.10:latest


## Run a1111
%cd /stable-diffusion-webui
!bash webui.sh -f --xformers --share --ckpt-dir /datasets/stable-diffusion-classic


git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git

cd stable-diffusion-webui/extensions

git clone https://github.com/Mikubill/sd-webui-controlnet.git

cd sd-webui-controlnet/models


wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11e_sd15_ip2p.pth

wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11f1e_sd15_tile.pth

wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11f1p_sd15_depth.pth

wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11p_sd15_canny.pth

wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11p_sd15_openpose.pth

wget https://huggingface.co/lllyasviel/ControlNet-v1-1/resolve/main/control_v11p_sd15_softedge.pth

wget https://huggingface.co/CiaraRowles/TemporalNet/resolve/main/diff_control_sd15_temporalnet_fp16.safetensors

wget https://huggingface.co/CiaraRowles/TemporalNet/resolve/main/cldm_v15.yaml

cp cldm_v15.yaml.1 diff_control_sd15_temporalnet_fp16.yaml



// Lora Download

https://civitai.com/api/download/models/62833
cd 62833 Detail_Tweaker_LoRA.safetensors



https://civitai.com/api/download/models/87153
cp 87153 Add_More_Details.safetensors



// Embedding

https://civitai.com/api/download/models/94057
cp 94057 FastNegativeV2.safetensors


https://civitai.com/api/download/models/9208
cp 9208 EasyNegative


https://civitai.com/api/download/models/77169
cp 77169 BadDream_UnrealisticDream



wget https://huggingface.co/Xynon/models/resolve/main/experimentals/TI/bad-image-9600.pt
wget https://huggingface.co/datasets/Nerfgun3/bad_prompt/resolve/main/bad_prompt_version2.pt
wget https://huggingface.co/yesyeahvh/bad-hands-5/resolve/main/bad-hands-5.pt
wget https://huggingface.co/datasets/gsdf/EasyNegative/resolve/main/EasyNegative.pt
wget https://civitai.com/api/download/models/5637

cp 5637 DeepNegativeV1.safetensors


wget https://huggingface.co/stabilityai/sd-vae-ft-mse-original/resolve/main/vae-ft-mse-840000-ema-pruned.ckpt