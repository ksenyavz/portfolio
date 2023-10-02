# Проверь себя
## Концепция 

```yaml
${название сущности}: !concept
  определение: |
    Короткий ответ на вопрос "Что это такое?" …

  ${название примера}: !example |
    Описание ситуации …

  # Заложенная на будущее точка расширения функциональности.
  # Отмечается тегом !extension
  ${название расширенного примера}: !extension |
    Описание ситуации …

  # Пример того, чего точно быть не может. Показывает где заканчивается эта сущность и начинается другая.
  # Например, для "Машинного масла" мы можем исключить ситуацию "Жидкость для утоления жажды".
  # Отмечается тегом !exclusion
  ${название исключения}: !exclusion |
    Описание ситуации …
```
## User story
```yaml
Ученик — Просмотр прогресса тестирования: !func
  Прогресс на странице профиля: !story
    сделано: no
    ситуация: Хочу посмотреть свой прогресс прохождения тестирования и для этого захожу на страницу своего профиля
    успех: В конце страницы профиля вижу прогрес прохождения тестирования (в соответствии с дизайном)
    отказ: …
    что понадобится:
      - ${продукт}. ${функция}
  Прогресс на странице "Проверь себя": !story
    сделано: yes
    ситуация: Перехожу на страницу "Проверь себя"
    успех: Вижу на странице свой прогресс
    отказ: Я не авторизован, поэтому блока прогресса на странице не вижу
    что понадобится:
      - ${продукт}. ${функция}
  # Заложенная на будущее точка расширения функциональности.
  # Отмечается тегом !extension
  ${название истории}: !extension
    ситуация: …

  # Пример того, чего точно быть не может. Показывает где пролегает та граница функциональности, за которую
  # не следует выходить. Решение о такой границе (scope) принимает product owner.
  # Отмечается тегом !exclusion
  ${название истории}: !exclusion
    ситуация: …

Ментор — Просмотр прогресса тестирования ученика: !func
  Прогресс на странице профиля ученика: !story
    сделано: no
    ситуация: Хочу посмотреть свой прогресс прохождения тестирования и для этого захожу на страницу своего профиля
    успех: В конце страницы профиля вижу прогрес прохождения тестирования (в соответствии с дизайном)
    
```
