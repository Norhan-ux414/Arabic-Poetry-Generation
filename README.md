# Arabic Poetry Generation using AraGPT2

This project focuses on generating Arabic poetry using a pretrained Arabic language model.  
The main idea was to fine-tune an Arabic GPT model on Arabic poetry data so it can generate text that looks similar to Arabic poetic style.

## Dataset

I used the Arabic Poetry Dataset from Kaggle.  
From the dataset, I focused only on poems written by **Al-Mutanabbi** and filtered the poems that are written in **Fusha (classical Arabic)**.

The main column used for training was:
- `poem_text`

Other columns such as ids or links were not necessary for this project.

## Preprocessing

Before training the model, I cleaned the dataset by:
- removing missing values
- removing duplicates
- filtering only Al-Mutanabbi poems
- filtering only Fusha poems
- cleaning some unnecessary characters

After that, the data was split into:
- training set
- validation set
- test set

## Model

For this project I used the pretrained Arabic model:

**AraGPT2 (aubmindlab/aragpt2-base)**

This model is already trained on Arabic text, so it is more suitable for Arabic generation tasks.

## Training

The model was fine-tuned on the poetry dataset using Hugging Face Transformers and PyTorch.

Main training settings:
- Epochs: 3
- Batch size: 2
- Model: AraGPT2

## Text Generation

After training, the model was tested with different prompts such as:    


- يا قلب      
Example:

generate_poem("يا قلب ") 


## Results

The model was able to generate Arabic text that has a poetic tone.

## Tools Used

- Python  
- Pandas  
- PyTorch  
- Hugging Face Transformers


## Author

Created by: **[Norhan Yahay]**














































