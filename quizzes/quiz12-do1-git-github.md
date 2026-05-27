# Тест 12: DO1 Контроль версий: Git и GitHub

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/3/1-git/">https://koroteev.site/os/3/1-git/</a><br><strong>Охват:</strong> Коммиты, staging area, ветки, слияние, удаленные репозитории, pull request и .gitignore.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br></div>

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
<h4>Вопрос 1. Какую основную проблему решает система контроля версий?</h4>
<div class="quiz-option" data-index="0">Устанавливает все библиотеки проекта в систему</div>
<div class="quiz-option" data-index="1">Сохраняет историю изменений и позволяет возвращаться к предыдущим состояниям проекта</div>
<div class="quiz-option" data-index="2">Компилирует программу без участия разработчика</div>
<div class="quiz-option" data-index="3">Увеличивает частоту процессора</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 2. Что создает команда git init?</h4>
<div class="quiz-option" data-index="0">Виртуальное окружение Python</div>
<div class="quiz-option" data-index="1">Новый локальный Git-репозиторий в текущем каталоге</div>
<div class="quiz-option" data-index="2">Удаленный сервер GitHub</div>
<div class="quiz-option" data-index="3">Docker-контейнер</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 3. Что такое commit в Git?</h4>
<div class="quiz-option" data-index="0">Сетевой порт GitHub</div>
<div class="quiz-option" data-index="1">Зафиксированное состояние изменений с сообщением и идентификатором</div>
<div class="quiz-option" data-index="2">Только загрузка файла в браузер</div>
<div class="quiz-option" data-index="3">Случайный временный файл</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 4. Почему сообщения коммитов должны быть осмысленными?</h4>
<div class="quiz-option" data-index="0">Без них нельзя открыть терминал</div>
<div class="quiz-option" data-index="1">Git не принимает короткие сообщения</div>
<div class="quiz-option" data-index="2">Сообщение определяет права доступа к репозиторию</div>
<div class="quiz-option" data-index="3">Они помогают понять, что и зачем изменилось</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 5. Какова роль staging area?</h4>
<div class="quiz-option" data-index="0">Сохранить пароль GitHub</div>
<div class="quiz-option" data-index="1">Запустить сервер Apache</div>
<div class="quiz-option" data-index="2">Подготовить выбранные изменения к следующему коммиту</div>
<div class="quiz-option" data-index="3">Сжать Docker-образ</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 6. Какая команда показывает текущее состояние файлов в рабочем каталоге?</h4>
<div class="quiz-option" data-index="0">git status</div>
<div class="quiz-option" data-index="1">git run</div>
<div class="quiz-option" data-index="2">git server</div>
<div class="quiz-option" data-index="3">git firewall</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 7. Зачем разработчик создает отдельную ветку?</h4>
<div class="quiz-option" data-index="0">Чтобы удалить main</div>
<div class="quiz-option" data-index="1">Чтобы изменить IP-адрес компьютера</div>
<div class="quiz-option" data-index="2">Чтобы отключить историю Git</div>
<div class="quiz-option" data-index="3">Чтобы изолировать работу над новой функцией или исправлением</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 8. Что делает merge?</h4>
<div class="quiz-option" data-index="0">Удаляет удаленный репозиторий</div>
<div class="quiz-option" data-index="1">Объединяет изменения из одной ветки с другой</div>
<div class="quiz-option" data-index="2">Компилирует Python</div>
<div class="quiz-option" data-index="3">Создает сетевой сокет</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 9. Что такое remote-репозиторий?</h4>
<div class="quiz-option" data-index="0">Копия репозитория на удаленном сервере, например GitHub</div>
<div class="quiz-option" data-index="1">Процесс Linux</div>
<div class="quiz-option" data-index="2">Локальная папка venv</div>
<div class="quiz-option" data-index="3">Файл requirements.txt</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 10. Чем clone отличается от fork в типичном процессе работы с GitHub?</h4>
<div class="quiz-option" data-index="0">fork работает только без Интернета</div>
<div class="quiz-option" data-index="1">Различие между ними не влияет на практическую работу системы</div>
<div class="quiz-option" data-index="2">clone создает ветку, а fork только показывает журнал изменений</div>
<div class="quiz-option" data-index="3">clone копирует репозиторий на локальную машину, fork создает копию в аккаунте GitHub</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 11. Для чего используется pull request?</h4>
<div class="quiz-option" data-index="0">Чтобы создать виртуальную машину</div>
<div class="quiz-option" data-index="1">Чтобы предложить изменения из своей ветки или fork в исходный проект</div>
<div class="quiz-option" data-index="2">Чтобы скачать Python-библиотеки</div>
<div class="quiz-option" data-index="3">Чтобы открыть порт 80</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 12. Что делает git pull?</h4>
<div class="quiz-option" data-index="0">Отправляет изменения на сервер без проверки</div>
<div class="quiz-option" data-index="1">Получает изменения из удаленного репозитория и интегрирует их локально</div>
<div class="quiz-option" data-index="2">Удаляет ветку main</div>
<div class="quiz-option" data-index="3">Открывает браузер</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 13. Что делает git push?</h4>
<div class="quiz-option" data-index="0">Запускает веб-сервер</div>
<div class="quiz-option" data-index="1">Очищает историю коммитов</div>
<div class="quiz-option" data-index="2">Скачивает зависимости Python</div>
<div class="quiz-option" data-index="3">Отправляет локальные коммиты в удаленный репозиторий</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 14. Зачем нужен файл .gitignore?</h4>
<div class="quiz-option" data-index="0">Чтобы включить NAT</div>
<div class="quiz-option" data-index="1">Чтобы спрятать все коммиты</div>
<div class="quiz-option" data-index="2">Чтобы исключить временные, служебные, секретные и сгенерированные файлы из репозитория</div>
<div class="quiz-option" data-index="3">Чтобы запустить Docker без Dockerfile</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 15. Какой файл опасно случайно добавить в публичный репозиторий?</h4>
<div class="quiz-option" data-index="0">.env с паролями и токенами</div>
<div class="quiz-option" data-index="1">requirements.txt</div>
<div class="quiz-option" data-index="2">README.md</div>
<div class="quiz-option" data-index="3">main.py без секретов</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 16. Что обычно означает конфликт слияния?</h4>
<div class="quiz-option" data-index="0">HTTP вернул 200</div>
<div class="quiz-option" data-index="1">Git не смог автоматически объединить изменения в одном и том же участке файла</div>
<div class="quiz-option" data-index="2">Сервер потерял IP-адрес</div>
<div class="quiz-option" data-index="3">Python не нашел модуль socket</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 17. Какой рабочий процесс наиболее безопасен для новой функции?</h4>
<div class="quiz-option" data-index="0">Скопировать проект вручную в 10 папок</div>
<div class="quiz-option" data-index="1">Писать код только в ZIP-архиве</div>
<div class="quiz-option" data-index="2">Создать ветку → сделать коммиты → проверить → открыть pull request/merge</div>
<div class="quiz-option" data-index="3">Редактировать main без коммитов → удалить .git</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 18. Какие файлы особенно важно исключать через .gitignore в Python-проекте?</h4>
<div class="quiz-option" data-index="0">Только файлы с расширением .md</div>
<div class="quiz-option" data-index="1">Все файлы с текстом лекции</div>
<div class="quiz-option" data-index="2">README.md и исходные .py-файлы</div>
<div class="quiz-option" data-index="3">venv, __pycache__, .env и временные/сгенерированные файлы</div>
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
