# IntellX

## Welcome to IntellX

IntellX is an attempt to .....


If you are new to the project and want to use/contribute, please read the project contributing guidelines [here](/guidelines.md). 

## Installation 

Install the project from PyPi:

` pip install intellx `

Or install from source 

``` 
git clone https://github.com/snehilsanyal/IntellX 
cd intellx
python setup.py install
```

Or install using Conda

```
conda env create --file=environment.yaml

```

Or using Docker

```
docker build --tag 'Dockerfile' 
```

Or using Poetry

```
poetry install ....

```


## Getting Started 

```py3
import intellx
from intellx.models import core, specialized
from intellx.datasets import instruct-mpt, dolly, oasst

# Easy to use models 
# Example: 
# {0: pre-train, 1: fine-tune}

# Load a pre-trained model
model = core.llms.load_model(model = 'vicuna-13b-delta', quantized = True, mode = 1)

# Train a model
# Example: 
# {0: train from scratch, 1: fine-tune}
model.train_model(model = 'bloom-7b', quantized = False, mode = 0, save_checkpoints = True)

# Use a specialized model for AdTech usecase
# Example:
model = specialized.load_model(model = 'bloom7b-intellx-adtech-S1')

# Save model 
model.save_model(format = ' .h5')

# Export model 
model.export_model(format = 'onnx')


```

## Pipeline 

Can we setup a whole pipeline for reproducing better results? Quickly implement new models?

Check out example notebooks [here](/examples/notebooks/)

`Pipeline: Data (ET) and Model (LD)`

1. Data Extraction (E)

This layer scrapes data from different sources:
- Tools we use (Slack, Jira)
- Tools we offer (Sight)

See utils/data.

2. Data Transformation (T)

This layer is used to transform the scraped data from layer E, to be used in a proper format. 

See utils/data.

3. Model Learning (L)

This layer uses already trained/fine-tuned models for different tasks to save time and resources. 

See foundational_models.

Also, applying different compression/quantization techniques comes under this stage.

See utils/models.

4. Model Deployment (D)

This layer is for deploying our own models to different platforms, web apps and deploying light weight models we prepared in the previous layer. Creating interfaces to interact with the model via slack bot/ chatbot comes under this stage.

See utils/models.


## Resources



## Show some love

```
doi citation: CITATION.cff

```
