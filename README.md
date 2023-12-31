# forecasting-model-optimal-oil-region
# Описание проекта:
Добывающая компания «ГлавРосГосНефть» предоставила пробы нефти в трёх регионах и характеристики для каждой скважины в регионе.
Нужно решить, где бурить новую скважину.

# Условия поставленной задачи:
Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).
При разведке региона исследуют 500 точек, из которых с помощью машинного обучения выбирают 200 лучших для разработки.
Бюджет на разработку скважин в регионе — 10 млрд рублей.
При нынешних ценах один баррель сырья приносит 450 рублей дохода. Доход с каждой единицы продукта составляет 450 тыс. рублей, поскольку объём указан в тысячах баррелей.
После оценки рисков нужно оставить лишь те регионы, в которых вероятность убытков меньше 2.5%. Среди них выбирают регион с наибольшей средней прибылью.

# Цель:
Необходимо построитть модель для определения региона, где добыча принесёт наибольшую прибыль.
Проанализировать возможную прибыль и риски.

# Шаги для выбора локации:
- Отпределяют регионы, собирают характеристики для скважин: качество нефти и объём её запасов;
- Посторим модель для предсказания объёма запасов в новых скважинах;
- Выбираем скважины с самыми высокими оценками значений;
- Определяем регион с максимальной суммарной прибылью отобранных скважин и минальным риском получить убыток.

# План работы

1  Изучение данных и подготовка к работе

1.1  Переменные константы и функции

1.2  Общая информация о датасетах и данных

1.3  Подготовка данных к работе

2  Обучение и проверка модели линейной регрессии для каждого региона.

3  Подготовка данных к расчёту прибыли

4  Расчёта прибыли по выбранным скважинам и предсказаным моделями запасами

5  Риски и прибыль для каждого региона

6  Итоги

# Итоги

Расчитали прибыль и риски по каждому региону, выбрали подходящий регион.

В работе использовали технику Bootstrap с 1000 выборок, чтобы найти распределение прибыли. Расчитали среднюю прибыль по переборам в регионах, 95%-й доверительный интервал и риск убытков.

Расчеты показали, что единственный регион, где вероятность убытков ниже, чем допустимое значение 2,5% - второй (вероятность убытков 1%). Он показывает самый узкий доверительный интервал (от 92.446962 до 917.910278 млн.руб) и самую высокую средняю прибыль (508.285688 млн.руб). В доверительный интервал переборы с убытком не попадают.
