<h2>Создание веб-сервиса: "Гостевая книга"</h2>

<p>Здравствуйте! В этом репозитории я представляю свою гостевую книгу, разработанную на PHP 8.3 и MySQL 8.2 с использованием OOP.</p>

<p>Начнем с файла <code>connect_db.php</code>, который используется в следующих файлах: <code>admin.php</code>, <code>delete.php</code>, <code>reg.php</code> и <code>send.php</code>. В этом файле описано подключение к базе данных, не забудьте указать свои данные для подключения.</p>

<p>В <code>functions.php</code> описаны классы, которые используются в файлах <code>index.php</code> и <code>reg.php</code>. В <code>index.php</code> я создаю форму, применяя свои классы <code>Main</code> и <code>CreateForm</code> из <code>functions.php</code>, а также использую файл <code>captcha.php</code> для генерации капчи.</p>

<p>Файл <code>reg.php</code> обрабатывает данные, отправленные с <code>index.php</code>, и также использует классы из <code>functions.php</code>, такие как <code>DB</code> и <code>CheckPostInput</code>. После обработки данных происходит переход либо на страницу с сообщениями <code>send.php</code>, либо на <code>admin.php</code>.</p>

<p>Чтобы перейти на <code>send.php</code>, вы можете нажать на соответствующую ссылку в шапке <code>index.php</code> или заполнить все поля и нажать кнопку <code>send</code>.</p>

<p>На странице <code>send.php</code> отображаются данные из базы данных в виде таблицы с полями: <code>text</code>, <code>username</code>, <code>email</code> и <code>date</code>. Таблица поддерживает сортировку по этим полям и включает пагинацию.</p>

<p>Для доступа к <code>admin.php</code>, администратор должен ввести в поля <code>username</code> и <code>email</code> слово <code>admin</code>. В этом файле добавляется дополнительное поле <code>actions</code>, в котором для каждой записи доступна функция <code>delete</code>, позволяющая удалить запись из таблицы и базы данных. Функция <code>delete</code> реализована в файле <code>delete.php</code>.</p>

<p>Также в репозитории присутствуют файлы <code>header.php</code> и <code>footer.php</code>, в которых описаны шапка и подвал страницы соответственно.</p>

<p>В файле <code>style.css</code> содержатся стили для различных тегов. Шрифт <code>georgia.ttf</code>, используемый в <code>captcha.php</code>, также прилагается.</p>

<p>Кроме того, я прикладываю дамп своей базы данных: <code>db_guestBook.sql</code>. При отправке данных с <code>index.php</code> в <code>reg.php</code>, помимо информации, введенной пользователем, в базе данных также сохраняются дата отправления, информация о браузере пользователя и его IP-адрес.</p>
