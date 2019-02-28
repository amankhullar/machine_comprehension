# Allow me to answer : Machine Comprehension with Bi-Directional Attention Flow
Machine Comprehension and Question Answering is the task of answering a question based on a given context. The task needs to be carried out by the computer and this paper introduces to an end-to-end model for question answering. 
>The model combines the idea of Bi-Directional Attention Flow (BiDAF) network along with high performing bidirectional Gated Recurrent Units.

## Introduction

With the improvements in the state of the art models for Natural Language Processing, the task of machine comprehension for question answering has gained widespread importance.  The task involves the machine answering a given question based on the provided context. The answers are a sub phrase of the context with the model predicting the starting and the ending word of the chosen sub phrase.

## Model

![Model Architecture](model.png?raw=true)

### BiDirectional Attention Flow

The BiDAF is a high performing SQuAD model The core part of the model dictates that the attention flows in both the directions. Hence the context attends to the questions as well as the questions attend to the context.

## Execution

To exectute the model : 
 - Clone the Repository
```sh
$ git clone https://github.com/amankhullar/machine_comprehension.git
```

- Get the required packages
```sh
$ cd machine_comprehension
$ ./get_started.sh
```

- Activate the Environmnent
```sh
$ source activate squad
```

- To start training the model
```sh
$ python main.py --experiment_name=bidaf --mode=train
```
- Tracking Progress in TensorBoard
```sh
$ cd experiments
$ tensorboard --logdir=. --port=4242
```
Now open http://localhost:4242/ in your browser.

- Example illustration
```sh
$ python main.py --experiment_name=bidaf --mode=show_examples
```
## Acknowledgment

I would like to thank NLP Group at Stanford University for encouraging open learning and posting the course assignments and final project material of the course CS224n.

The lectures by Dr. Christopher Manning and Dr. Richard Socher helped me gain an insight into the field of Natural Language Processing which helped me complete this challenging project.

## References

This work is inspired from the work of Minjoon Seo et al. The link for their work is [BiDAF](https://allenai.github.io/bi-att-flow/)
