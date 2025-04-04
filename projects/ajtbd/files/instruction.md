# Инструкция для JTBD-анализа интервью с риелторами

## I. Структура и методология анализа

### 1. Определение иерархии работ
- **Уровень 1:** Верхнеуровневые работы (например, "Привлечение клиентов")
- **Уровень 2:** Конкретные каналы и методы, направленные на достижение верхнеуровневой цели
- **Уровень 3:** Специфические подработы, раскрывающие механизм выполнения работ 2-го уровня

### 2. Правила формирования работ и иерархии
- **Избегать обобщающих работ:** Не создавать работы, объединяющие или дублирующие другие работы того же уровня
- **Конкретизация:** Работы одного уровня должны представлять разные методы или каналы, а не быть обобщением друг друга
- **Детализация:** На каждом последующем уровне раскрывать конкретные инструменты и процессы для достижения работы верхнего уровня

### 3. Процесс анализа интервью
1. **Последовательное чтение:** Обрабатывайте интервью целиком, отмечая все упоминания работ
2. **Группировка цитат:** Объединяйте схожие высказывания под общими темами
3. **Выделение барьеров и болей:** Особое внимание уделяйте эмоционально окрашенным фразам
4. **Проверка контекста:** Убедитесь, что цитата содержит полный контекст, а не вырвана из него

### 4. Выделение точных цитат
- Используйте только прямую речь интервьюируемого
- Цитаты должны включать полное описание работы, не ограничиваясь отдельными словами
- При наличии нескольких цитат о той же работе, разделяйте их символом "|"
- Исключайте короткие ответы типа "Да", "Конечно", "Согласен"

## II. Формат описания работ (Jobs Format)

### Структура описания каждой работы:
1. **ID работы:** Уникальный код (W001, W002, ...)
2. **Родительская работа:** ID работы верхнего уровня (пусто для уровня 1)
3. **Аудитория:** "АН" - агентство недвижимости, "ЧМАК" - частный маклер
4. **Уровень иерархии:** 1, 2 или 3
5. **Формулировка:** "Когда [контекст], я хочу [действие], чтобы [результат]"
   - Важно: результат подработы должен соответствовать действию родительской работы
6. **Цитаты:** Полные дословные высказывания из интервью
7. **Источник:** Имя файла интервью
8. **Текущие решения:** Инструменты и методы выполнения работы
9. **Важность:** Оценка от 0 до 1, рассчитанная по формуле:
   ```
   Важность = (Частота упоминания × Эмоциональная окраска) / Максимальное значение в выборке
   ```
10. **Неудовлетворенность:** Оценка от 0 до 1, рассчитанная по формуле:
   ```
   Неудовлетворенность = Упомянутые проблемы / (Упомянутые проблемы + Упомянутые решения)
   ```

## III. Критерии оценки эмоциональной окраски и частоты

### Эмоциональная окраска:
- **3 балла:** Высказывания с сильными положительными эмоциями ("обожаю", "это ключевое для меня")
- **2 балла:** Нейтрально-положительные высказывания ("эффективно работает", "приносит результат")
- **1 балл:** Нейтральные упоминания без эмоциональной оценки
- **-1 балл:** Упоминания проблем и трудностей ("сложно", "отнимает время")
- **-2 балла:** Сильные негативные эмоции ("ненавижу", "вызывает стресс")

### Частота упоминания:
- Подсчет количества отдельных упоминаний работы в разных контекстах
- При повторных упоминаниях в одном контексте считать как одно

## IV. Предотвращение дублирования и избыточной абстракции

### Правила для избежания избыточных работ:
1. **Не создавать обобщающие работы того же уровня**, если для этого уровня уже существуют конкретные детализированные работы (например, не создавать работу "Использовать разные каналы для привлечения", если уже есть конкретные работы "Вести социальные сети", "Получать рекомендации")
2. **Фокусироваться на конкретных инструментах и каналах**, а не на обобщенных описаниях
3. **Проверять новые работы на пересечение с существующими**, избегая дублирования смысла
4. **При появлении новой информации** дополнять уже существующие работы, а не создавать новые с похожим содержанием

### При анализе нескольких интервью:
1. Сначала построить базовый граф работ на основе первого интервью
2. При анализе последующих интервью сопоставлять упомянутые работы с уже имеющимися в графе
3. Добавлять новые работы только если они действительно отличаются от существующих
4. Обогащать существующие работы новыми цитатами и уточнениями из новых интервью

## V. Формат результатов

Результаты анализа должны быть представлены в CSV-формате с разделителем ";" со следующими столбцами:
```
ID;Родительская работа;Аудитория;Уровень иерархии;Формулировка;Цитаты;Источник;Текущие решения;Важность;Неудовлетворенность
```

## VI. Практические рекомендации

### При работе с интервью:
1. Выделяйте сначала все работы верхнего уровня, затем переходите к детализации
2. Обращайте внимание на выражения типа "я хочу", "мне нужно", "я должен"
3. Ищите описания процессов, которые респондент выполняет регулярно
4. Отмечайте инструменты и сервисы, которые упоминаются в контексте выполнения работы
5. Фиксируйте эмоциональные реакции при описании различных аспектов работы

### Для точности анализа:
- Проводите перекрестную проверку работ разных уровней на логическую связность
- Убедитесь, что все значимые фрагменты интервью проанализированы
- При формулировке работ используйте язык и терминологию, близкую к оригинальным высказываниям