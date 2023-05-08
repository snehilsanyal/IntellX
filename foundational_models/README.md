## Foundational Models

This is the folder for foundational model scripts

- Use different foundational models like LLMs, TTI, TTV in single-line imports
- Each model will have one .py file, which has different methods 
    1. load_model
    2. save_model
    3. export_model


```py3
import intellx.foundational_models as ifm 

llm_model = ifm.llms.load_model(model = ')

tti_model = ifm.text-to-image(model = 'stable-diffusion')

ttv_model = ifm.text-to-video(model = 'gen2')

```

