# Mask-Language-Modeling for NLI

This is a project where we apply Mask Language Modeling (MLM) after using a prompting technique 
in order to perform Natural Language Inference (NLI). The models used are BERT, RoBERTa, GPT2 and BART.
The datasets used are SICK, SNLI and MNLI.

Firstly, it's a good idea to read the project report [here](./Project_report/Prompt_NLI_report.pdf). The project is divided into 2 experiments. The first part is the main experiment, while the second is the analysis part. 

## How to use:

For starters clone the repository:  `git clone https://github.com/arpajj/Mask-Language-Modeling-for-NLI/tree/update`

### A) Main Experiment:

Create templates by using `python create_templates.py`.

To use GPT-2 model, run `python run_gpt2.py --model MODEL_NAME --dataset DATASET_NAME --template START`.

To use BERT, RoBERTa and BART model, run `python runner.py --model MODEL_NAME --dataset DATASET_NAME --template START`.

### B) Analysis Part: 

Create the templates by running  `python create_templates.py` inside the directory [.../analysis/Helpers](./analysis/Helpers). 
You will be asked to enter the name of the dataset; you will have to choose between `sick`, `snli` or `multi_nli`.

Then, make the dataloaders by running `python make_dataloaders.py` (inside the directory [.../analysis/Helpers](./analysis/Helpers))
and again the name of the dataset used. It also returns all the short and long dataloaders (see report).

Important tokens: For the extraction of tokens from the validation set run the "runner_valid.ipynb" and copy the tokens produced in the end
for the 3 labels. Then paste them into the "runner.ipynb" so to run the section of "Important Tokens" for the test set.

Short & Long sequences: After the run of "make_dataloaders.py" run the section "Short & Long Sequences" of the "runner.ipynb".
