# Тест 16: NP4 Веб-сервер

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/4/4-web-server/">https://koroteev.site/os/4/4-web-server/</a><br><strong>Охват:</strong> HTTP/HTTPS, Nginx, виртуальные хосты, обратный прокси, Flask, статический и динамический контент.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br></div>

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

<div class="quiz-question" data-correct="1">
<h4>Вопрос 1. Какую основную функцию выполняет веб-сервер?</h4>
<div class="quiz-option" data-index="0">Маршрутизирует IP-пакеты между подсетями</div>
<div class="quiz-option" data-index="1">Принимает HTTP/HTTPS-запросы и возвращает ответы клиентам</div>
<div class="quiz-option" data-index="2">Создает Git-коммиты</div>
<div class="quiz-option" data-index="3">Компилирует Java-код</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 2. Чем веб-сервер отличается от веб-приложения?</h4>
<div class="quiz-option" data-index="0">Различие между ними не влияет на практическую работу системы</div>
<div class="quiz-option" data-index="1">Приложение работает только с MAC-адресами</div>
<div class="quiz-option" data-index="2">Веб-сервер не принимает запросы</div>
<div class="quiz-option" data-index="3">Веб-сервер обслуживает протокол и инфраструктуру, приложение формирует бизнес-логику и динамический ответ</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 3. Зачем Nginx часто ставят перед Flask-приложением?</h4>
<div class="quiz-option" data-index="0">Для обратного прокси, обслуживания статических файлов, TLS, буферизации и первичной защиты</div>
<div class="quiz-option" data-index="1">Чтобы заменить весь Python-код приложения</div>
<div class="quiz-option" data-index="2">Чтобы отменить необходимость HTTP-запросов</div>
<div class="quiz-option" data-index="3">Чтобы хранить исходный код вместо Git</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 4. Что такое виртуальный хост?</h4>
<div class="quiz-option" data-index="0">Тип Python-потока</div>
<div class="quiz-option" data-index="1">Отдельный физический компьютер</div>
<div class="quiz-option" data-index="2">Команда Git</div>
<div class="quiz-option" data-index="3">Конфигурация, позволяющая одному серверу обслуживать несколько сайтов/доменов</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 5. Как сервер обычно понимает, какой сайт открыть при нескольких доменах на одном IP?</h4>
<div class="quiz-option" data-index="0">По имени основного файла сайта на диске сервера</div>
<div class="quiz-option" data-index="1">По имени локального пользователя Linux</div>
<div class="quiz-option" data-index="2">По MAC-адресу клиента</div>
<div class="quiz-option" data-index="3">По заголовку Host в HTTP-запросе</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 6. Что такое статический контент?</h4>
<div class="quiz-option" data-index="0">Файлы, отдаваемые без генерации на стороне приложения: HTML, CSS, JS, изображения</div>
<div class="quiz-option" data-index="1">Список процессов Linux</div>
<div class="quiz-option" data-index="2">Любой TCP-пакет</div>
<div class="quiz-option" data-index="3">Страница, каждый раз собираемая из базы данных</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 7. Что такое динамический веб-контент?</h4>
<div class="quiz-option" data-index="0">Только изображение PNG</div>
<div class="quiz-option" data-index="1">Файл, который нельзя открыть</div>
<div class="quiz-option" data-index="2">Ответ, сформированный программой с учетом запроса, данных или состояния</div>
<div class="quiz-option" data-index="3">Адрес маршрутизатора</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 8. Какие основные части есть у HTTP-запроса?</h4>
<div class="quiz-option" data-index="0">Только имя пользователя</div>
<div class="quiz-option" data-index="1">Только IP и MAC</div>
<div class="quiz-option" data-index="2">Метод, путь, версия, заголовки и при необходимости тело</div>
<div class="quiz-option" data-index="3">Только бинарный ключ</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 9. Что означает код HTTP 200?</h4>
<div class="quiz-option" data-index="0">Запрос успешно обработан</div>
<div class="quiz-option" data-index="1">Ресурс не найден</div>
<div class="quiz-option" data-index="2">Требуется сменить IP</div>
<div class="quiz-option" data-index="3">Ошибка сервера</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 10. Что делает обратный прокси?</h4>
<div class="quiz-option" data-index="0">Передает только файлы с диска и не может проксировать запросы</div>
<div class="quiz-option" data-index="1">Принимает запрос от клиента и передает его внутреннему серверу приложения</div>
<div class="quiz-option" data-index="2">Компилирует Python</div>
<div class="quiz-option" data-index="3">Определяет доменное имя по FTP-соединению</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 11. Какой порт обычно используется HTTP по умолчанию?</h4>
<div class="quiz-option" data-index="0">53</div>
<div class="quiz-option" data-index="1">22</div>
<div class="quiz-option" data-index="2">25</div>
<div class="quiz-option" data-index="3">80</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 12. Какой порт обычно используется HTTPS по умолчанию?</h4>
<div class="quiz-option" data-index="0">21</div>
<div class="quiz-option" data-index="1">110</div>
<div class="quiz-option" data-index="2">443</div>
<div class="quiz-option" data-index="3">8086</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 13. Для чего используется Beautiful Soup в теме веб-парсинга?</h4>
<div class="quiz-option" data-index="0">Для создания Git-веток</div>
<div class="quiz-option" data-index="1">Для настройки firewall</div>
<div class="quiz-option" data-index="2">Для извлечения данных из HTML-структуры</div>
<div class="quiz-option" data-index="3">Для шифрования TLS</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 14. Какое ограничение важно учитывать при веб-парсинге?</h4>
<div class="quiz-option" data-index="0">Только скорость процессора</div>
<div class="quiz-option" data-index="1">Только параметры пользовательского интерфейса</div>
<div class="quiz-option" data-index="2">Правила сайта, robots.txt, нагрузку на сервер и законность использования данных</div>
<div class="quiz-option" data-index="3">Только визуальный стиль страницы без правил сайта</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 15. Почему веб-серверу полезно эффективно отдавать статические файлы?</h4>
<div class="quiz-option" data-index="0">Это удаляет необходимость в TCP</div>
<div class="quiz-option" data-index="1">Это снижает нагрузку на приложение и ускоряет ответы</div>
<div class="quiz-option" data-index="2">Это означает, что динамический контент больше не нужен</div>
<div class="quiz-option" data-index="3">Это изменяет механизм разрешения доменных имен</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 16. Что лучше всего описывает путь браузера к странице?</h4>
<div class="quiz-option" data-index="0">DNS → TCP/TLS соединение → HTTP-запрос → HTTP-ответ → отображение</div>
<div class="quiz-option" data-index="1">Vim → Python venv → rm → reboot</div>
<div class="quiz-option" data-index="2">ARP → ZIP → grep → sed</div>
<div class="quiz-option" data-index="3">Git commit → Docker build → SSH → chmod</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 17. Почему серверное приложение не всегда публикуют напрямую в Интернет?</h4>
<div class="quiz-option" data-index="0">Потому что GitHub требует Nginx</div>
<div class="quiz-option" data-index="1">Потому что приложения не умеют слушать порты</div>
<div class="quiz-option" data-index="2">Потому что приложение не может принимать HTTP-запросы напрямую</div>
<div class="quiz-option" data-index="3">Спереди нужен слой, который берет на себя TLS, статику, ограничения, проксирование и защиту</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 18. Почему Flask подходит для учебного серверного приложения?</h4>
<div class="quiz-option" data-index="0">Это замена IP-адресации</div>
<div class="quiz-option" data-index="1">Это протокол транспортного уровня</div>
<div class="quiz-option" data-index="2">Это легковесный WSGI-фреймворк, позволяющий быстро описать маршруты и ответы HTTP</div>
<div class="quiz-option" data-index="3">Это полноценная ОС для виртуализации</div>
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
