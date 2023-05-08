## Models

This is the folder for model scripts. IntellX provides two types of models:

1. Core models:

- IntellX core models 
- Thirdparty open-source models (like bloom, vicuna etc.)

2. Specialized models

These models are made by combining core and open-source models for specialized usecases. Some of the usecases provided are:
- AdTech
- Legal
- Healthcare
- Personal Assistant


- Use different core models like LLMs, TTI, TTV in single-line imports
- Each model will have one .py file, which has different methods 
    1. load_model
    2. save_model
    3. export_model


```py3
from intellx.models import core, specialized 

# Sample usage of core models
llm_model = core.llms.load_model(model = ')

tti_model = core.text-to-image(model = 'stable-diffusion')

ttv_model = core.text-to-video(model = 'gen2')

# Sample usage of combined models

```

