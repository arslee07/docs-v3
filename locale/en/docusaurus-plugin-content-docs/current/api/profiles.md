---
title: Профили
description: Документация для взаимодействия с профилями
---

# Методы

## Информация о профиле пользователя

Данный метод информацию об указанном профиле

### Параметры запроса

| Тип | Путь        | Результат	                   |
|-----|-------------|------------------------------|
| GET | /users/:id	 | [UserProfiIe](#userprofile)	 |

# Типы данных

## UserProfile

| 	Поле	              | 	Тип			                                        | 	Описание	                  |
|---------------------|------------------------------------------------|-----------------------------|
| 	username	          | 	строка	                                       | Имя пользователя            |
| 	discriminator	     | строка                                         | Дискриминатор пользователя	 |
| avatar?	            | строка	                                        | Аватар	                     |
| id	                 | строка	                                        | ID пользователя	            |
| 	badges	            | массив [UserBadge](#userbadge)                 | Значки пользователя	        |
| bots	               | массив [PartialBot](/api/bots#ResourceBot)     | Боты пользователя	          |
| 	servers	           | 	[PartialServer](/api/servers/#ResourceServer) | Сервера пользователя	       |
| 	socials?	          | объект [UserLinkTypes](#UserLinkTypes)         | Ссылки пользователя		       |
| 	description?	      | строка                                         | Описание профиля            |
| 	shortDescription?	 | строка	                                        | Короткое профиля	           |
| 	status?	           | строка	                                        | Статус пользователя	        |
| 	shortDomain?	      | строка                                         | Короткая ссылка	            |

  
---

## UserBadge

Знак профиля

| 	Поле	     | 	Тип			 | 	Описание	       |
|------------|---------|------------------|
| 	id	       | 	число	 | 	ID значка       
| name	      | строка  | Название значка  
| 	assetURL	 | строка  | Ссылка на иконку |

## UserLinkTypes

Тип ссылки

| Код	 | 	Имя	      | 	Описание	               |
|------|------------|--------------------------|
| 	0	  | 	Vk		      | 	vk.com	                 |
| 	1	  | 	Telegram	 | 	t.me	                   |
| 	2	  | 	Donate	   | Ссылка на пожертвование	 |
| 	3	  | 	Git	      | Ссылка на Git профиль	   |
| 4	   | Custom     | Своя ссылка	             |
