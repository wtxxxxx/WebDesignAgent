# WebDesignAgent

## Description


## Demo Video
### Auto Generation
[feedback.webm](https://github.com/DAMO-NLP-SG/WebDesignAgent/assets/109561120/63641bf7-ffb6-4518-a594-4a7223ec2899)

### Human Feedback
[auto.webm](https://github.com/DAMO-NLP-SG/WebDesignAgent/assets/109561120/d5f099e0-5a01-44fa-bb26-bf7733fd9608)

## Quick Start

```bash
Make sure you install the google chrome
```

```bash
git clone https://github.com/DAMO-NLP-SG/WebDesignAgent.git
cd WebDesignAgent
pip install -r requirement.txt
```

### Add your API_KEY

#### Use Azure API

set your api config in LLM.py line 22
```python
os.environ["AZURE_OPENAI_ENDPOINT"] = ""
os.environ["AZURE_OPENAI_KEY"] = ""
os.environ["AZURE_OPENAI_API_VERSION"] = ""
```

#### Use Openai API

Set is_azure = False(LLM.py line 18)

and set your api config in LLM.py line 39
```python
os.environ["OPENAI_API_KEY"] = ""
os.environ["OPENAI_PROXY_URL"] = ""
```


### Run in terminal
Our method support three ways to generate a website: 

1. Depend on a description of a website.
2. Depend on a img of a website.
3. Both on them.

Set img(img path) or text in webdesign.py line 371

```python
agent.act(img = "1.png",text = "a shopping website")
```

And then
```bash
python webdesign.py
```


### Run in GUI
```python
python gui.py
```
Then you will enter the gui as follows:

You can select the mode between chat and web design, and choose the model.

#### Auto Generation
If you want to auto generate a website. You can follow the following steps to proceed：

1. set save file(the generated website will be saved in this file).
2. set the description of the website or give a img for website or both.
3. click plan.
4. set refine times you want.
5. click auto generation.


#### Human Feedback
If you want to generate a website more human control. You can follow the following steps to proceed：

1. set save file(the generated website will be saved in this file).
2. set the description of the website or give a img for website or both.
3. click plan.
4. click page you want to modify, and modify anything you want to change.
5. click create website.
6. enter feedback if needed and click refine website.