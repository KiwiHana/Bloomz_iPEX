# Bloomz_iPEX
Run Bloomz-560m by iPEX
```
conda create -n llm python=3.9
conda activate llm
pip install torch==2.0.1a0 torchvision==0.15.2a0 intel_extension_for_pytorch==2.0.110+xpu -f https://developer.intel.com/ipex-whl-stable-xpu-idp
pip install accelerate sentencepiece
python test_bloomz.py
```
