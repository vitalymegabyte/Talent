# Talent
## Сборка и запуск
Собирается командой
`docker-compose build`

Запускается после этого
`docker-compose up`

## Стандарт разработки на фронтенде
Для названий используем CamelCase, однако файлы называем прописными-буквами-через-дефис. Названия .js-файлов всегда заканчиваются на .component.js

Страницы лежат каждая в отдельной папке в `src/pages`, аналогично компоненты лежат каждый в отдельной папке в `src/components`. Для добавления новой страницы создаем папку, кладём туда файл страницы. Затем проводим импорт в App.js:

`import NewPage from './pages/new/new.component';`

А после добавляем в роутер:

```
        <Switch>
          <Route path='/' component={IndexPage} />
          <Route path='/new' component={NewPage} />
        </Switch>
```



## Стандарт разработки на бэкенде
С библиотекой aiohttp я опыта ещё не имел, однако точно используем snake_case для названий файлов и CamelCase для названий классов. Для работы с БД будем использовать SQLALchemy.

## Использование Git
Для новых фич заводим ветки:
`git checkout -b [name]`
Пушим ТОЛЬКО в сторонние ветки. Мастер обновляется мердж-реквестами, и никак иначе.
