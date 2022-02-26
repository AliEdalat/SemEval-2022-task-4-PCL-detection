# SemEval-2022-task-4-PCL-detection

## AliEdalat at SemEval-2022 Task 4: Patronizing and Condescending Language Detection using Fine-tuned Language Models, BERT+BiGRU, and Ensemble Models

### Abstract

This paper presents the AliEdalat team system that participated in SemEval-2022 Task 4: Patronizing and Condescending Language (PCL) Detection. This task aims to detect the presence of PCL and PCL categories in text. This task helps prevent further discrimination against vulnerable communities. To detect the presence of PCL, we use the ensemble model, including three basic models: fine-tuned bigbird, finetuned mpnet, and BERT + BiGRU. This model performs worse than the baseline due to overfit and its rank is 68/78. We also offer another model to solve first model’s problem. We consider the different categories of PCL separately. To detect each category of PCL, we act like a PCL detector. Instead of BERT + BiGRU, we use fine-tuned roberta in making the models. Our model works better than baseline and our ranking is 26/49. We present new models in two categories that they have better performance than original models.

link to paper: 

The paper describes in detail the structure of the used models.


### task 1 result

|Model|Eval f1|Test f1|
|:----|:----|:----|
|(BigBird, MPNet, BERT+BiGRU)|0.5965|0.3031|
|(BigBird, MPNet)|0.5789|0.5505|
|Baseline |0.4829|0.4911|


### task 2 result

|Model|Eval f1|Test f1|
|:----|:----|:----|
|Our |0.3677|0.2531|
|Problem-free model in Compassion and Metaphor (PCM)|-|0.3160|
|Baseline |0.1340|0.1041|

results of our models in the "Compassion" and "Metaphor" categories

|Category|Model|Eval f1|Test f1|
|:----|:----|:----|:----|
|Metaphor|Our (MPNet, BigBird 1:4) |0.4557|0.1345|
| |PCM (MPNet, BigBird) |-|0.2947|
|Compassion|Our (BigBird, MPNet, RoBERTa) |0.5565|0.1129|
| |PCM (BigBird, MPNet)|-|0.3932|

BigBird 1:4 means that the two classes zero and one weigh one and four in the fine-tuned bigbird, respectively.
