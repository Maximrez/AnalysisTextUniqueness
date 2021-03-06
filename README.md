# Название: AnalysisTextUniqueness

### Задача: Разработка программы проверки текста на заимствования.

Расстояние Жаккарда, используемое для нахождения сходств в текстах, подразумевает двустороннее вхождение, что не совсем
подходит для нашей задачи. Заимствованность предложения в программе определяется как частное числа элементов пересечения
множеств мешков слов исходного предложения и текста найденной страницы и количества уникальных слов в исходном предложении. 

#### Описание работы программы:
1. Запуск программы с подачей названия файла в качестве аргумента или в стандартном вводе
2. Открытие файла и чтение (доступны форматы .txt и .pdf с помощью библитеки pdfminer), обработка возможных ошибок (неправильное название,
отсутствие файла)
3. Обработка текста, разделение на предложения, разделение на слова с помощью библиотеки NLTK
4. Поиск предложений, число уникальных слов в которых больше 7, в Google через RapidAPI, сопровождающийся
выводом прогресса в стандартный вывод
5. Определение заимствованности предложения в найденных страницах с помощью описанного ранее алгоритма
6. Вывод результатов работы программы: наиболее заимствованных предложений, наиболее используемых ссылок,
всех предложений с указанием их заимствованности и ссылки на ресурс
7. Запись результатов работы программы в файл с названием название исходного файла + _result в директорию расположения
исходного файла

#### Результаты:
В директории data есть файл с текстом referat_history.txt и результат работы программы на этом файле
result_referat_history.txt

Выявлена следующая метрика работы программы:
менее 50% - низкая заимствованность;
от 50 до 85% - средняя заимствованность;
более 85% - высокая заимствованность.

#### Возможности доработки:
1. Расширение списка читаемых форматов (doc, docx)
2. Вывод результатов программы с использованием графических элементов
3. Усовершенствование алгоритма для более точного определения заимствованности
