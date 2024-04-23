# Шпаргалка по Git
## Коммиты
### Оформление коммитов

**Рекомендации:**
1. Сообщение не должно быть длиннее 72 символов.
2. Сообщение должно относительно коротким и информативным.
   
   *Пример:* `git commit -m "Добавить урок про оформление сообщений коммитов"`
3. Для сообщений на русском языке часто рекомендуют использовать инфинитивы.

    *Пример:* `Добавить тесты для PipkaService`, `Исправить ошибку #123` и т.д.

   Для сообщений на английском рекомендуется использовать повелительное наклонение (англ. imperative).

    *Пример:* `Use library mega_lib_300`, `Fix exit button` и т.д.
   
**Стили оформления:**
1. **Корпоративный**  
   В корпоративном стиле в начале сообщения обычно указывают Jira-ID, а после — текст сообщения.  
    *Пример:* `$ git commit -m "LGS-239: Дополнить список пасхалок новыми числами" `
2.  **Conventional Commits**  
    Conventional Commits предлагает такой формат коммита: `<type>: <сообщение>`.  
    Первая часть type — это тип изменений. Таких типов достаточно много. Вот два примера:  
      - feat (сокращение от англ. feature) — для новой функциональности;
      - fix (от англ. «исправить», «устранить») — для исправленных ошибок.
        
    Более подробный список можно увидеть [на сайте с описанием этого стиля](https://www.conventionalcommits.org/ru/v1.0.0-beta.4/#%D1%81%D0%BF%D0%B5%D1%86%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D1%8F).

    *Пример:* `git commit -m "feat: добавить подсчёт суммы заказов за неделю" `

3. **GitHub-стиль**  
   Если коммит «закрывает» или «решает» какую-то задачу, то в его сообщении удобно указывать ссылку на неё. Для этого в любом месте сообщения нужно указать `#<номер задачи>`.
    
    *Пример:* `$ git commit -m "Исправить #334, добавить график температуры" `

### Исправления (редактирование) коммита:
1. Дополнить последний коммит новыми файлами

    *Пример:* `git commit --amend --no-edit `
   
 2. Изменить сообщение последнего коммита

     *Пример:* `git commit --amend -m "Новое сообщение"`
    
### Отмена изменений до коммита:
1. Отмена изменений одного файла

     *Пример:* `git restore --staged <file>`
2. Отмена всех изменений

   *Пример:* `git restore --staged .`
