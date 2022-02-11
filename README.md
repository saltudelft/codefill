# CodeFill
This repository contains the code for our paper titled as 
<b>"CodeFill: Multi-token Code Completion by Jointly Learning from Structure and Naming Sequences"</b>, DOI: 10.1145/3510003.3510172.
This work is authored by _Maliheh Izadi_, _Roberta Gismondi_, and _Georgios Gousios_ 
and it has been accepted for publication at #ICSE2022.

## Abstract
Code completion is an essential feature of IDEs, yet current autocompleters are restricted to either grammar-based or NLP-based single token completions.
Both approaches have significant drawbacks: grammar-based autocompletion is restricted in dynamically-typed language environments, whereas NLP-based autocompleters struggle to understand the semantics of the programming language and the developer's code context.

In this work, we present CodeFill, a language model for autocompletion that combines learned structure and naming information.
Using a parallel Transformer architecture and multi-task learning, CodeFill consumes sequences of source code token names and their equivalent AST token types.
Uniquely, CodeFill is trained both for single-token and multi-token (statement) prediction, which enables it to learn long-range dependencies among grammatical and naming elements.
We train CodeFill on two datasets, consisting of 29M and 425M lines of code, respectively.
To make the evaluation more realistic, we develop a method to automatically infer points in the source code at which completion matters.
We compare CodeFill against four baselines and two state-of-the-art models, GPT-C and TravTrans+.
CodeFill surpasses all baselines in single token prediction (MRR: 70.9% vs. 66.2% and 67.8%) and outperforms the state of the art for multi-token prediction (ROUGE-L: 63.7% vs. 52.4% and 59.2%, for n=4 tokens). 
We publicly release our source code and datasets.

# Data
Our datasets are available on <a href="https://huggingface.co/rgismondi/python-50k-dedup/tree/main">HuggingFace hub</a>. 
