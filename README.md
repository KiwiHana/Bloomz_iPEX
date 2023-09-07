# Bloomz_iPEX
bloomz-560m has long 1st token latency 110s by iPEX

Run Bloomz-560m by iPEX

download model：https://huggingface.co/bigscience/bloomz-560m/tree/main
```
conda create -n llm python=3.9
conda activate llm
pip install torch==2.0.1a0 torchvision==0.15.2a0 intel_extension_for_pytorch==2.0.110+xpu -f https://developer.intel.com/ipex-whl-stable-xpu-idp
pip install accelerate sentencepiece
python test_bloomz.py
```

```
/home/ubuntu/miniconda3/envs/llm/lib/python3.9/site-packages/torchvision/io/image.py:13: UserWarning: Failed to load image Python extension: ''If you don't plan on using image functionality from `torchvision.io`, you can ignore this warning. Otherwise, there might be something wrong with your environment. Did you have `libjpeg` or `libpng` installed before building `torchvision` from source?
  warn(
Namespace(model_dir='/home/ubuntu/Downloads/kiwi/llm/bloomz-560m/', max_new_tokens=32, input_tokens='32')
Test /home/ubuntu/Downloads/kiwi/llm/bloomz-560m/...
The argument `trust_remote_code` is to be used with Auto classes. It has no effect here and is ignored.
<class 'transformers.models.bloom.modeling_bloom.BloomForCausalLM'>
torch.float16
torch.Size([1, 33])
torch.Size([1, 33])
=========First token cost 110.3764s=========
torch.Size([1, 33])
=========First token cost 0.0499s=========
torch.Size([1, 33])
=========First token cost 0.0200s=========
torch.Size([1, 33])
=========First token cost 0.0198s=========
torch.Size([1, 33])
=========First token cost 0.0191s=========
torch.Size([1, 33])
=========First token cost 0.0202s=========
torch.Size([1, 33])
=========First token cost 0.0201s=========
torch.Size([1, 33])
=========First token cost 0.0202s=========
torch.Size([1, 33])
=========First token cost 0.0202s=========
torch.Size([1, 33])
=========First token cost 0.0202s=========
Prompt: 我总是在晚上失眠,这个症状已经持续很长时间,所以晚上睡不着到底应该怎么处理,请告诉我一些可行的建议与方法,越详细越好
Output: ['我', '总', '是在', '晚上', '失眠', ',', '这个', '症状', '已经', '持续', '很', '长时间', ',', '所以', '晚上', '睡', '不着', '到底', '应该', '怎么', '处理', ',', '请', '告诉我', '一些', '可行的', '建议', '与', '方法', ',', '越', '详细', '越好', '']
Inference time: 0.02396416664123535 s
[136.0453770160675, 0.054793596267700195, 0.023982524871826172, 0.024051427841186523, 0.022850751876831055, 0.02391529083251953, 0.023853063583374023, 0.023738861083984375, 0.023859024047851562, 0.02396416664123535]
```
