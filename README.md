# Русская документация TextBlob
Количество текстовых данных в Интернете значительно увеличилось за последние десятилетия. Нет сомнений в том, что обработка такого количества информации должна быть автоматизирована, и пакет TextBlob - один из довольно простых способов выполнить NLP - обработку естественного языка.

# TextBlob: упрощенная обработка текста
TextBlob - это библиотека Python (2 и 3) для обработки текстовых данных.  Он предоставляет простой API-интерфейс для погружения в общие задачи обработки естественного языка (NLP), такие как тегирование части речи, извлечение именных фраз, анализ тональности, классификация, перевод и многое другое.
>  from textblob import TextBlob
>  
>  text = '''
>  Заглавная угроза в рыбе "Капле" всегда поражала меня как высший фильм.
>  Монстр: ненасытно голодная амебоподобная масса, способная проникать
>  практически хоть куда, способная - как обреченный врач пугающе
>  описывать это - «ассимиляция плоти при контакте».
>  Будьте прокляты ехидные сравнения с желатином, это концепция с самым большим
>  разрушительным потенциальным последствием, мало чем отличаясь от сценария серой слизи
>  предложеным технологическими теоретиками, опасающимися что
>  искусственный интеллект процветает.
>  '''
>  
>  blob = TextBlob(text)
>  blob.tags           # [('The', 'DT'), ('titular', 'JJ'),
>                      #  ('threat', 'NN'), ('of', 'IN'), ...]
>  
>  blob.noun_phrases   # WordList(['titular threat', 'blob',
>                      #            'ultimate movie monster',
>                      #            'amoeba-like mass', ...])
>  
>  for sentence in blob.sentences:
>      print(sentence.sentiment.polarity)
>  **0.060**
>  **-0.341**
