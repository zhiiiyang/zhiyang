---
authors:
- admin
date: "2020-01-01"
draft: false
gallery_item:
image:
  caption: ''
  focal_point: "center"
  preview_only: false
projects:
tags:
- Python
- Machine learning
title: 'Auto-generating GitHub commit messages using textgenrnn'
summary: a quick tutorial of using `PyGitHub` and `textgenrnn` in Jupyter notebook
---


## Introducing textgenrnn
`textgenrnn` allows easy and straightforward process of training a text-generating neural network with a few lines of code using Keras/TensorFlow. 
![](https://github.com/minimaxir/textgenrnn/raw/master/docs/textgenrnn_console.gif)


### Install PyGithub and textgenrnn
In this post, we will be introducing two Python libraries called [PyGitHub](https://github.com/PyGithub/PyGithub) and (textgenrnn)[(https://github.com/minimaxir/textgenrnn)]. You can type the commands in the Windows shell to install these two libraries.

```bash
pip install PyGitHub
pip install textgenrnn
```

### Store your GitHub token
Go to GitHub [website](https://github.com/settings/tokens) to generate your personal access tokens. Then type the following command in your Windows Shell to store it. 

```bash
set GITHUB_KEY = xxxxxxxxxxxxxxxxxxxxxx
```

### We're ready to auto-generate commit messages

```python
import os
from github import Github
from textgenrnn import textgenrnn
```

```python
GitHub_api = os.environ.get("GITHUB_KEY")
```

### Download commit messages from my personal website `zhiiiyang/zhiyang` on [GitHub](https://github.com/zhiiiyang/zhiyang)


```python
g = Github(GitHub_api)
repo = g.get_repo("zhiiiyang/zhiyang")
commits = repo.get_commits()
messages = []
for i in commits:
    messages.append(i.commit.message)
```

## Save it to a text file


```python
with open('commits.txt', 'w') as f:
    for message in messages:
        f.write("%s\n" % message)
```

## Read it into `textgenrnn`


```python
textgen = textgenrnn()
textgen.generate()
```

    All of the story of relationships who says "New All Trump Control Complete Man Works
    
    

## Train a model



```python
textgen.train_from_file("commits.txt", num_epochs=3)
```

    135 texts collected.
    Training on 2,248 character sequences.
    Epoch 1/3
    17/17 [==============================] - ETA: 18s - loss: 2.18 - ETA: 9s - loss: 2.3687 - ETA: 6s - loss: 2.428 - ETA: 5s - loss: 2.378 - ETA: 4s - loss: 2.279 - ETA: 3s - loss: 2.251 - ETA: 2s - loss: 2.198 - ETA: 2s - loss: 2.149 - ETA: 2s - loss: 2.151 - ETA: 1s - loss: 2.135 - ETA: 1s - loss: 2.091 - ETA: 1s - loss: 2.029 - ETA: 0s - loss: 2.000 - ETA: 0s - loss: 1.979 - ETA: 0s - loss: 1.949 - ETA: 0s - loss: 1.922 - 3s 200ms/step - loss: 1.8895
    ####################
    Temperature: 0.2
    ####################
    add the  in the image
    
    add the  in the sizes
    
    add the  in the site to the size
    
    ####################
    Temperature: 0.5
    ####################
    change the site of the sizes
    
    add the  in sizes
    
    add hail
    
    ####################
    Temperature: 1.0
    ####################
    change the sites
    
    fil a talk
    
    tag doo ssight
    
    Epoch 2/3
    17/17 [==============================] - ETA: 1s - loss: 1.077 - ETA: 1s - loss: 1.079 - ETA: 1s - loss: 1.152 - ETA: 1s - loss: 1.151 - ETA: 1s - loss: 1.096 - ETA: 1s - loss: 1.120 - ETA: 1s - loss: 1.095 - ETA: 1s - loss: 1.087 - ETA: 1s - loss: 1.102 - ETA: 0s - loss: 1.098 - ETA: 0s - loss: 1.080 - ETA: 0s - loss: 1.071 - ETA: 0s - loss: 1.069 - ETA: 0s - loss: 1.058 - ETA: 0s - loss: 1.065 - ETA: 0s - loss: 1.074 - 2s 129ms/step - loss: 1.0706
    ####################
    Temperature: 0.2
    ####################
    add a new post
    
    add a new post
    
    add a new post
    
    ####################
    Temperature: 0.5
    ####################
    post talks
    
    add my fix analy
    
    change the talk
    
    ####################
    Temperature: 1.0
    ####################
    change the finish
    
    add Sepost
    
    adjust salilogy
    
    Epoch 3/3
    17/17 [==============================] - ETA: 1s - loss: 0.730 - ETA: 1s - loss: 0.844 - ETA: 1s - loss: 0.762 - ETA: 1s - loss: 0.749 - ETA: 1s - loss: 0.745 - ETA: 1s - loss: 0.781 - ETA: 1s - loss: 0.773 - ETA: 1s - loss: 0.790 - ETA: 1s - loss: 0.776 - ETA: 0s - loss: 0.800 - ETA: 0s - loss: 0.809 - ETA: 0s - loss: 0.804 - ETA: 0s - loss: 0.797 - ETA: 0s - loss: 0.795 - ETA: 0s - loss: 0.806 - ETA: 0s - loss: 0.813 - 2s 129ms/step - loss: 0.8175
    ####################
    Temperature: 0.2
    ####################
    add a talk
    
    add a new post
    
    add a new post
    
    ####################
    Temperature: 0.5
    ####################
    change the talk
    
    add a new post
    
    add a new post
    
    ####################
    Temperature: 1.0
    ####################
    drag
    
    Mika font now slides finish shang haim
    
    change the laymor post
    
    

## Predict the safest commit message
`Temperature` parameter controls how conservative or risky the model's guess is going to be. The higher the value is, the riskier the prediction is. 


```python
textgen.generate(10, return_as_list=True, temperature=0)
```

    100%|██████████████████████████████████████████████████████████████████████████████████| 10/10 [00:00<00:00, 11.02it/s]
    




    ['add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post',
     'add a new post']



## Predict the riskies commit message


```python
textgen.generate(10, return_as_list=True, temperature=1)
```

    100%|██████████████████████████████████████████████████████████████████████████████████| 10/10 [00:00<00:00,  8.84it/s]
    




    ['change the change the deniik for color',
     'a smooj of tags',
     'change the post',
     'adjust cast',
     'add slides',
     'adidal strouther',
     'add a talk',
     'adjust playe font',
     'add the gobour',
     'delete the iam']


