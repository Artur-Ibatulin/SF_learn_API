# SF_learn_API

Приложения, которое определяет тональность текста.
Необходимый перечень библиотек представлен в файле requirements.txt 

```python
from fastapi import FastAPI
from transformers import pipeline

app = FastAPI()
classifier = pipeline("sentiment-analysis")

@app.get("/")
def root():
    return {"message": "Hello World"}

@app.get("/predict/")
def predict():
    return classifier("I like machine learning engineering!")
```

## Запуск (Linux)
```python
    uvicorn main:app
```

