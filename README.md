
# Evaluation of Text Generation Tasks

Code is adapted from [COCO Captions Evaluator]('https://github.com/tylin/coco-caption')


Usage
 
```pythonstub
from evaluator.eval import Evaluator

# list of predicted sentences 
y = [
"Trump is the president of United States",
"Obama is the ex president of United States"
]
# list of ground truth  (or list of lists of multiple ground truths)
# can have multiple label sentences per input  
# evaluation code will pick the closest one to the predicted target

labels = [
"Trump is the president of USA",
"Obama is the ex of USA"
]

e = Evaluator(y, labels)
e.evaluate()

print(e.overall_eval)

```

Results
```python

{'Bleu_1': 0.6490006524513375,
 'Bleu_2': 0.5948189231818395,
 'Bleu_3': 0.5563635247729869,
 'Bleu_4': 0.5088831646200179,
 'CIDEr': 6.3483970550044528,
 'METEOR': 0.4589624106163319,
 'ROUGE_L': 0.72752674981258092}

```



