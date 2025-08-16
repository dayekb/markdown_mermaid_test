---

## 🧠 Шпаргалка по Mermaid: История нейронных сетей

> Вставьте любой блок кода ниже в `README.md`, обернув его в тройные апострофы с указанием `mermaid`:
> ````
> ```mermaid
> ваш_код_здесь
> ```
> ````

---

### 1. **Timeline (Жизненная лента) — Эволюция нейросетей**
```mermaid
timeline
    title Эволюция нейронных сетей
    section 1940-е
        1943 : Перцептрон (Маккалок и Питтс)
        1958 : Перцептрон Розенблатта
    section 1980-е
        1986 : Обратное распространение ошибки (Rumelhart et al.)
        1989 : Первые свёрточные сети (LeCun)
    section 1990-е
        1997 : LSTM (Хёхрайтер и Шмидхубер)
    section 2010-е
        2012 : AlexNet побеждает в ImageNet
        2014 : GAN (Иан Гудфеллоу)
        2015 : ResNet
    section 2020-е
        2017 : Transformer (Vaswani et al.)
        2020 : GPT-3 (175 млрд параметров)
        2023 : GPT-4, Llama, Claude
```

---

### 2. **Flowchart (Блок-схема) — Архитектуры нейросетей**
```mermaid
flowchart TD
    A[Ранние сети] --> B[Перцептрон]
    A --> C[Многослойный перцептрон]
    C --> D[Свёрточные сети (CNN)]
    C --> E[Рекуррентные сети (RNN)]
    E --> F[LSTM / GRU]
    C --> G[Transformer]
    G --> H[Большие языковые модели]
    H --> I[GPT, Llama, PaLM]
    H --> J[Мультимодальные модели]
```

---

### 3. **Graph (Граф зависимостей) — Развитие вычислительных мощностей**
```mermaid
graph LR
    A[CPU] --> B[GPU]
    B --> C[TPU / NPU]
    C --> D[Кластеры GPU]
    D --> E[Облачные вычисления]
    E --> F[Тренировка моделей >100B параметров]
    F --> G[Доступность через API]
```

---

### 4. **Pie Chart — Источники данных для LLM**
```mermaid
pie
    title Источники данных для больших языковых моделей
    "Википедия" : 10
    "Книги" : 15
    "Научные статьи" : 10
    "Веб-страницы (Common Crawl)" : 50
    "Форумы и соцсети" : 10
    "Код (GitHub)" : 5
```

---

### 5. **Gantt (Диаграмма Ганта) — Ключевые события в ИИ**
```mermaid
gantt
    title Ключевые вехи в развитии ИИ и нейросетей
    dateFormat  YYYY
    section Архитектуры
    Перцептрон        : 1958, 1y
    CNN               : 1989, 2y
    LSTM              : 1997, 2y
    Transformer       : 2017, 1y
    section Модели
    AlexNet           : 2012, 1y
    GPT               : 2018, 1y
    GPT-3             : 2020, 1y
    GPT-4             : 2023, 1y
    section Инфраструктура
    GPU для ИИ        : 2012, 3y
    TPU               : 2016, 2y
    Облака для ML     : 2018, 5y
```

---

### 6. **ER Diagram — Источники данных и модели**
```mermaid
erDiagram
    DATASET ||--o{ MODEL : "использует"
    DATASET {
        string name
        string source
        int size_GB
    }
    MODEL ||--o{ INFERENCE_API : "выпускает"
    MODEL {
        string name
        int parameters_B
        string release_year
    }
    INFERENCE_API {
        string provider
        string endpoint
    }

    DATASET }o--|| "Common Crawl" : ""
    DATASET }o--|| "Wikipedia" : ""
    DATASET }o--|| "GitHub" : ""
    MODEL }o--|| "GPT-4" : ""
    MODEL }o--|| "Llama" : ""
    MODEL }o--|| "Claude" : ""
```

---

### 7. **User Journey — Путь данных в LLM**
```mermaid
journey
    title Путь данных в обучении LLM
    section Сбор
      Веб-скрапинг : 5: Common Crawl
      Книги и статьи : 4: Архивы
      Соцсети : 3: Публичные данные
    section Очистка
      Удаление дубликатов : 4: Да
      Фильтрация токсичности : 5: Да
      Токенизация : 5: Да
    section Обучение
      Предобучение : 5: На всём корпусе
      Дообучение : 3: На специализированных данных
      Выравнивание (RLHF) : 4: По человеческим оценкам
```

---

### 8. **State Diagram — Эволюция масштаба моделей**
```mermaid
stateDiagram-v2
    [*] --> SmallModel
    SmallModel --> MediumModel : Рост данных
    MediumModel --> LargeModel : GPU + параллелизм
    LargeModel --> GiantModel : Кластеры + оптимизации
    GiantModel --> DistributedTraining : TPUs, Pipeline Parallelism
    DistributedTraining --> EfficientInference : Quantization, Pruning
    EfficientInference --> EdgeDeployment : Мобильные и встраиваемые ИИ
```

---

## ✅ Как использовать
1. Скопируйте нужный блок.
2. Вставьте в `README.md` между тройными апострофами:
   ````markdown
   ```mermaid
   ваш_диаграмма_здесь
   ```
   ````
3. Убедитесь, что ваш хостинг (GitHub, GitLab и др.) поддерживает Mermaid.
   > ⚠️ GitHub пока **не поддерживает Mermaid по умолчанию** в README, но вы можете:
   > - Использовать [Mermaid Live Editor](https://mermaid.live) для генерации изображений.
   > - Или использовать платформы, где Mermaid работает (например, GitLab, Obsidian, Docusaurus).

---

## 📌 Советы
- Для GitHub: сохраните диаграммы как изображения через [mermaid.live](https://mermaid.live).
- Используйте `%% комментарии` внутри Mermaid, чтобы пояснить логику.
- Тестируйте диаграммы в редакторе: [Mermaid Live Editor](https://mermaid.live/edit)

