# Tips.ru REST API
## /getevents
###### Получить список событий доступных на сайте.

Параметры:
- start_date (int _timestamp_)
- end_date (int _timestamp_)
- first_team (string)
- second_team (string)
- sport (int)
- league (int)
- limit (int)

Возвращаемые данные:
- event_id 
- url
- title
- start_date
- sport
- league
- image
- odds_count

## /getodds
###### Получить список ставок к событию.

Обязательные параметры:
- event_id (int) **required**

Параметры:
- bookmaker (int)
- market_type (string)
- limit (int)

Возвращаемые данные:
- odds 
-- author
--- author_image
--- author_link
-- start_date
-- title
-- description
-- source
-- source_link
-- odds_data
--- market
--- participant
--- price

## /getinsides
###### Получить список инсайдов.

Параметры:
- event_id (int)
- date (int _timestamp_)
- limit (int)
- search_query (string)

Возвращаемые данные:
- id
- title
- description
- creation_date
- author
-- author_image
-- author_link
- source
- source_link

## /getnews
###### Получить список новостей.

Параметры:
- author (array)
- category (array)
- date (int _timestamp_)
- limit (int)
- search_query (string)
- filter (string)

Возвращаемые данные:
- id
- title
- description
- creation_date
- author
-- author_image
-- author_link
- source
- source_link
- image

