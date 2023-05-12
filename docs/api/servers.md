---
title: Сервера
description: Документация для взаимодействия с серверами
---

# Методы

## Информация о сервере
Данный метод информацию об указанном сервере

### Параметры запроса
| Тип | Путь      | Параметры 		|	Результат	|
|-----|-----------|---------------|-----------|
| GET | /bots/:id | :id - ID бота	| [ResourceServer](#resourceserver)


# Типы данных

## ResourceServer

|	Поле	|	Тип			|	Описание	|
|-------|---------|-----------|
|	id		|	строка	|	ID бота	|
|	name	|	строка	| Имя бота	|
|	shortDescription	|	строка	| Короткое описание	|
|	description	|	строка	| Описание сервера	|
|	avatar?	|	строка	| Аватар сервера (иконка) |
|	shortLink?	| строка	| Короткая ссылка на сервер	|
|	inviteLink	|	строка	| Ссылка-приглашение	|
|	premiumActive	|	true/false	|	Статус премиума	|
|	premiumSplashURL?	|	строка	|	Ссылка на сплеш	|	
|	premiumAutoFetch?	|	true/false	| Автообовление информации	|
|	standardBannerID	|	число	| ID стандартного баннера 	|
|	premiumBannerURL?	|	строка	| URL Премиум баннера сервера	|
|	owner	|	строка	| Владелец сервера	|
|	status	|	[ResourceStatus](#resourcestatus) | Статус сервера |
|	ratings	|	массив [ResourceRating](#resourcerating)	| Рейтинг сервера |
|	prefix	|	строка	| Префикс бота	|
|	createdDate	|	строка	| Дата создания	|
|	supportServerInviteLink?	|	строка | Ссылка на саппорт сервер	|
|	members?	| число	|	Количество участников	|
|	website?	|	строка	|	Ссылка на сайт	|
|	tags	|	массив [Tags](#tags)	|	Теги сервера	|
|	moderators	|	массив [PartialUser](#partialuser)	|	Модераторы	|
|	upCount	|	число	| Количество апов	|
|	ups?	|	массив [ResourceUp](#resourceup)	|	Апы сервера	|

---
## ResourceStatus
Статус сервера на мониторинге

| Код	|	Имя	|	Описание	|
|-----|-----|-----------|
|	0	|	Hidden	|	Сервер скрыт	|
|	1	|	Public	|	Сервер на мониторинге	|
|	2	|	Banned	| Сервер забаннен	|
|	3	|	Pending	|	Сервер ожидает проверки	|


## ResourceRating
Рейтинг Сервера

| Поле | Тип	| Описание	|
|------|------|-----------|
| count | число	|	Количество оценок |
| raiting	|	число | Рейтинг от 1 до 5	|

---

## Tags
Возможные теги сервера

| Код | Имя |
|-----|-----|
| 130 |Общение|
| 131 |Фан|
| 132 |Игры|
| 133 |Кино|
| 134 |Аниме|
| 135 |Искусство|
| 136 |Кодинг|
| 137 |Музыка|
| 138 |18+|
| 139 |Role-Play|
| 140 |Юмор|
| 160 |Genshin|
| 161 |Minecraft|
| 162 |GTA|
| 163 |CS|
| 164 |Dota|
| 165 |Among Us|
| 166 |Fortnite|
| 167 |Brawl Stars|
---

## ResourceUp
Информация о апе.

| Поле	| Тип	|	Описание	|
|-------|-----|-----------|
|	id	|	строка	|	ID апа
|	expires	|	строка	|	Дата истечения	|


## PartialUser
Тип PartialUser использует свойства из [UserProfiIe](/api/profiles#userprofile), но не имеет в себе свойств `badges` `bots` `servers`