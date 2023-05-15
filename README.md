<p align="center">
      <img src="https://i.ibb.co/52yx53P/parse.png" width="420">
</p>

<p align="center">
   <img src="https://img.shields.io/badge/python-3.10-green" alt="Python Version">
   <img src="https://img.shields.io/badge/Version-1.0(Alpha)-yellowgreen" alt="Parser Version">
   <img src="https://img.shields.io/badge/Licence-MIT-blueviolet" alt="License">
</p>

## О проекте

Скрапер/Парсер информации с hh.ru, собирает информацию о вакансиях по указанному запросу, создает папку с результатом парсинга.
В папке будет .csv файл со всеми данными, текстовый автогенерируемый отчет и графики сгенерированнные по полученной информации.
Детали использования смотреть в документации

## Настройка окружения для работы
1. Сначала нужно поставить виртуальное окружение
 ```bash
   python3.10 -m venv ../venv
   source ../venv/bin/activate
 ```
2. Скачать пакеты
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

После этого скрапер готов к использованию.

# Запуск скрапера

Запуск осуществляется через <strong>job.start_scraper.py</strong>

Появится ввод имени файла: ввести название файла(без расширения) .csv добавится само
Искомая работа(запрос): ввести работу вакансии с которой будет собирать скрапер
Количество страниц для парсинга: сколько страниц пройдет скрапер(страница == 20 вакансий)

<strong>!!!Важно пока имя файла и работу которую ищем должны называться одинаково</strong>(Потом это будет исправлено)

# Текстовый отчет и графики
Текстовый отчет будет содержать таблицу по городам с количеством вакансий, средней зарплате и среднем требуемом опыте и такую же таблицу с компаниями

Пример таблицы:

<p align="center">
      <img src="https://i.ibb.co/2ypJxjv/2023-05-15-02-52-32.png" width="1200"
</p>

Графики
Будут нарисованы графики с распределением зарплаты и опыта, также c 5 самыми выкосооплачиваемыми городами и распределением зарплат относительно опыта

Пример графика:
      
<p align="center">
      <img src="https://i.ibb.co/dgSrdzQ/2023-05-15-02-59-42.png" width="1200"
</p>




## Говнокодер(то есть разработчик который это написал)

- [Alex](https://github.com/Friztutu)

## Time for work

на 100 страниц(2000 вакансий) ≈ 1 час

## License

Project JobParser is distributed under the MIT licence


