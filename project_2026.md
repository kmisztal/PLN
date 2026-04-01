
# Projekt zaliczeniowy — NLP (magisterka)

## O co chodzi?

Zadanie polega na jest przygotowaniu **indywidualnego projektu NLP na dowolny temat**.

Najważniejsze w projekcie nie jest „wykręcenie najlepszego wyniku”, ale pokazanie, że rozumiecie Państwo:

- jak dane wpływają na model,
    
- jak preprocessing zmienia wyniki,
    
- kiedy bardziej złożony model pomaga,
    
- jak analizować błędy,
    
- jak wyciągać wnioski z eksperymentów.
    

---

## Temat projektu

Temat jest dowolny, o ile dotyczy NLP. Temat musi wpisywać się w jedną ze ścieżek

### Ścieżka A — klasyczne supervised NLP

- klasyfikacja tekstu
    
- analiza sentymentu
    
- spam / fake news
    
- intent classification
    
- authorship / style detection
    
- NLI / stance detection
    

### Ścieżka B — ekstrakcja informacji

- NER
    
- slot filling
    
- keyword extraction
    
- relation extraction
    
- entity linking
    

### Ścieżka C — retrieval i embeddingi

- semantic search
    
- duplicate question detection
    
- clustering dokumentów
    
- retrieval ranking
    
- recommendation over text
    

### Ścieżka D — generatywne NLP / LLM

- summarization
    
- QA
    
- RAG
    
- chatbot task-oriented
    
- prompt engineering
    
- fine-tuning małego modelu
    
- porównanie modeli foundation

## Dane

Mogą Państwo korzystać z:

- publicznych zbiorów danych (np. Kaggle, HuggingFace Datasets, UCI, własny scraping)
    
- własnych danych
    
- danych z API lub serwisów internetowych
    

W projekcie należy jasno opisać:

- źródło danych
    
- liczbę przykładów
    
- sposób czyszczenia danych
    
- podział na zbiory treningowy / walidacyjny / testowy
    
- potencjalne ograniczenia danych (szum, bias, brak balansu klas)
    

Możecie używać własnych danych albo publicznych datasetów.

---

## Co musi się znaleźć w projekcie?

### 1) Baseline

Najpierw przygotujcie **proste rozwiązanie bazowe**, np.:

- TF-IDF + Logistic Regression
    
- embedding search
    
- zero-shot prompting
    
- prosty model pretrained
    

To jest punkt odniesienia dla dalszych eksperymentów.

---

### 2) Minimum 3 eksperymenty

To najważniejsza część projektu.

Pokażcie **minimum 3 warianty rozwiązania**, które odpowiadają na konkretne pytanie.

Np.:

- czy preprocessing pomaga?
    
- czy lematyzacja poprawia wynik?
    
- czy transformer daje lepsze rezultaty?
    
- czy lepszy prompt działa lepiej?
    
- jak chunking wpływa na RAG?
    

Celem jest pokazanie, że projekt został przemyślany.

---

### 3) Ewaluacja

Porówanie wyników używając sensownych metryk, np.:

- accuracy / F1
    
- ROUGE / BLEU
    
- Recall@K / MRR
    
- human evaluation
    

Zlaecana:

- tabela wyników
    
- wykres
    
- krótkie omówienie
    

---

### 4) Analiza błędów

Zaprezentowanie:

- co działa dobrze,
    
- gdzie model się myli,
    
- jakie są typowe błędy,
    
- co mogło je powodować.
    

To często jest ważniejsze niż sama metryka.

---

### 5) Wnioski

Na końcu krótko:

- co najbardziej pomogło,
    
- co nie zadziałało,
    
- co Was zaskoczyło,
    
- czego się nauczyliście.
    

---

## Czy można używać LLM/API?

Tak — możecie używać gotowych modeli, modeli z Hugging Face i API LLM.

Ale:

> **LLM ma być narzędziem, a nie całym rozwiązaniem.**

Projekt nie może polegać wyłącznie na:

- jednym wywołaniu API,
    
- gotowym notebooku z internetu,
    
- tutorialu bez własnych eksperymentów.
    

Najważniejsze są **porównania i wnioski**.

---

## Co należy przygotować na obronę?

- notebook `.ipynb`
    
- kod potrzebny do uruchomienia
    
- krótki opis na początku notebooka
    
- wymagane biblioteki
    

Notebook powinien działać od początku do końca.

---

## Jak projekt będzie oceniany?

Najwięcej punktów dostaniecie za:

- sensowny problem i dane
    
- dobry baseline
    
- ciekawe eksperymenty
    
- pokazanie wpływu preprocessingu / modelu
    
- analizę błędów
    
- sensowne wnioski
    
- czytelny notebook
    

---

## Najważniejsze

Nie interesuje mnie projekt typu:

> „użyłem dużego modelu i działa”.

Interesuje mnie projekt typu:

> „sprawdziłem 3 podejścia, preprocessing poprawił wynik o 5%, ale większy model już nie pomógł”.

To właśnie jest **dobry projekt badawczo-eksperymentalny**.


## Kryteria oceniania (100 pkt)

| Element | Punkty |
| --- | --- |
| Definicja problemu i dane | 20 |
| Baseline i metodologia eksperymentów | 35 |
| Implementacja modelu / pipeline | 20 |
| Analiza wyników i błędów | 15 |
| Jakość kodu i reprodukowalność | 10 |
| Jeśli projekt dotyczy języka polskiego | 10 (bonus) |


# 10 przykładowych projektów 

| # | Projekt | Trudność (1–5) | Problem z danymi? |
| --- | --- | --- | --- |
| 1 | Analiza sentymentu recenzji produktów | 1 | **Nie** – bardzo łatwe (Amazon, IMDB, Allegro, Kaggle) |
| 2 | Wykrywanie fake newsów / clickbaitu | 2 | **Mały** – dane publiczne są dostępne, ale bywają zaszumione |
| 3 | NER dla ofert pracy (skills, stanowiska, technologie) | 3 | **Średni** – dane łatwe do zebrania, etykiety trudniejsze |
| 4 | Duplicate question detection (np. pytania ze StackOverflow/Quora) | 2 | **Nie** – bardzo dobre datasety publiczne |
| 5 | Semantic search po artykułach naukowych lub dokumentach PDF | 3 | **Nie** – dane łatwe z arXiv / własnych PDF |
| 6 | RAG chatbot odpowiadający na pytania z dokumentacji kursu | 4 | **Nie** – można użyć własnych materiałów kursowych |
| 7 | Automatyczne streszczanie newsów lub artykułów | 4 | **Mały** – dużo datasetów, ale ewaluacja trudniejsza |
| 8 | Klasyfikacja intencji wiadomości e-mail / support tickets | 3 | **Średni** – dane trzeba znaleźć lub zbudować |
| 9 | Porównanie prompt engineering vs fine-tuning małego modelu | 5 | **Nie** – można użyć gotowych datasetów z HF |
| 10 | Wykrywanie halucynacji w odpowiedziach systemu RAG | 5 | **Tak** – najtrudniejsze, dane często trzeba przygotować samemu |
