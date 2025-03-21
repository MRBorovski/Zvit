# Task 1
|                                       Gigachad                                                   |                                          Photo with Text                                                |                                              Gothia                                                     |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
|![Gigachad](https://github.com/MRBorovski/Workshop_1_Tihonov_Vlad/blob/main/Workshop/GIGACHAD.png)|![PWT](https://github.com/MRBorovski/Workshop_1_Tihonov_Vlad/blob/main/Workshop/Photo%20with%20text.png) |![Gothia](https://github.com/MRBorovski/Workshop_1_Tihonov_Vlad/blob/main/Workshop/Gothia%203%20(2).png) |

## 1. Аналіз вихідних файлів
### 1.	Виберіть 3 типи зображень (фотографія, скріншот, графічне зображення з текстом).

### 2.	Зафіксуйте їхній початковий розмір, формат (JPEG, PNG тощо) та вагу файлу.
|***Назва зображення***|  ***PNG***  | ***Розмір у px*** |
|----------------------|-------------|-------------------|
| GIGACHAD             |   1.1 MB    |     1250x1147     |
| Photo with text      |   144 kB    |     365x738       |
| Gothia 3             |   103 MB    |     8600x10400    |

## 2. Стиснення без втрати якості (lossless)
### 3.  Завантажте кожне зображення в Squoosh.
### 4.  Використайте формати PNG (lossless) та WebP (lossless).
### 5.  Зафіксуйте зміни у вазі файлу після кожного перетворення.
### 6.  Переконайтеся, що якість зображення залишилася незмінною.

|***Назва зображення***|  ***PNG***  |***Browser PNG (lossless)***|***WEBP (lossless)***|
|----------------------|-------------|----------------------------|---------------------|
| GIGACHAD             |  1.1 MB     |           1.23 MB          |       596 kB        |
| Photo with text      |  144 kB     |           145 kB           |       106 kB        |
| Gothia 3             |  103 MB     |           115 MB           |       68 MB         |

## 3. Стиснення з втратою якості (lossy)
### 7.  Використайте формати MozJPEG, WebP (lossy) та AVIF.
### 8.  Виконайте стиснення на рівнях якості 100%, 75% та 50%.
### 9.  Зафіксуйте зміни розміру файлу.
### 10. Визначте мінімальний рівень якості, при якому зображення залишається прийнятним.

| ***MozJPEG***  | ***100%***| ***75%*** |***50%***|***min ok quality***|
|----------------|-----------|-----------|---------|--------------------|
| GIGACHAD       |  325 kB   |  35.6 kB  | 22.8 kB |         25%        |
| Photo with text|  211 kB   |  36.3 kB  | 24.2 kB |         16%        |
| Gothia 3       |  24.3 MB  |  7.51 MB  | 4.52 MB |         25%        |

|   ***WebP***   | ***100%***| ***75%*** |***50%***|***min ok quality***|
|----------------|-----------|-----------|---------|--------------------|
| GIGACHAD       |  130 kB   |  18.7 kB  | 14.3 kB |         10%        |
| Photo with text|  69.7 kB  |  30.1 kB  | 24.7 kB |         0%         |
| Gothia 3       |  19.3 MB  |  6.11 MB  | 4.47 MB |         36%        |

|   ***AVIF***   | ***100%***| ***75%*** |***50%***|***min ok quality***|
|----------------|-----------|-----------|---------|--------------------|
| GIGACHAD       |  212 kB   |  18.5 kB  | 8.36 kB |         30%        |
| Photo with text|  61.7 kB  |  27.3 kB  | 16.0 kB |         8%         |
| Gothia 3       |    - MB   |    - MB   | 68 MB   |         21%        |

## 4. Оптимізація розміру відповідно до цільового використання
### 11. Зменшіть розмір зображень відповідно до їхнього застосування:
- Для вебу: максимальна ширина 1200 px.
- Для мобільних пристроїв: максимальна ширина 600 px.
- Для Retina-дисплеїв: створіть 2x або 3x версію зображення.
### 12. Зафіксуйте зміни у вазі файлу після кожного етапу.

|***WEBP (lossless)***|***1200 px***|***600 px***|***2x***| ***3x*** |
|---------------------|-------------|------------|--------|----------|
| GIGACHAD            |   808 kB    |   236 kB   | 2.71 MB|  5.70 MB |
| Photo with text     |   139 kB    |   139 kB   | 568 kB |  987 kB  |
| Gothia 3            |   2.12 MB   |   546 kB   | -  MB  |  -  MB   |

## 5. Візуальний аналіз та висновки
### 14.  Порівняйте вихідні та оптимізовані зображення.
### 15.  Визначте, які формати та параметри оптимізації найкраще підходять для кожного типу зображень.

|                  |                                                                                                                                      ***Порівняння вхідних та оптимізованих зображень.***                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   ***AVIF***     | На мою думку данний формат стискання погано підходить під зображення з невисокую контрастністю або ж темні зображення де багато чорного та його відтінків, а також мені не вдалося стистуи великий файл до 100% та 75%                                                                                                                     |
|   ***WebP***     | Данний метод стиснення показуе найкращі результати на мою думку, він майже не зменшує кінцеву якість картинки ні на 75% ні на 50%. Та всеж у нього є недоліки, наприклад втрата кольору на зображеннях з 1-піксельними контрастними переходами                                                                                             |
| ***MozJPEG***    | Я вважаю MozJPEG покращенною у всіх аспектах версією звичайного JPEG, адже в тестах "JPEG vs MozJPEG" останній перевершує JPEG у всьому, серед зроблених мною тестів він показав найкращі показнкики стиснення, та всеж не найкращі показники якості, часто зображення ближче до критичної відмітки втрачало в контрастності, насиченості. |

###  Які формати та параметри оптимізації найкраще підходять для кожного типу зображень?
На мою думку: 
#### 1. формат AVIF ідеально підходить для стискання файлів з текстом.
#### 2. формат WebP ідеально підходить для стискання фото та файлів з мінімальною втратою якості.
#### 3. формат MozJPEG ідеально підходить для стискання великих файлів з невеликою втратою якості, абож для максимального стиснення, ціною втати якості зображення.
