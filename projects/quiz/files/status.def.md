**Инструкция по определению статусов квизов**

### 1. Введение
Данная инструкция регламентирует правила определения статуса квиза на основе заполненности ответов и завершённости.

### 2. Описание статусов
Каждый квиз может находиться в одном из следующих состояний:

- **Завершён** – если поле `ended=true`.
- **Закрыт** – если `ended=false` и **все** поля, начинающиеся с `field.*`, пустые.
- **Начат** – если `ended=false`, но хотя бы одно поле `field.*` содержит значение.

### 3. Алгоритм определения статуса
Для определения статуса квиза необходимо:
1. Проверить значение `ended`.
   - Если `ended=true`, статус = **"завершен"**.
   - Если `ended=false`, переход к следующему шагу.
2. Проверить заполненность полей `field.*`.
   - Если **все** `field.*` пустые, статус = **"закрыт"**.
   - Если хотя бы одно `field.*` заполнено, статус = **"начат"**.

### 4. Применение в отчетности
При анализе квизов во всех отчётах и визуализациях должна использоваться данная система классификации. Статус должен определяться автоматически согласно указанному алгоритму.

### 5. Контроль изменений
Любые изменения в логике определения статусов должны согласовываться и документироваться в обновлениях данной инструкции.

