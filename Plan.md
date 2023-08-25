# **Планирование автоматизации тестирования комплексного сервиса по покупке тура**

## **1\. Перечень автоматизируемых сценариев**

Основные позитивные сценарии:


<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top">Название сценария</th><th colspan="1" valign="top">Шаги</th><th colspan="1" valign="top">Ожидаемый результат</th></tr>
<tr><td colspan="1" rowspan="8" valign="top">1</td><td colspan="1" rowspan="8" valign="top">Покупка тура по APPROVED карте</td><td colspan="1" valign="top">1 Зайти на страницу http://localhost:8080</td><td colspan="1" valign="top">Открывается страница «Путешествие дня»</td></tr>
<tr><td colspan="1" valign="top">2 Нажать кнопку «Купить»</td><td colspan="1" valign="top">Появляется раздел «Оплата по карте» с полями для заполнения</td></tr>
<tr><td colspan="1" valign="top">3 В поле «Номер карты» ввести: 1111 2222 3333 4444 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">4 В поле «Месяц» ввести одно из значений: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">5 В поле «Год» в формате двух последних цифр ввести значение года больше текущего до плюс 5 лет</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">6 В поле «Владелец» ввести имя и фамилию через пробел латиницей (макс. 21 символ)</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">7 В поле «CVC/CVV» ввести любое трехзначное число</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">8 Нажать кнопку «Продолжить»</td><td colspan="1" valign="top"><p>Появляется сообщение «Успешно! Операция одобрена банком».</p><p>В БД в таблице «payment_entity» появляется запись о платеже со статусом «APPROVED»</p></td></tr>
<tr><td colspan="1" rowspan="8" valign="top">2</td><td colspan="1" rowspan="8" valign="top">Покупка тура по DECLINED  карте</td><td colspan="1" valign="top">1 Зайти на страницу http://localhost:8080</td><td colspan="1" valign="top">Открывается страница «Путешествие дня»</td></tr>
<tr><td colspan="1" valign="top">2 Нажать кнопку «Купить»</td><td colspan="1" valign="top">Появляется раздел «Оплата по карте» с полями для заполнения</td></tr>
<tr><td colspan="1" valign="top">3 В поле «Номер карты» ввести: 5555 6666 7777 8888  </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">4 В поле «Месяц» ввести одно из значений: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">5 В поле «Год» в формате двух последних цифр ввести значение года больше текущего до плюс 5 лет</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">6 В поле «Владелец» ввести имя и фамилию через пробел латиницей (макс. 21 символ)</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">7 В поле «CVC/CVV» ввести любое трехзначное число</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">8 Нажать кнопку «Продолжить»</td><td colspan="1" valign="top"><p>Появляется сообщение «Ошибка! Банк отказал в проведении операции».</p><p>В БД в таблице «payment_entity» появляется запись о платеже со статусом «<a name="__ddelink__8_232159447"></a>DECLINED»</p></td></tr>
<tr><td colspan="1" rowspan="8" valign="top">3</td><td colspan="1" rowspan="8" valign="top">Покупка тура в кредит по APPROVED карте</td><td colspan="1" valign="top">1 Зайти на страницу http://localhost:8080</td><td colspan="1" valign="top">Открывается страница «Путешествие дня»</td></tr>
<tr><td colspan="1" valign="top">2 Нажать кнопку «Купить в кредит»</td><td colspan="1" valign="top">Появляется раздел «Кредит по данным карты» с полями для заполнения</td></tr>
<tr><td colspan="1" valign="top">3 В поле «Номер карты ввести»: 1111 2222 3333 4444 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">4 В поле «Месяц» ввести одно из значений: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">5 В поле «Год» в формате двух последних цифр ввести значение года больше текущего до плюс 5 лет</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">6 В поле «Владелец» ввести имя и фамилию через пробел латиницей (макс. 21 символ)</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">7 В поле «CVC/CVV» ввести любое трехзначное число</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">8 Нажать кнопку «Продолжить»</td><td colspan="1" valign="top"><p>Появляется сообщение «Успешно! Операция одобрена банком».</p><p>В БД в таблице «credit_request_entity» появляется запись о платеже со статусом «APPROVED»</p></td></tr>
<tr><td colspan="1" rowspan="8" valign="top">4</td><td colspan="1" rowspan="8" valign="top">Покупка тура в кредит по DECLINED карте</td><td colspan="1" valign="top">1 Зайти на страницу http://localhost:8080</td><td colspan="1" valign="top">Открывается страница «Путешествие дня»</td></tr>
<tr><td colspan="1" valign="top">2 Нажать кнопку «Купить в кредит»</td><td colspan="1" valign="top">Появляется раздел «Кредит по данным карты» с полями для заполнения</td></tr>
<tr><td colspan="1" valign="top">3 В поле «Номер карты ввести»: 5555 6666 7777 8888</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">4 В поле «Месяц» ввести одно из значений: 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12 </td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">5 В поле «Год» в формате двух последних цифр ввести значение года больше текущего до плюс 5 лет</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">6 В поле «Владелец» ввести имя и фамилию через пробел латиницей (макс. 21 символ)</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">7 В поле «CVC/CVV» ввести любое трехзначное число</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">8 Нажать кнопку «Продолжить»</td><td colspan="1" valign="top"><p>Появляется сообщение «Успешно! Операция одобрена банком».</p><p>В БД в таблице «credit_request_entity» появляется запись о платеже со статусом «DECLINED»</p></td></tr>
</table>


