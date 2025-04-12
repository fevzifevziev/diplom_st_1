# diplom_st_1
```mermaid
graph TD
    A[Пользовательский запрос] --> B[Векторный поиск]
    B -->|CSV: myDS.csv| C[SentenceTransformer<br>all-MiniLM-L6-v2]
    C --> D[FAISS<br>question_vectors.npy]
    D --> E[Контекст]
    E -->|Задачи + textBD.txt| F[Системный промпт]
    F --> G[Генерация<br>Mistral/OpenRouter]
    G --> H[Ответ с LaTeX]
    H --> I[Обработка LaTeX<br>QuickLaTeX API]
    I -->|PNG изображения| J[Замена на<br>[формула](latex_images/...)]
    J --> K[Вывод в консоль]
```
