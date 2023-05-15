<p align="center">
      <img src="https://i.ibb.co/52yx53P/parse.png" width="420">
</p>

<p align="center">
   <img src="https://img.shields.io/badge/python-3.10-green" alt="Python Version">
   <img src="https://img.shields.io/badge/Version-1.0(Alpha)-yellowgreen" alt="Parser Version">
   <img src="https://img.shields.io/badge/Licence-MIT-blueviolet" alt="License">
</p>

## О проекте

Скрапер/Парсер информации с hh.ru, собирает информацию о вакансиях по указанному запросу, создает папку с результатом парсинга.<br/>
В папке будет .csv файл со всеми данными, текстовый автогенерируемый отчет и графики сгенерированнные по полученной информации.<br/>
Детали использования смотреть в документации

## Настройка окружения для работы
1. Сначала нужно поставить виртуальное окружение
 ```bash
   python3.10 -m venv venv
   source venv/bin/activate
 ```
2. Скачать пакеты
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

После этого скрапер готов к использованию.

# Запуск скрапера
<strong> в папке hh.ru-parser-scraper/job/ </strong>

```bash
python3 start_scraper.py
```

Появится ввод имени файла: ввести название файла(без расширения) .csv добавится само <br/>
Искомая работа(запрос): ввести название вакансии которую будет собирать скрапер<br/>
Количество страниц для парсинга: сколько страниц пройдет скрапер(страница == 20 вакансий)<br/>

<strong>!!!Важно пока имя файла и работу которую ищем должны называться одинаково</strong>(Потом это будет исправлено)

# Хранение данных

Все собранные данные в виде csv таблицы будут хранится в папке hh.ru-parser-scraper/job/csv_data
Папка csv_data будет создана автоматически

# Текстовый отчет
Текстовый отчет будет хранится в папке hh.ru-parser-scraper/job/<имя файла которое вы ввели>_annalyze/

Текстовый отчет будет содержать: 
1. Заголовок(запрос, время создания отчета).
2. Общую информацию(общее количество вакансий в таблице, среднее зарплата и средний требуемый опыт.
3. Таблицу по городам(количество вакансий в городе, средняя з/п этих вакансий, средний требуемый опыт этих вакансий)
4. Таблицу по компаниям(количество вакансий компании, средняя з/п этих вакансий, средний требуемый опыт этих вакансий)

Пример заголовка:
<p align="center">
      <img src="https://i.ibb.co/8dcdJKr/2023-05-15-06-19-44.png" alt="title" width="1200"
</p>   
      
Пример раздела с общей информации:
<p align="center">
      <img src="https://i.ibb.co/9qNX9N1/2023-05-15-06-21-54.png" alt="info" width="1200"
</p>

Пример таблиц:
<p align="center">
      <img src="https://i.ibb.co/2ypJxjv/2023-05-15-02-52-32.png" alt="table1" width="1200"
</p>
      

<p align="center">
      <img src="https://i.ibb.co/2399tg1/2023-05-15-06-23-44.png" alt="table2" width="1200"
</p>

      
# Графики
Нарисовынные графикки хранятся в папке hh.ru-parser-scraper/job/<имя файла которое вы ввели>_annalyze/graphs/<br/>
Будут нарисованы графики с распределением зарплаты, и распределением запрлаты от опыта

Пример графика:
      
<p align="center">
      <img src="https://i.ibb.co/dgSrdzQ/2023-05-15-02-59-42.png" width="1200"
</p>




## Говнокодер(то есть разработчик который это написал)

- [Alex](https://github.com/Friztutu)

## Time for work

на 100 страниц(2000 вакансий) ≈ 1 час

## License

Project hh.ru-parser-scraper is distributed under the MIT licence