Сценарии проверки невалидных значений:

Предусловие № 1

|Шаги|Ожидаемый результат|
| :-: | :-: |
|1 Зайти на страницу http://localhost:8080|Открывается страница «Путешествие дня»|
|2 Нажать кнопку «Купить»|Появляется раздел «Оплата по карте» с полями для заполнения|

Предусловие № 2

1\. Выполняется предусловие № 1

2\. Устанавливаются валидные значения для всех полей кроме исследуемого:

|Поле|Валидное значение|
| :-: | :-: |
|Номер карты|1111 2222 3333 4444 |
|Месяц|01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11, 12 |
|Год|В формате двух последних цифр ввести значение года больше текущего до плюс 5 лет|
|Владелец|Имя и фамилия ввести через пробел латиницей (макс. 21 символ)|
|CVC/CVV|Любое трехзначное число|

Предусловие № 3\*

|Шаги|Ожидаемый результат|
| :-: | :-: |
|1 Зайти на страницу http://localhost:8080|Открывается страница «Путешествие дня»|
|2 Нажать кнопку «Купить в кредит»|Появляется раздел «Кредит по данным карты» с полями для заполнения|


Сценарии:

<table><tr><th colspan="1" valign="top"></th><th colspan="1" valign="top">Название сценария</th><th colspan="1" valign="top">Предусловие</th><th colspan="1" valign="top">Шаги</th><th colspan="1" valign="top">Ожидаемый результат</th></tr>
<tr><td colspan="1" rowspan="2" valign="top">1</td><td colspan="1" rowspan="2" valign="top">Пустое поле «Номер карты»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1 Оставить поле «Номер карты» пустым</td><td colspan="1" valign="top">Отображается пустое поле</td></tr>
<tr><td colspan="1" valign="top">2 Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">2</td><td colspan="1" rowspan="2" valign="top">Ввод номера карты с 1 значением</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 1 любую цифру</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">3</td><td colspan="1" rowspan="2" valign="top">Ввод номера карты с 15 значениями</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 15 любых цифр</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" valign="top">4</td><td colspan="1" valign="top">Ввод номера карты с 17 значениями</td><td colspan="1" valign="top">Предусловие № 1</td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 17 любых цифр</td><td colspan="1" valign="top">17-ое значение в поле «Номер карты» не отображается</td></tr>
<tr><td colspan="1" valign="top">5</td><td colspan="1" valign="top">Ввод номера карты с буквенным отображением (кириллица)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 16 любых букв на кириллице</td><td colspan="1" valign="top">Поле «Номер карты» остается пустым</td></tr>
<tr><td colspan="1" valign="top">6</td><td colspan="1" valign="top">Ввод номера карты с буквенным отображением (латиница)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 16 любых букв на латинице</td><td colspan="1" valign="top">Поле «Номер карты» остается пустым</td></tr>
<tr><td colspan="1" valign="top">7</td><td colspan="1" valign="top">Ввод номера карты со спецсимволами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 16 любых спецсимволов</td><td colspan="1" valign="top">Поле «Номер карты» остается пустым</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">8</td><td colspan="1" rowspan="2" valign="top">Пустое поле «Месяц»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  Оставить поле «Месяц» пустым</td><td colspan="1" valign="top">Отображается пустое поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">9</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Месяц» одной цифры</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Месяц» ввести одно любое значение от 0 до 9</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">10</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Месяц» двойного нулевого значения</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Месяц» ввести: 00</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат».</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">11</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Месяц» граничного значения 13</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Месяц» ввести: 13</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверно указан срок действия карты»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">12</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Месяц» двойного значения, отличного от валидных значений и невалидных граничных</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Месяц» ввести любое двойное значение большее 14</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверно указан срок действия карты»</td></tr>
<tr><td colspan="1" valign="top">13</td><td colspan="1" valign="top">Ввод месяца с 3 значениями</td><td colspan="1" valign="top">Предусловие № 1</td><td colspan="1" valign="top">1   В поле «Месяц» ввести 3 любые цифры</td><td colspan="1" valign="top">3-е значение в поле «Месяц» не отображается</td></tr>
<tr><td colspan="1" valign="top">14</td><td colspan="1" valign="top">Ввод месяца с буквенным отображением (кириллица)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Месяц» ввести 2 любые буквы на кириллице</td><td colspan="1" valign="top">Поле «Месяц» остается пустым</td></tr>
<tr><td colspan="1" valign="top">15</td><td colspan="1" valign="top">Ввод месяца с буквенным отображением (латиница)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Месяц» ввести 2 любые буквы на латинице</td><td colspan="1" valign="top">Поле «Месяц» остается пустым</td></tr>
<tr><td colspan="1" valign="top">16</td><td colspan="1" valign="top">Ввод месяца со спецсимволами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Месяц» ввести 2 любых спецсимвола</td><td colspan="1" valign="top">Поле «Месяц» остается пустым</td></tr>
<tr><td colspan="1" rowspan="3" valign="top">17</td><td colspan="1" rowspan="3" valign="top">Ввод месяца меньше текущего для текущего года</td><td colspan="1" rowspan="3" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Год» ввести текущий год</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  В поле «Месяц» ввести валидное значение месяца меньший текущего</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">3  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверно указан срок действия карты»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">18</td><td colspan="1" rowspan="2" valign="top">Пустое поле «Год»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  Оставить поле «Год» пустым</td><td colspan="1" valign="top">Отображается пустое поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">19</td><td colspan="1" rowspan="2" valign="top">Ввод года с 1 значением</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1   В поле «Номер карты» ввести 1 любую цифру</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">20</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Год» двойного нулевого значения</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Год» ввести: 00</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Истёк срок действия карты »</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">21</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Год» нижнего граничного значения</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Год» ввести значение года на единицу меньше текущего</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Истёк срок действия карты »</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">22</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Год» верхнего граничного значения</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Год» ввести значение года на 6 лет больше текущего</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение « Неверно указан срок действия карты»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">23</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «Месяц» двойного значения, отличного от валидных значений и невалидных граничных</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «Месяц» ввести любое двойное значение большее значения текущего года плюс 7 лет</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверно указан срок действия карты»</td></tr>
<tr><td colspan="1" valign="top">24</td><td colspan="1" valign="top">Ввод года с 3 значениями</td><td colspan="1" valign="top">Предусловие № 1</td><td colspan="1" valign="top">1   В поле «Год» ввести 3 любые цифры</td><td colspan="1" valign="top">3-е значение в поле «Год» не отображается</td></tr>
<tr><td colspan="1" valign="top">25</td><td colspan="1" valign="top">Ввод года с буквенным отображением (кириллица)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Год» ввести 2 любые буквы на кириллице</td><td colspan="1" valign="top">Поле «Год» остается пустым</td></tr>
<tr><td colspan="1" valign="top">26</td><td colspan="1" valign="top">Ввод года с буквенным отображением (латиница)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Год» ввести 2 любые буквы на латинице</td><td colspan="1" valign="top">Поле «Год» остается пустым</td></tr>
<tr><td colspan="1" valign="top">27</td><td colspan="1" valign="top">Ввод года со спецсимволами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Год» ввести 2 любых спецсимвола</td><td colspan="1" valign="top">Поле «Год» остается пустым</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">28</td><td colspan="1" rowspan="2" valign="top">Пустое поле «Владелец»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  Оставить поле «Номер карты» пустым</td><td colspan="1" valign="top">Отображается пустое поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Поле обязательно для заполнения»</td></tr>
<tr><td colspan="1" valign="top">29</td><td colspan="1" valign="top">Ввод владельца на кириллице</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Владелец» ввести имя и фамилию на кириллице</td><td colspan="1" valign="top">Поле «Владелец» остается пустым</td></tr>
<tr><td colspan="1" valign="top">30</td><td colspan="1" valign="top">Ввод владельца цифрами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Владелец» ввести  любые числа</td><td colspan="1" valign="top">Поле «Владелец» остается пустым</td></tr>
<tr><td colspan="1" valign="top">31</td><td colspan="1" valign="top">Ввод владельца спецсимволами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1\.   В поле «Владелец» ввести любые спецсимволы, за исключением тире</td><td colspan="1" valign="top">Поле «Владелец» остается пустым</td></tr>
<tr><td colspan="1" valign="top">32</td><td colspan="1" valign="top">Ввод граничного значения для поля «Владелец»</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «Владелец» ввести 22 символа с пробелом латиницей</td><td colspan="1" valign="top">22-е значение в поле «Владелец» не отображается</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">33</td><td colspan="1" rowspan="2" valign="top">Отсутствие пробела в поле «Владелец»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1   В поле «Владелец» ввести  имя или фамилию</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверно указан срок владелец карты»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">34</td><td colspan="1" rowspan="2" valign="top">Пустое поле «CVC/CVV»</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  Оставить поле «CVC/CVV» пустым</td><td colspan="1" valign="top">Отображается пустое поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">35</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «CVC/CVV» одной цифры</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «CVC/CVV» ввести одно любое значение от 0 до 9</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" rowspan="2" valign="top">36</td><td colspan="1" rowspan="2" valign="top">Ввод в поле «CVC/CVV» двух цифр</td><td colspan="1" rowspan="2" valign="top">Предусловие № 2</td><td colspan="1" valign="top">1  В поле «CVC/CVV» ввести одно любое значение от 10 до 99</td><td colspan="1" valign="top">Данные отображаются в поле</td></tr>
<tr><td colspan="1" valign="top">2  Нажать кнопку «Продолжить»</td><td colspan="1" valign="top">Появляется сообщение «Неверный формат»</td></tr>
<tr><td colspan="1" valign="top">37</td><td colspan="1" valign="top">Ввод кода CVC/CVV с 4 значениями</td><td colspan="1" valign="top">Предусловие № 1</td><td colspan="1" valign="top">1  В поле «CVC/CVV» ввести 4 любые цифры</td><td colspan="1" valign="top">4-е значение в поле «CVC/CVV» не отображается</td></tr>
<tr><td colspan="1" valign="top">38</td><td colspan="1" valign="top">Ввод кода CVC/CVV с буквенным отображением (кириллица)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «CVC/CVV» ввести 3 любые буквы на кириллице</td><td colspan="1" valign="top">Поле «CVC/CVV» остается пустым</td></tr>
<tr><td colspan="1" valign="top">39</td><td colspan="1" valign="top">Ввод кода CVC/CVV с буквенным отображением (латиница)</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «CVC/CVV» ввести 3 любые буквы на латинице</td><td colspan="1" valign="top">Поле «CVC/CVV» остается пустым</td></tr>
<tr><td colspan="1" valign="top">40</td><td colspan="1" valign="top">Ввод кода CVC/CVV со спецсимволами</td><td colspan="1" valign="top">Предусловие № 1 </td><td colspan="1" valign="top">1   В поле «CVC/CVV» ввести 3 любых спецсимвола</td><td colspan="1" valign="top">Поле «CVC/CVV» остается пустым</td></tr>
</table>

