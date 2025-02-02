# Learning_with_a_teacher (Обучение с учителем)
## Описание проекта Интернет магазин

Интернет-магазин «В один клик» продаёт разные товары: для детей, для дома, мелкую бытовую технику, косметику и даже продукты. Отчёт магазина за прошлый период показал, что активность покупателей начала снижаться. Привлекать новых клиентов уже не так эффективно: о магазине и так знает большая часть целевой аудитории. Возможный выход — удерживать активность постоянных клиентов. Сделать это можно с помощью персонализированных предложений.

«В один клик» — современная компания, поэтому её руководство не хочет принимать решения просто так — только на основе анализа данных и бизнес-моделирования. У компании есть небольшой отдел цифровых технологий, и вам предстоит побыть в роли стажёра в этом отделе.

**Итак, вашему отделу поручили разработать решение, которое позволит персонализировать предложения постоянным клиентам, чтобы увеличить их покупательскую активность.**

Продумывать подход к решению этой задачи вам не придётся — руководитель отдела его уже сформировал:

Нужно промаркировать уровень финансовой активности постоянных покупателей. В компании принято выделять два уровня активности: «снизилась», если клиент стал покупать меньше товаров, и «прежний уровень».

Нужно собрать данные по клиентам по следующим группам:

Признаки, которые описывают коммуникацию сотрудников компании с клиентом.

Признаки, которые описывают продуктовое поведение покупателя. Например, какие товары покупает и как часто.

Признаки, которые описывают покупательское поведение клиента. Например, сколько тратил в магазине.

Признаки, которые описывают поведение покупателя на сайте. Например, как много страниц просматривает и сколько времени проводит на сайте.

Для исследования нам даны четыре датафрейма: market_file - с данными о поведении покупателя на сайте, о коммуникациях с покупателем и его продуктовом поведении; market_money - с данными о выручке, которую получает магазин с покупателя; market_time - с данными о времени (в минутах), которое покупатель провёл на сайте в течение периода и money - с данными о среднемесячной прибыли покупателя за последние 3 месяца: какую прибыль получает магазин от продаж каждому покупателю.

**ЗАДАЧИ**
1. Нужно построить модель, которая предскажет вероятность снижения покупательской активности клиента в следующие три месяца.

2. В исследование нужно включить дополнительные данные финансового департамента о прибыльности клиента: какой доход каждый покупатель приносил компании за последние три месяца.

3. Используя данные модели и данные о прибыльности клиентов, нужно выделить сегменты покупателей и разработать для них персонализированные предложения.

Выбиралась лучшая модель среди KNeighborsClassifier(), DecisionTreeClassifier(), LogisticRegression(), SVC(). Для подбора гиперпараметров моделей  использовался рандомизированный (случайный) поиск гиперпараметров с помощью RandomizedSearchCV, который является более быстродействующим по сравнению с GridSearchCV. В качестве метрики использовалась метрика ROC-AUC (Receiver Operating Characteristic - Area Under the Curve).
Была проведена оценка важности признаков для лучшей модели с помощью метода SHAP.
