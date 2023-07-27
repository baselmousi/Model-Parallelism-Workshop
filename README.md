# Model-Parallelism-Workshop
Code and notes associated with the model parallelism workshop. The workshop was delivered by Nvidia. 
# Slides 
You can access the workshop slides via this [link](https://drive.google.com/drive/folders/1ngVnPV90p7OMoZ6dQLysZwcu45vs-CNb?usp=drive_link)
# Lab 1 
Lab 1 covers the material needed to scale the training of large neural models to multiple gpus. Slides 1 & 2 cover the needed material for the lab. 

## Notebooks summary 

1. Notebook 01 gives an overview of the class environment and introduces some basic slurm commands. Throughout the workshop, we used two nodes each containing two gpus.
2.  Notebook 02 gives an introduction about the distributed training strategies and uses the pytorch distributed launcher to scale the pretraining of GPT to multiple gpus within the same node.
3. Notebook 03 scales the training to multiple nodes and profiles the trianing using the pytorch profiler. It also introduces hybrid parallelism via running the pretraining using tensor parallelism and  pipeline parallelism.
4. Notebook 04 introduces possbile optimizations to the pretraining of gpt. It introduces concepts like mixed precision training, activation checkpointing, and gradient accumulation. Moreover, the notebook introduces some useful utils (computing number of parameters of a a model and estimating the peak flops and the amount of time needed to train the model)
5. Notebook 05 scales the training of an image classifier using deepspeed and the zero redundancy optimizer
6. Notebook 06 introduces the concept of a mixture of experts architecture and shows how we can add 'expert layers' to an architecture using deepspeed

## Papers 

## External Resources 

# Lab 2 
insert here lab 2 summary and important things to remember. Include a brief description for each notebook. 
# Papers and their summaries 
include links for each paper discussed along with a summary. maybe include the summary in an excel sheet.
# Conclusion and possible applicatiosn 

conclude the workshop and put a list of applications. Where Can you apply the knowledge that you learned??