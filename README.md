# 42-AI x POC Technical Test

- [42-AI x POC Technical Test](#42-ai-x-poc-technical-test)
- [The task](#the-task)
	- [Definition](#definition)
	- [The data](#the-data)
	- [The model](#the-model)
	- [Your results](#your-results)
- [What matters for this test](#what-matters-for-this-test)
- [Practical details](#practical-details)
	- [Setup for the Technical Test](#setup-for-the-technical-test)
	- [Submitting your work](#submitting-your-work)
	- [Questions](#questions)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


-----------------

> **POC** stands for *Proof of Concept*: a small, focused implementation whose goal is to demonstrate that an idea is technically feasible, rather than to deliver a production-ready product.

-----------------

# The task

## Definition

You need to classify a collection of clothes in each category they belong to.


## The data

You will need to use PyTorch to classify the [FashionMNIST dataset](https://github.com/zalandoresearch/fashion-mnist).

FashionMNIST is based on the MNIST dataset but for clothing.


![Fashion-MNIST data sample](./assets/Fashion-MNIST-dataset.ppm)

> Some caveats:
> 
> Fashion-MNIST is a dataset of Zalando's article images—consisting of 
> 	- a training set of 60,000 examples 
> 	- a test set of 10,000 examples. 
> 
> Each example is a 28x28 grayscale image, associated with a label from 10 classes. 
> 
> Zalando intends Fashion-MNIST to serve as a direct drop-in replacement for the original MNIST dataset for benchmarking machine learning algorithms. 
> 
> It shares the same image size and structure of training and testing splits.

## The model

For the construction of the model, you must use PyTorch.

On the architecture of your neural network (number and type of layers, activation functions, optimizer, ...) you are completely free!

## Your results

You need to evaluate your model results.

---------------------
# What matters for this test

We are looking for candidates with the ability to dive deep in a question, with the goal of solving a problem, and then share their findings in a comprehensive manner.


As such, we want you to document your thought and research process.

There is a lot of different choices that you have to make to solve this problem.

 - What model to use ? 
 - Which parameters to give him ? 
 - How to evaluate your results ?
 - ...

We want you to be aware of these choices, by specifying them in a markdown cell before your code blocks, and sourcing what motivated your choice.

It can be:
 - as simple as a link to an online tutorial found from a google search like `PyTorch FashionMNIST classification tutorial`
 - as complex as a citation from a relevant research paper
 - as adventurous as a conclusion from your own benchmark


It should be easy for someone discovering your notebook to read and understand your work.

---------------------
# Practical details

## Setup for the Technical Test

We recommend using [uv](https://docs.astral.sh/uv/), a modern and fast Python package manager. If you don't have it yet:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Then, at the root of the project, create an environment and install the dependencies:

```bash
uv init
uv add jupyter notebook ipykernel torch torchvision numpy matplotlib
```

This creates a `.venv/` folder at the root of the project containing all the dependencies. You can now open `Subject.ipynb` in one of the following ways.

### Option A — VS Code (recommended)

1. Open the project folder in VS Code (make sure the **Python** and **Jupyter** extensions are installed).
2. Open `Subject.ipynb`.
3. Click **Select Kernel** at the top-right of the notebook, choose **Python Environments**, and pick the interpreter located at `./.venv` (at the root of the project).
4. Run the cells. Because the kernel points to `./.venv`, all the dependencies installed with `uv add` are available — no extra installation needed.

### Option B — Jupyter in the browser

Launch the Jupyter web app directly from the uv environment:

```bash
uv run jupyter notebook
```

`uv run` executes Jupyter inside the project's `.venv`, so the `Python 3 (.venv)` kernel is selected automatically and all dependencies are available. Then open `Subject.ipynb` from the web interface.

### Option C — Google Colab

If you have any problems with your local setup, you can use [Google Colab](https://colab.research.google.com/?utm_source=scs-index): upload `Subject.ipynb`, and Colab will provide a ready-to-use Python environment (you may need to install missing packages with `!pip install ...` directly in a cell, since uv is not used there).


---------------------
## Submitting your work

Fill the notebook ```Subject.ipynb```, making sure to include your explanations and notes (in the markdown cells) alongside your code — they are as important as the code itself.

You can submit your work in one of two ways:

- **Send us the `Subject.ipynb` file directly**, with all your explanations and notes included.
- **Or create a Git repository** (e.g. on GitHub) containing your notebook and send us the link.

Before submitting, verify that we will be able to run the notebook without errors if we do it from the first cell to the last one.


-----

## Questions

If you have any questions, please contact Diego Agudelo, Director of the AI Lab (diego.agudelo@42ai.fr), and/or Allan Debert (allan.debert@42ai.fr).