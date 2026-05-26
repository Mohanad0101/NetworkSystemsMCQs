# Тест 11: DO0 Использование Linux для разработки

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/3/0-environment/">https://koroteev.site/os/3/0-environment/</a><br><strong>Охват:</strong> Виртуальное окружение Python, зависимости, работа с файлами, структура проекта и переносимость.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br><strong>Версия:</strong> v6 — только ключевые и информативные вопросы.</div>

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
<h4>Вопрос 1. Для чего используется виртуальное окружение Python?</h4>
<div class="quiz-option" data-index="0">Для замены интерпретатора Python на Java</div>
<div class="quiz-option" data-index="1">Для изоляции зависимостей конкретного проекта</div>
<div class="quiz-option" data-index="2">Для автоматического шифрования всех файлов</div>
<div class="quiz-option" data-index="3">Для ускорения процессора</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 2. Какую роль обычно выполняет файл requirements.txt?</h4>
<div class="quiz-option" data-index="0">Настраивает MAC-адрес компьютера</div>
<div class="quiz-option" data-index="1">Хранит историю всех коммитов Git</div>
<div class="quiz-option" data-index="2">Хранит список зависимостей проекта для повторяемой установки</div>
<div class="quiz-option" data-index="3">Описывает структуру каталогов проекта вместо зависимостей</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 3. Какая команда обычно создает виртуальное окружение стандартными средствами Python?</h4>
<div class="quiz-option" data-index="0">python -m venv venv</div>
<div class="quiz-option" data-index="1">ssh venv</div>
<div class="quiz-option" data-index="2">git init venv</div>
<div class="quiz-option" data-index="3">docker run venv</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 4. Зачем активировать виртуальное окружение перед установкой пакетов?</h4>
<div class="quiz-option" data-index="0">Чтобы удалить все глобальные пакеты</div>
<div class="quiz-option" data-index="1">Чтобы установить пакеты в системный Python по умолчанию</div>
<div class="quiz-option" data-index="2">Чтобы pip устанавливал библиотеки внутрь окружения проекта</div>
<div class="quiz-option" data-index="3">Чтобы изменить IP-адрес</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 5. Почему Vim часто изучают в курсах Linux-разработки?</h4>
<div class="quiz-option" data-index="0">Он доступен в терминале и полезен при работе на удаленных серверах</div>
<div class="quiz-option" data-index="1">Он предназначен только для графического дизайна</div>
<div class="quiz-option" data-index="2">Он компилирует Docker-образы</div>
<div class="quiz-option" data-index="3">Он предназначен только для редактирования сетевых маршрутов</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 6. Что обычно изучают в теме системного программирования на Python в рамках курса?</h4>
<div class="quiz-option" data-index="0">Только создание HTML-стилей</div>
<div class="quiz-option" data-index="1">Только разработка мобильных игр</div>
<div class="quiz-option" data-index="2">Работа со средствами ОС: файлами, папками, процессами и консольными командами</div>
<div class="quiz-option" data-index="3">Только настройка DNS у провайдера</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 7. Какой модуль Python чаще всего используют для работы с путями в современном стиле?</h4>
<div class="quiz-option" data-index="0">socket</div>
<div class="quiz-option" data-index="1">pathlib</div>
<div class="quiz-option" data-index="2">threading</div>
<div class="quiz-option" data-index="3">random</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 8. Что делает модуль os в типичном учебном файловом менеджере?</h4>
<div class="quiz-option" data-index="0">Управляет только Git-ветками</div>
<div class="quiz-option" data-index="1">Помогает работать с файловой системой и окружением ОС</div>
<div class="quiz-option" data-index="2">Создает HTML-запросы</div>
<div class="quiz-option" data-index="3">Шифрует сетевой трафик</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 9. Для чего может использоваться модуль subprocess?</h4>
<div class="quiz-option" data-index="0">Для запуска внешних программ и команд из Python</div>
<div class="quiz-option" data-index="1">Для замены всех потоков процессами</div>
<div class="quiz-option" data-index="2">Для хранения CSS-стилей</div>
<div class="quiz-option" data-index="3">Для создания DNS-зон</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 10. Почему при переносе проекта важно фиксировать зависимости?</h4>
<div class="quiz-option" data-index="0">Без списка версий проект может не запуститься или работать иначе</div>
<div class="quiz-option" data-index="1">Потому что TCP требует requirements.txt</div>
<div class="quiz-option" data-index="2">Потому что без этого невозможно открыть проект в редакторе</div>
<div class="quiz-option" data-index="3">Потому что Git не сохраняет текстовые файлы</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 11. Какой файл обычно НЕ стоит добавлять в репозиторий Python-проекта?</h4>
<div class="quiz-option" data-index="0">Исходный код .py</div>
<div class="quiz-option" data-index="1">Файл README.md</div>
<div class="quiz-option" data-index="2">Файл requirements.txt</div>
<div class="quiz-option" data-index="3">Папку venv с установленными библиотеками</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 12. Что является хорошей практикой для структуры небольшого Python-проекта?</h4>
<div class="quiz-option" data-index="0">Называть все файлы одинаково</div>
<div class="quiz-option" data-index="1">Разделять код, зависимости, документацию и тестовые данные</div>
<div class="quiz-option" data-index="2">Смешивать секреты и код</div>
<div class="quiz-option" data-index="3">Хранить все файлы в одной строке README</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 13. Что означает переносимость проекта в контексте окружения разработки?</h4>
<div class="quiz-option" data-index="0">Привязка проекта только к одному текстовому редактору</div>
<div class="quiz-option" data-index="1">Автоматическое получение публичного IP</div>
<div class="quiz-option" data-index="2">Возможность воспроизвести запуск на другой машине с минимальными ручными действиями</div>
<div class="quiz-option" data-index="3">Невозможность установки зависимостей</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 14. Почему полезно уметь работать с файлами программно?</h4>
<div class="quiz-option" data-index="0">Это используется только в играх</div>
<div class="quiz-option" data-index="1">Это нужно только для изменения настроек терминала</div>
<div class="quiz-option" data-index="2">Многие задачи автоматизации требуют обхода каталогов, чтения, записи и преобразования файлов</div>
<div class="quiz-option" data-index="3">Это отменяет необходимость в ОС</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 15. Какой риск связан с хранением абсолютных путей в коде?</h4>
<div class="quiz-option" data-index="0">Python перестанет понимать строки</div>
<div class="quiz-option" data-index="1">HTTP заменится FTP</div>
<div class="quiz-option" data-index="2">Проект может не работать на другой машине или у другого пользователя</div>
<div class="quiz-option" data-index="3">Git удалит файл</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 16. Какая команда обычно устанавливает зависимости проекта из файла requirements.txt?</h4>
<div class="quiz-option" data-index="0">pip install -r requirements.txt</div>
<div class="quiz-option" data-index="1">git commit requirements.txt</div>
<div class="quiz-option" data-index="2">docker run requirements.txt</div>
<div class="quiz-option" data-index="3">python -m venv requirements.txt</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 17. Что обычно делает команда pip freeze &gt; requirements.txt?</h4>
<div class="quiz-option" data-index="0">Записывает список установленных пакетов окружения в файл требований</div>
<div class="quiz-option" data-index="1">Удаляет виртуальное окружение</div>
<div class="quiz-option" data-index="2">Запускает Flask-сервер в production</div>
<div class="quiz-option" data-index="3">Создает новый Git-репозиторий</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 18. Почему папку виртуального окружения обычно не добавляют в Git?</h4>
<div class="quiz-option" data-index="0">Git технически не умеет хранить папки</div>
<div class="quiz-option" data-index="1">Она большая, машинно-зависимая и может быть восстановлена по requirements.txt</div>
<div class="quiz-option" data-index="2">Она нужна только для DNS-настроек</div>
<div class="quiz-option" data-index="3">Она нужна Git для хранения истории коммитов</div>
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