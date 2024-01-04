# How do Transformers work?
## Transformer History
- Original Transformer architecture: 2017, focus on translation tasks.
- GPT: 2018, fine-tuning on various **NLP tasks**.
- BERT: 2018, designet to produce **better summaries of sentences**
- GPT-2: 2019, improved version of **GPT**
- DistilBERT: 2019, faster and lighter version of BERT.
- BART and T5: 2019, Use the same architecture as the **original transformer**
- GPT-3: Improved version of **GPT-2**, no need of **fine-tunning (zero-shot learning)**
## Transformer categories
- GPT-like: *auto-regressive* transformer model
- BERT-like: *auto-encoding* transformer model
- BART/T5-like: *sequence-to-sequence* transformer model
## How do the language model transformers work?
These transformer models have been trained as *language models*. 

They have been **trained** on large amounts of **raw text** in a **self-supervised** fashion. This means the labels are created automatically from the inputs (like predicting the next word or filling in some masked words).

The **language models** develop a **statistical understanding** of the language it has been trained on.

This **statistical understanding** is not very useful. 

Because of that, the model goes through a **transfer learning** process.

The **transfer learning** process is a supervised fine-tunning using human-annotated labels on a given task.

Task examples:
- *casual language modeling*: predicting the next word in a sentence having read n previous words
- *masked language modeling*: model predicts a masked word

The general strategy for a **better performance** is by **increasing models' sizes** --> High environmental impact

### Transformer architecture
A transformer can have the following parts:
 - **Encoder**: Receives an input and builds a representation of it (**numbers**). It is optimized to acquire understanding from the input.
 - **Decoder**: Uses the **encoder** numerical representation (**features**) along with other inputs and generates a **target sequence**. It is optimized for generating outputs.

We can use those parts the following way:
- **Encoder-only models**:
    - Tasks that require **understanding of the input**
        - Sentence classification
        - Named Entity Recognition
- **Decoder-only models**:
    - Tasks that require text generation 
- **Encoder-Decoder or Sequence-to-Sequence models**:
    - Tasks that require generation and an input:
        - Translation
        - Summarization 

Using both encoder-decodre/ sequence-to-sequence transformer

#### Attention layers
A layer that tell the model to pay specific attention to **certain words** in the input sentence when dealing the **representation of each word**

#### Architectures and Checkpoints
- **Architecture**: Skeleton of the model
- **Checkpoints**: Weights that will be loaded in a given architecture

For example:
- **BERT** is an **architecture**
- `bert-base-cased`, a set of weights trained by the Google team for the first release of BERT, is a **checkpoint**.

However, one can say “the BERT model” and “the bert-base-cased model.”


## What is self-supervised learning?
Self-supervised learning is a **type of training** in which the objective is automatically compuited from the inputs of the model.

This means that humans are **not needed to label the data**.

## What is Pretraining
*Pretraining* is the **act of training a model from scratch**.

It requires:
- A large **corpus** of data
- Lots of money for computation
- Lots of time

## What is Transfer Learning?
**Transfer learning** is the act of initializing a model with **another model's weights**. 

**Faster** than training from scratch.

**Pros**:
- Better results than training from scratch.
- Less data needed
- Less computation needed.

**Cons**:
- Bias from regional and gender prejudices

ImageNet is used as a dataset for pretraining CV models.

In GPT-2 40GB of data from reddit used. BERT was trained with Wikipedia.

*Fine-tuning* is done **after** a model has been pretrained.

Steps:
1. Acquire the pretrained language model
2. Perform additional training with a dataset specific to your task

Advantages:
- Pretrained model was already trained with similarities from the fine-tuning dataset. The model will have already some statistical understanding.
- Less data needed for decent results.
- Less time needed.