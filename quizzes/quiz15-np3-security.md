# Тест 15: NP3 Безопасность сетевых приложений

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/4/3-security/">https://koroteev.site/os/4/3-security/</a><br><strong>Охват:</strong> Симметричное и асимметричное шифрование, TLS, сертификаты, подписи, хэширование и защита секретов.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br><strong>Версия:</strong> v6 — только ключевые и информативные вопросы.</div>

<style>
.quiz-container { max-width: 900px; margin: 0 auto; }
.quiz-question { background: #f8f9fa; border: 1px solid #e0e0e0; border-radius: 8px; padding: 20px; margin-bottom: 20px; }
.quiz-question h4 { margin-top: 0; color: #333; }
.quiz-option { display: block; padding: 11px 15px; margin: 8px 0; background: #fff; border: 2px solid #ddd; border-radius: 6px; cursor: pointer; transition: all 0.2s; line-height: 1.45; }
.quiz-option:hover { border-color: #3F51B5; background: #f0f2ff; }
.quiz-option.selected { border-color: #3F51B5; background: #e8eaf6; }
.quiz-option.correct { border-color: #2e7d32 !important; background: #e8f5e9 !important; color: #1b5e20; font-weight: 600; }
.quiz-option.correct::before { content: "✓ "; font-weight: 700; }
.quiz-option.wrong { border-color: #c62828 !important; background: #ffebee !important; color: #b71c1c; font-weight: 600; }
.quiz-option.wrong::before { content: "✗ "; font-weight: 700; }
.quiz-option.disabled { pointer-events: none; cursor: default; }
.quiz-score { text-align: center; padding: 20px; background: #e8eaf6; border-radius: 8px; margin-top: 30px; display: none; }
.quiz-score h3 { margin-top: 0; color: #3F51B5; }
.quiz-btn { display: inline-block; margin: 30px 8px 0; padding: 12px 28px; background: #3F51B5; color: #fff; border: none; border-radius: 6px; font-size: 16px; cursor: pointer; }
.quiz-btn:hover { background: #303f9f; }
.quiz-btn.secondary { background: #607D8B; }
.quiz-btn.secondary:hover { background: #455A64; }
.quiz-meta { margin: 12px 0 24px; color: #555; font-size: 14px; }
.quiz-learning-note { padding: 10px 14px; margin: 0 0 18px; border-left: 4px solid #3F51B5; background: #f3f5ff; color: #333; border-radius: 4px; }
</style>

<div class="quiz-container">

<div class="quiz-question" data-correct="0">
<h4>Вопрос 1. Что является основной целью шифрования в сетевой безопасности?</h4>
<div class="quiz-option" data-index="0">Сделать данные непонятными для посторонних без нужного ключа</div>
<div class="quiz-option" data-index="1">Заменить IP-адреса MAC-адресами</div>
<div class="quiz-option" data-index="2">Ускорить маршрутизацию пакетов</div>
<div class="quiz-option" data-index="3">Удалить необходимость в протоколах</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 2. Чем симметричное шифрование отличается от асимметричного?</h4>
<div class="quiz-option" data-index="0">Асимметричное работает только без сети</div>
<div class="quiz-option" data-index="1">В симметричном используются только открытые ключи</div>
<div class="quiz-option" data-index="2">Симметричное используется только для DNS</div>
<div class="quiz-option" data-index="3">В симметричном один общий секретный ключ, в асимметричном пара открытый/закрытый ключ</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 3. Почему симметричное шифрование часто применяют для передачи основного объема данных?</h4>
<div class="quiz-option" data-index="0">Оно обычно быстрее асимметричного</div>
<div class="quiz-option" data-index="1">Оно работает только с HTML</div>
<div class="quiz-option" data-index="2">Оно используется для назначения IP-адресов клиентам</div>
<div class="quiz-option" data-index="3">Оно не требует ключа</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 4. Какую проблему решает асимметричное шифрование в защищенном соединении?</h4>
<div class="quiz-option" data-index="0">Назначает IP-адреса вместо обмена ключами</div>
<div class="quiz-option" data-index="1">Ускоряет физический канал</div>
<div class="quiz-option" data-index="2">Удаляет необходимость в портах</div>
<div class="quiz-option" data-index="3">Помогает безопасно согласовать секрет или проверить подлинность стороны</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 5. Что нельзя раскрывать в паре асимметричных ключей?</h4>
<div class="quiz-option" data-index="0">Закрытый ключ</div>
<div class="quiz-option" data-index="1">Открытый ключ</div>
<div class="quiz-option" data-index="2">Имя протокола</div>
<div class="quiz-option" data-index="3">Алгоритм</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 6. Какую роль выполняет открытый ключ?</h4>
<div class="quiz-option" data-index="0">Используется только для удаления файлов</div>
<div class="quiz-option" data-index="1">Определяет номер транспортного порта сервера</div>
<div class="quiz-option" data-index="2">Должен храниться в секрете как пароль</div>
<div class="quiz-option" data-index="3">Может использоваться для проверки подписи или шифрования данных владельцу закрытого ключа</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 7. Что такое цифровая подпись в общем смысле?</h4>
<div class="quiz-option" data-index="0">Обычная картинка в конце письма</div>
<div class="quiz-option" data-index="1">Способ выбора IP-адреса</div>
<div class="quiz-option" data-index="2">Способ упаковки исполняемых файлов в контейнер</div>
<div class="quiz-option" data-index="3">Механизм проверки подлинности и целостности сообщения</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 8. Почему в защищенных протоколах часто используют и симметричную, и асимметричную криптографию вместе?</h4>
<div class="quiz-option" data-index="0">Асимметричная часть помогает согласовать доверие и ключи, а симметричная быстро шифрует основной поток данных</div>
<div class="quiz-option" data-index="1">Симметричная криптография используется только для проверки DNS-записей</div>
<div class="quiz-option" data-index="2">Асимметричная криптография всегда быстрее симметричной при передаче больших файлов</div>
<div class="quiz-option" data-index="3">Обе схемы нужны только для сжатия данных</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 9. Что в контексте HTTPS/TLS означает рукопожатие?</h4>
<div class="quiz-option" data-index="0">Команда Git merge</div>
<div class="quiz-option" data-index="1">Отправка HTML без заголовков</div>
<div class="quiz-option" data-index="2">Начальный обмен, где стороны согласуют параметры защиты и ключи</div>
<div class="quiz-option" data-index="3">Физическое подключение кабеля</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 10. Почему проверка сертификата сервера важна для клиента?</h4>
<div class="quiz-option" data-index="0">Она ускоряет загрузку CSS</div>
<div class="quiz-option" data-index="1">Она определяет оптимальный сетевой маршрут до сервера</div>
<div class="quiz-option" data-index="2">Она применяется только после отключения защищенного канала</div>
<div class="quiz-option" data-index="3">Она помогает убедиться, что клиент общается с нужным сервером, а не с подменой</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 11. Чем хэширование отличается от шифрования?</h4>
<div class="quiz-option" data-index="0">Хэширование работает только в браузере</div>
<div class="quiz-option" data-index="1">Хэш можно однозначно расшифровать обратно в исходные данные</div>
<div class="quiz-option" data-index="2">Хэш обычно необратим, а шифрование предполагает восстановление данных с ключом</div>
<div class="quiz-option" data-index="3">Шифрование не использует ключей</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 12. Что проверяет контроль целостности сообщения?</h4>
<div class="quiz-option" data-index="0">Что порт 80 открыт</div>
<div class="quiz-option" data-index="1">Что данные не были изменены при передаче</div>
<div class="quiz-option" data-index="2">Что сервер имеет публичный IP</div>
<div class="quiz-option" data-index="3">Что файл является изображением</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 13. Какой пример лучше всего иллюстрирует угрозу man-in-the-middle?</h4>
<div class="quiz-option" data-index="0">Злоумышленник находится между клиентом и сервером и подменяет обмен</div>
<div class="quiz-option" data-index="1">Пользователь забыл имя файла</div>
<div class="quiz-option" data-index="2">Git создал новую ветку</div>
<div class="quiz-option" data-index="3">Клиент не получил ответ из-за высокой нагрузки процессора</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 14. Почему нельзя считать шифрование единственной мерой безопасности приложения?</h4>
<div class="quiz-option" data-index="0">Оно исключает необходимость проверки прав доступа и логики приложения</div>
<div class="quiz-option" data-index="1">Оно не работает с вебом</div>
<div class="quiz-option" data-index="2">Оно защищает канал/данные, но не исправляет уязвимости авторизации, кода и конфигурации</div>
<div class="quiz-option" data-index="3">Оно заменяет настройку сетевого фильтра на сервере</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 15. Какой риск связан с хранением ключей прямо в исходном коде репозитория?</h4>
<div class="quiz-option" data-index="0">Ключи могут попасть к посторонним через историю Git или публичный доступ</div>
<div class="quiz-option" data-index="1">Репозиторий перестанет поддерживать ветки</div>
<div class="quiz-option" data-index="2">Git перестанет хранить историю</div>
<div class="quiz-option" data-index="3">Код станет быстрее</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 16. Что означает принцип минимальных привилегий?</h4>
<div class="quiz-option" data-index="0">Пароли публикуются в README</div>
<div class="quiz-option" data-index="1">Все пользователи получают root</div>
<div class="quiz-option" data-index="2">Все порты открываются наружу</div>
<div class="quiz-option" data-index="3">Компонент получает только те права, которые нужны ему для работы</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 17. Какой объект чаще всего подтверждает подлинность открытого ключа веб-сервера?</h4>
<div class="quiz-option" data-index="0">Цифровой сертификат</div>
<div class="quiz-option" data-index="1">Файл .gitignore</div>
<div class="quiz-option" data-index="2">MAC-таблица коммутатора</div>
<div class="quiz-option" data-index="3">Файл requirements.txt</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 18. Что лучше всего описывает безопасный обмен в сетевом приложении?</h4>
<div class="quiz-option" data-index="0">Конфиденциальность, целостность и аутентичность должны рассматриваться вместе</div>
<div class="quiz-option" data-index="1">Достаточно использовать любой публичный IP</div>
<div class="quiz-option" data-index="2">Достаточно отключить DNS</div>
<div class="quiz-option" data-index="3">Достаточно только скрыть номер порта</div>
</div>

<div class="quiz-actions"><button class="quiz-btn" onclick="showScore(this)">Показать результат</button><button class="quiz-btn secondary" onclick="resetQuiz(this)">Сбросить тест</button></div>
<div class="quiz-score"><h3 class="score-text"></h3><p class="score-detail"></p></div>
</div>

<script>
(function() {
  function findContainer(el) { return el.closest('.quiz-container') || document; }

  function answerOption(option) {
    var question = option.closest('.quiz-question');
    if (!question || question.classList.contains('answered')) return;

    question.classList.add('answered');
    var correct = parseInt(question.getAttribute('data-correct'), 10);
    var selected = parseInt(option.getAttribute('data-index'), 10);
    var correctOption = question.querySelector('.quiz-option[data-index="' + correct + '"]');

    question.querySelectorAll('.quiz-option').forEach(function(opt) {
      opt.classList.add('disabled');
      opt.setAttribute('aria-disabled', 'true');
    });

    option.classList.add('selected');

    if (selected === correct) {
      option.classList.add('correct');
    } else {
      option.classList.add('wrong');
      if (correctOption) correctOption.classList.add('correct');
    }
  }

  document.addEventListener('click', function(event) {
    var option = event.target.closest('.quiz-option');
    if (!option) return;
    answerOption(option);
  });

  window.showScore = function(btn) {
    var container = btn ? findContainer(btn) : document;
    var total = container.querySelectorAll('.quiz-question').length;
    var correctCount = 0;
    container.querySelectorAll('.quiz-question').forEach(function(q) {
      var correct = parseInt(q.getAttribute('data-correct'), 10);
      var selected = q.querySelector('.quiz-option.selected');
      if (selected && parseInt(selected.getAttribute('data-index'), 10) === correct) correctCount++;
    });
    var scoreDiv = container.querySelector('.quiz-score');
    var scoreText = container.querySelector('.score-text');
    var scoreDetail = container.querySelector('.score-detail');
    if (!scoreDiv || !scoreText || !scoreDetail) return;
    scoreDiv.style.display = 'block';
    scoreText.textContent = 'Ваш результат: ' + correctCount + ' из ' + total;
    var pct = Math.round(correctCount / total * 100);
    if (pct >= 90) scoreDetail.textContent = 'Отлично. Материал усвоен уверенно.';
    else if (pct >= 70) scoreDetail.textContent = 'Хорошо. Есть отдельные темы для повторения.';
    else if (pct >= 50) scoreDetail.textContent = 'Удовлетворительно. Рекомендуется повторить основные понятия главы.';
    else scoreDetail.textContent = 'Рекомендуется повторить главу и пройти тест еще раз.';
    scoreDiv.scrollIntoView({ behavior: 'smooth' });
  };

  window.resetQuiz = function(btn) {
    var container = btn ? findContainer(btn) : document;
    container.querySelectorAll('.quiz-question').forEach(function(q) {
      q.classList.remove('answered');
      q.querySelectorAll('.quiz-option').forEach(function(opt) {
        opt.classList.remove('selected', 'correct', 'wrong', 'disabled');
        opt.removeAttribute('aria-disabled');
      });
    });
    var score = container.querySelector('.quiz-score');
    if (score) score.style.display = 'none';
    container.scrollIntoView({ behavior: 'smooth' });
  };
})();
</script>