\* Тестовые сценарии невалидных значений для покупки тура в кредит аналогичны вышеуказанным сценариями, за исключением того, что взамен Предусловия № 1 используется Предусловие № 2.

## **2\. Перечень используемых инструментов с обоснованием выбора**

||Используемый инструмент|Обоснование выбора|
| :- | :- | :- |
|1|IntelliJ IDEA|Удобная интегрированная среда разработки|
|2|Java|Популярный объектно-ориентированный язык программирования общего назначения |
|3|JUnit5|Наиболее широко используемая среда тестирования для приложений Java |
|4|Selenide|Удобный фреймворк для автоматизированного тестирования веб-прибожений |
|5|Allure|Построение понятных отчетов автотестов с графическим отображением и скриншотами|
|6|Faker|Библиотека широкого спектра для генерации случайных данных|
|7|Loombok|Библиотека, основанная на аннотациях, позволяющая сократить шаблонный код|
|8|Gradle|Инструмент с высокой производительностью для автоматизации сборки|
|9|GitHub|Сеть для коллективной разработки IT-проектов с контролем версий|
|10|AppVeyor|Распределенный веб-сервис непрерывной интегарции для сборки и тестирования кода, расположенного на GitHub|
|11|Docker|Развертывание приложения в виде переносимых автономных контейнеров|
|12|<a name="__ddelink__11824_1623082742"></a>DBeaver|Удобная работа с СУБД|


## **3\. Перечень и описание возможных рисков при автоматизации**

1\. Отсутствие детальной информации о работе приложения.

2\. Отсутствие тестовых меток на веб-странице.

3\. Наличие бага, затрудняющего проверку других автотестов.

4\. Изменение структуры сервиса

5\. Технические неполадки.

## **4\. Интервальная оценка с учётом рисков в часах**

1\. Подготовка к тестированию: 8 часов.

2\. Тестирование: 20 часов.

3\. Подготовка отчетов: 12 часов


## **5\. План сдачи работ: когда будут проведены автотесты, результаты их проведения и отчёт по автоматизации.**

1\. Проведение автотестов: до 30.08.2023.

2\. Подготовка отчетов: до 02.09.2023.
