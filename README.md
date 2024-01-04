# The 🤗 NLP Course

This repo contains a summary from the **[Hugging Face NLP course](https://huggingface.co/course/chapter1/1)**. 

The course teaches you about applying Transformers to various tasks in natural language processing and beyond. Along the way, you'll learn how to use the [Hugging Face](https://huggingface.co/) ecosystem — [🤗 Transformers](https://github.com/huggingface/transformers), [🤗 Datasets](https://github.com/huggingface/datasets), [🤗 Tokenizers](https://github.com/huggingface/tokenizers), and [🤗 Accelerate](https://github.com/huggingface/accelerate) — as well as the [Hugging Face Hub](https://huggingface.co/models).

## 📔 Jupyter notebooks

The Jupyter notebooks containing all the code from the course are hosted on the [`huggingface/notebooks`](https://github.com/huggingface/notebooks) repo. If you wish to generate them locally, first install the required dependencies:

```bash
python -m pip install -r requirements.txt
```

Then run the following script:

```bash
python utils/generate_notebooks.py --output_dir nbs
```

If you use *venv* remember to install a new kernel into your jupyter lab/notebook: 


```bash
python -m ipykernel install --user --name=nlp-course-venv
```
This script extracts all the code snippets from the chapters and stores them as notebooks in the `nbs` folder.

## 🙌 Acknowledgements

The structure of this repo and README are inspired by the wonderful [Advanced NLP with spaCy](https://github.com/ines/spacy-course) course and [🤗 NLP course](https://huggingface.co/learn/nlp-course/).
