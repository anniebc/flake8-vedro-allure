# flake8-vedro-allure

Плагин для flake8, основан на плагине [flake8-vedro](https://github.com/anniebc/flake8-vedro).
Может использоваться отдельно

Игнорирование правил стандартное для flake8:
- через файл `setup.cfg` и параметра `ignore`
- через комментарий `#noqa: ALR001`


## История
### Версия 0.0.1

Валидация тестовых сценариев на наличие декоратора allure_labels и его содержимого:

Возможности конфигурации в `setup.cfg`:


```
[flake8]
;опциональность декоратора для теста
is_allure_labels_optional = false

;теги, необходимые для каждого теста
required_allure_labels = Feature,Story,Priority

;теги, которые не могут быть навешаны на 1 тест несколько раз
unique_allure_labels = Priority
```