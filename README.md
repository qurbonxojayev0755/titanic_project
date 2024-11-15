# Проект: Анализ данных пассажиров Титаника
## Цель проекта
Исследовать, очистить и обработать данные о пассажирах Титаника, выявить ключевые факторы, влияющие на выживаемость, и визуализировать результаты.
## Этапы выполнения
<b>1. Импорт и первичный анализ данных. Exploratory Data Analysis (EDA)</b>
 • Загрузите данные из файлов train.csv, test.csv и gender_submission.csv.
 • Проведите базовое исследование структуры данных, используя методы .head(), .info() и .describe(), чтобы понять, какие столбцы содержат пропуски или выбросы.
 
<b>2. Очистка данных. Data Cleaning</b>
• Обработка пропущенных значений:
   - Столбец Age: Заполните пропуски медианным значением или средним значением в зависимости от пассажирского класса и пола.
   - Столбец Embarked: Заполните пропуски наиболее частым значением.
   - Столбец Cabin: Этот столбец может содержать много пропусков, поэтому можно либо оставить только первую букву каюты, либо удалить столбец полностью.
   - Столбец Fare: Проверьте наличие пропущенных значений и заполните их медианным значением.
 • Обработка выбросов:
   - Проверьте значения в столбцах Age и Fare на наличие аномально высоких или низких значений и решите, что с ними делать.
Embarked: обозначает порт, из которого пассажир сел на борт корабля.
C — Cherbourg (Шербур)
Q — Queenstown (Куинстаун)
S — Southampton (Саутгемптон)

<b>3. Создание новых признаков. Feature Engineering</b>
• Извлеките титул пассажира из столбца Name и создайте новый признак Title, который может повлиять на выживаемость.
 • Создайте признак FamilySize на основе количества родственников на борту (SibSp и Parch).
 • Создайте бинарный признак IsAlone, указывающий, путешествовал ли пассажир один.
<b>4. Анализ и визуализация данных. Data Visualization</b>
• Проведите анализ факторов, влияющих на выживаемость, с помощью следующих визуализаций:
   - Гистограмма выживаемости (Survived): Покажите распределение выживания по категориям (выжил / не выжил).
   - Гистограмма распределения возраста (Age): Покажите распределение возраста среди выживших и не выживших.
   - Диаграмма размаха (boxplot) для стоимости билета (Fare): Показать разброс стоимости билета в зависимости от класса (Pclass) и статуса выживаемости.
   - Столбчатая диаграмма по классу и полу (Pclass, Sex): Сравните процент выживших в разных классах для мужчин и женщин.
   - Групповая столбчатая диаграмма (barplot) для FamilySize и выживаемости: Показать влияние размера семьи на выживаемость.
   - Круговая диаграмма для пункта отправления (Embarked): Показать процент выживших и не выживших для каждого пункта отправления.
   - Диаграмма рассеяния (scatterplot): Показать взаимосвязь между возрастом и стоимостью билета, используя цвет для обозначения выживаемости (Survived).
   - Тепловая карта корреляций (heatmap): Постройте корреляционную матрицу для количественных переменных, чтобы выявить взаимосвязи между различными признаками.
<b>5. Сортировка и группировка данных. Data Aggregation & Grouping</b>
• Выполните группировку по таким признакам, как Pclass, Sex, Embarked и FamilySize, чтобы изучить средний показатель выживаемости для каждой группы.
 • Используйте группировку и сортировку для анализа зависимости между стоимостью билета и классом (Pclass), а также между размером семьи и выживаемостью.
<b>6. Подготовка отчета. Report Preparation</b>
• Оформите краткий отчет о проделанной работе с описанием подходов к очистке и обработке данных, выводами по визуализациям и выявленным факторам, влияющим на выживаемость пассажиров.
Результат
Ваш проект должен включать:
 • Очищенные данные.
 • Набор визуализаций, показывающих ключевые зависимости и выводы.
 • Описание проделанных шагов и краткий анализ результатов.
# Project: Titanic Passenger Data Analysis
## Project Goal
The goal of this project is to explore, clean, and process Titanic passenger data, identify key factors influencing survival, and visualize the findings.
Project Steps
<b>1. Exploratory Data Analysis (EDA)</b>
• Import data from train.csv, test.csv, and gender_submission.csv files.
 • Perform initial exploration using .head(), .info(), and .describe() to understand data structure, check for missing values, and get a basic statistical overview.
<b>2. Data Cleaning</b>
• Handling Missing Values:
   - Age: Fill missing values with the median or mean based on passenger class and gender.
   - Embarked: Fill missing values with the most frequent value.
   - Cabin: Consider using only the first letter of the cabin or removing the column if it has limited analytical value.
   - Fare: Check for missing values and fill them with the median.

 • Outlier Treatment:
   - Identify potential outliers in Age and Fare, and determine appropriate handling (e.g., capping values or excluding outliers).
<b>3. Feature Engineering</b>
• Extract passenger titles from the Name column and create a new feature (Title) to see its impact on survival.
 • Create a FamilySize feature based on the number of relatives onboard (SibSp and Parch).
 • Add a binary feature, IsAlone, indicating whether a passenger traveled alone.
<b>4. Data Visualization</b>
• Perform analysis on survival factors using the following visualizations:
   - Survival Histogram: Display the distribution of survivors vs. non-survivors.
   - Age Distribution Histogram: Show age distribution among survivors and non-survivors.
   - Box Plot of Fare by Class and Survival: Show Fare spread across classes and survival status.
   - Bar Chart for Class and Gender (Pclass, Sex): Compare survival rates across classes for males and females.
   - Grouped Bar Chart for FamilySize and Survival: Show the impact of family size on survival.
   - Pie Chart for Embarked: Display the survival and non-survival percentages by embarkation point.
   - Scatter Plot: Display the relationship between Age and Fare, with color indicating survival status.
   - Correlation Heatmap: Create a correlation matrix for numerical variables to uncover relationships between features.
<b>5. Data Aggregation & Grouping</B>
• Group data by features like Pclass, Sex, Embarked, and FamilySize to analyze average survival rates within each group.
 • Use grouping and sorting to analyze relationships between ticket price and class (Pclass) as well as between family size and survival.
<b>6. Report Preparation</b>
• Prepare a concise report on the data cleaning and processing approach, visualization insights, and key factors affecting passenger survival.
Summary
The project deliverables should include:
 • Cleaned data.
 • Set of visualizations showcasing key dependencies and findings.
 • Description of steps taken and a brief analysis of the results.


