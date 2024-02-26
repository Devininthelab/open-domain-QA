# Open Domain Question Answering

[Pretrained](https://huggingface.co/winvswon78/distilbert-finetuned-squadv2)

## Prerequisites
```python
datasets==2.16.1
evaluate==0.4.1
transformers[sentencepiece]==4.35.2
accelerate==0.26.1
```

## Inference

```python
# Use a pipeline as a high-level helper
from transformers import pipeline

PIPELINE_NAME = 'question-answering'
MODEL_NAME = 'winvswon78/distilbert-finetuned-squadv2'
pipe = pipeline(PIPELINE_NAME, model=MODEL_NAME)

#Example
INPUT_QUESTION = 'Where is the cat?'
INPUT_CONTEXT = 'The cat sits under the table, trying to catch a mouse.'
pipe(question=INPUT_QUESTION, context=INPUT_CONTEXT)
```

## Metrics
| Metric        | Score |
|---------------|-------|
| Exact         | 49.77 |
| F1            | 53.75 |
| Total         | 11873 |
| HasAns Exact  | 75.52 |
| HasAns F1     | 83.49 |
| HasAns Total  | 5928  |
| NoAns Exact   | 24.10 |
| NoAns F1      | 24.10 |
| NoAns Total   | 5945  |
| Best Exact    | 65.27 |
| Best Exact Thresh | -11.46 |
| Best F1       | 67.29 |
| Best F1 Thresh| -9.32  |
