# VKPhotosGeoTags

## Описание проекта
** VKPhotosGeoTags ** — Скрипт, который выгружает на заданной территории в заданный промежуток времени фотки с геометками из VK

## Основные переменные
- vk_access_token — Токен для доступа к API VK
- coords - Широта и долгота рассматриваемой территории
- dist - Радиус поиска фоток (м.)
- start_date - Стартовая дата поиска фотографий (Например, 2022, 1, 1)
- end_date - Конечная дата поиска фотографий (Например, 2024, 12, 1)

## Возвращаемая переменная
gdf_points — GeoDataFrame с колонками:
- id - id фотографии
- owner_id - id пользователя/группы, опубликовавший фотографию
- url - Ссылка на фотографию
- date - Дата фотографии
- text - Описание фотографии при наличии
- lat - Широта
- long - Долгота

## Как получить API VK для доступа к сервису:
1. Переходим по [ссылке](https://id.vk.com/about/business/go/docs/ru/vkid/latest/vk-id/connection/create-application) и создаем приложение
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/1.jpg?raw=true)
2. Добавляем приложение
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/2.jpg?raw=true)
3. Включаем web и вводим имя для приложения
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/3.jpg?raw=true)
4. Вводим домен и redirect (Можно вставить любой сайт, например сам VK)
![alt text](https://github.com/[rstsluv]/[VKPhotoGeoTagsScrapper]/[images]/4.jpg?raw=true)
5. Вводим код из СМС
6. Заходим в мои приложенияа
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/6.jpg?raw=true)
7. Скроллим вниз и копируем сервисный ключ доступа
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/7.jpg?raw=true)
8. Вставляем свой ключ доступа в переменную vk_access_token
![alt text](https://github.com/rstsluv/VKPhotoGeoTagsScrapper/images/8.jpg?raw=true)