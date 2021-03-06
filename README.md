# TSDSs
Code
Issues
Pull requests
Actions
Projects
Wiki
Security

This repository creates a ULMFiT model (by Howard & Ruder 2018) for tweet datasets. In this ReadME file the code files and folder structure is shortly explained as well as the setup procedure for the right PyTorch and fastai version.

Code Files:

  'model': 
standard ULMFiT (Howard and Ruder 2018) with Wikitext-103 as pretraining dataset and Twitter US Airline Sentiment dataset                  from Kaggle for fine-tuning and sentiment classification.

  'model_ext_pretraining':
Extension of standard ULMFiT part 1: Wikitext-103 language model extended by fine-tuning it on Sentiment140 dataset from Kaggle.

  'model_ext_small_vocab':
Extension of standard ULMFiT part 2: extendeded language model used as basis for sentiment classification on Twitter US Airline Sentiment dataset, using only the vocabulary of the Twitter US Airline Sentiment dataset for Fine-Tuning. 

  'model_ext_large_vocab':
Extension of standard ULMFiT part 3: extendeded language model used as basis for sentiment classification on Twitter US Airline Sentiment dataset, combining the vocabulary of the Sentiment140 and the Twitter US Airline Sentiment dataset for Fine-Tuning.

  'model_forward_pass':
Explaining the ULMFiT model process by an example tweet. Output and shape of each specific model layer is provided to get a detailed understanding how textual data is processed by a language model.

  'functions':
Code file with auxiliary functions in order to keep the code short in the model files.


Folder structure:

  'clas', 'lm', 'Test_lm', 'prediction':
Empty default folders where the model files store the tokenized tweet data in order to easy access them later. The code will automatically store the files in these folders and create a model folder with the saved learners.

  'datasets':
Folder where the used datasets from Kaggle have to be stored in so that the model files can access them.

  'wt103':
Folder where the parameters from the pretrained Wikitext-103 language model have to be stored in so that the model can access them

  'images':
Images for the blogpost

  'model_extension_parameters':
'clas' and 'lm' folders for the files 'model_ext_pretraining', 'model_ext_small_vocab' and 'model_ext_large_vocab'. The code will automatically store the files in these folders and create a model folder with the saved learners.


Fastai setup:

As we are working with the outdated version fastai 0.7.0. due to functionality issues, there are a few steps that need to be executed before starting with the code.

A detailled overview is provided by Jeremy Howard in the fastai forum (https://forums.fast.ai/t/fastai-v0-7-install-issues-thread/24652)

On Mac:
1. Open Terminal
2. Navigate to desired folder:            cd "~\path\folder"
3. Clone fastai repository from GitHub:   git clone https://github.com/fastai/fastai.git
4. Navigate to cloned repository:         cd fastai
5. Create environment:                    conda env create -f environment-cpu.yml
6. Activate environment:                  conda activate fastai-cpu
7. Start Jupyter Notebook: jupyter notebook

Make sure you activate the environment every time before starting the jupyter notebook


On Windows the commands have to be run in the Anaconda Prompt console. The Prompt console must be runned as an administrator.

    ?? 2022 GitHub, Inc.

    Terms
    Privacy
    Security
    Status
    Docs
    Contact GitHub
    Pricing
    API
    Training
    Blog
    About

Loading complete
