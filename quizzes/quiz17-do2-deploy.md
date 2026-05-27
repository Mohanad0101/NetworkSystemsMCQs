# Тест 17: DO2 Создание и развертывание серверного приложения

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/3/2-deploy/">https://koroteev.site/os/3/2-deploy/</a><br><strong>Охват:</strong> Переменные окружения, SSH/SCP, firewall, Dockerfile, контейнеры, запуск сервиса и автоматизация деплоя.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br></div>

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

<div class="quiz-question" data-correct="3">
<h4>Вопрос 1. Что означает развертывание приложения на сервере?</h4>
<div class="quiz-option" data-index="0">Только удаление Git-истории</div>
<div class="quiz-option" data-index="1">Только написание комментариев в коде</div>
<div class="quiz-option" data-index="2">Только локальное открытие файла</div>
<div class="quiz-option" data-index="3">Подготовку окружения и запуск программы так, чтобы ей могли пользоваться клиенты</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 2. Зачем разделяют окружения разработки, тестирования и production?</h4>
<div class="quiz-option" data-index="0">Чтобы открыть все порты наружу</div>
<div class="quiz-option" data-index="1">Чтобы в каждом окружении обязательно был разный исходный код</div>
<div class="quiz-option" data-index="2">Чтобы исключить использование системы контроля версий</div>
<div class="quiz-option" data-index="3">Чтобы отделить эксперименты от стабильной рабочей системы</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 3. Какие параметры обычно выносят в переменные окружения?</h4>
<div class="quiz-option" data-index="0">Секреты, адреса БД, режим запуска, порты и внешние настройки</div>
<div class="quiz-option" data-index="1">Только HTML-заголовки</div>
<div class="quiz-option" data-index="2">Имена всех функций</div>
<div class="quiz-option" data-index="3">Все комментарии кода</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 4. Почему опасно жестко записывать пароли в исходный код?</h4>
<div class="quiz-option" data-index="0">Такие данные будут недоступны при локальном запуске</div>
<div class="quiz-option" data-index="1">NAT перестанет работать</div>
<div class="quiz-option" data-index="2">Python перестанет запускаться</div>
<div class="quiz-option" data-index="3">Они могут попасть в Git-историю или публичный репозиторий</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 5. Для чего нужен firewall на сервере?</h4>
<div class="quiz-option" data-index="0">Создавать Python-зависимости</div>
<div class="quiz-option" data-index="1">Хранить Git-коммиты</div>
<div class="quiz-option" data-index="2">Изменять HTML</div>
<div class="quiz-option" data-index="3">Фильтровать сетевой трафик и открывать только необходимые порты</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 6. Какой порт обычно нужен для SSH-администрирования?</h4>
<div class="quiz-option" data-index="0">80</div>
<div class="quiz-option" data-index="1">53</div>
<div class="quiz-option" data-index="2">443</div>
<div class="quiz-option" data-index="3">22</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 7. Какой риск связан с неправильной настройкой SSH?</h4>
<div class="quiz-option" data-index="0">Невозможность использовать Docker-контейнеры на сервере</div>
<div class="quiz-option" data-index="1">Автоматическое ускорение сайта</div>
<div class="quiz-option" data-index="2">Несанкционированный удаленный доступ к серверу</div>
<div class="quiz-option" data-index="3">Автоматическое удаление образов контейнеров</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 8. Для чего используется SCP?</h4>
<div class="quiz-option" data-index="0">Для защищенного копирования файлов между локальной и удаленной машиной</div>
<div class="quiz-option" data-index="1">Для создания веток Git</div>
<div class="quiz-option" data-index="2">Для управления DNS-зонами</div>
<div class="quiz-option" data-index="3">Для запуска HTTP-запросов</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 9. Что является недостатком полностью ручного развертывания?</h4>
<div class="quiz-option" data-index="0">Оно не требует сервера</div>
<div class="quiz-option" data-index="1">Высокий риск забыть шаг и получить неповторяемый результат</div>
<div class="quiz-option" data-index="2">Оно исключает необходимость проверять результат после копирования</div>
<div class="quiz-option" data-index="3">Оно делает сетевое подключение к серверу невозможным</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 10. Как деплой через Git обычно помогает обновлять приложение?</h4>
<div class="quiz-option" data-index="0">Сервер получает новую версию из репозитория, после чего выполняются нужные команды запуска/обновления</div>
<div class="quiz-option" data-index="1">Git устанавливает системные пакеты без описания окружения</div>
<div class="quiz-option" data-index="2">Git управляет сетевой фильтрацией вместо администратора</div>
<div class="quiz-option" data-index="3">Git управляет сетевой конфигурацией сервера вместо администратора</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 11. Что фиксирует Dockerfile?</h4>
<div class="quiz-option" data-index="0">Только описание внешнего интерфейса приложения</div>
<div class="quiz-option" data-index="1">Шаги сборки окружения приложения: базовый образ, зависимости, файлы, команды и порт</div>
<div class="quiz-option" data-index="2">Историю всех DNS-запросов</div>
<div class="quiz-option" data-index="3">Только учетные данные администратора системы</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 12. Почему Docker удобен при развертывании серверных приложений?</h4>
<div class="quiz-option" data-index="0">Он упаковывает приложение с окружением и снижает расхождения между машинами</div>
<div class="quiz-option" data-index="1">Он запускает приложение без операционной системы хоста</div>
<div class="quiz-option" data-index="2">Он хранит секреты безопасно прямо в образе</div>
<div class="quiz-option" data-index="3">Он отменяет необходимость в тестировании</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 13. Чем контейнер обычно отличается от виртуальной машины?</h4>
<div class="quiz-option" data-index="0">Контейнер обычно разделяет ядро хоста и запускается легче, а виртуальная машина запускает отдельную гостевую ОС</div>
<div class="quiz-option" data-index="1">Контейнер всегда требует больше ресурсов, чем виртуальная машина</div>
<div class="quiz-option" data-index="2">Виртуальная машина не может запускать серверные приложения</div>
<div class="quiz-option" data-index="3">Контейнер используется только для хранения текстовых файлов</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 14. Что делает команда docker build в типичном процессе?</h4>
<div class="quiz-option" data-index="0">Запускает контейнер без предварительной сборки образа</div>
<div class="quiz-option" data-index="1">Собирает образ из Dockerfile</div>
<div class="quiz-option" data-index="2">Открывает порт 22</div>
<div class="quiz-option" data-index="3">Запускает GitHub Pages</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 15. Что делает команда docker run в типичном процессе?</h4>
<div class="quiz-option" data-index="0">Редактирует Vim-файл</div>
<div class="quiz-option" data-index="1">Запускает контейнер из образа</div>
<div class="quiz-option" data-index="2">Преобразует DNS в IP</div>
<div class="quiz-option" data-index="3">Создает Git-коммит</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 16. Зачем при запуске контейнера пробрасывают порт?</h4>
<div class="quiz-option" data-index="0">Чтобы закрыть приложение от всех клиентов</div>
<div class="quiz-option" data-index="1">Чтобы изменить имя Git-ветки</div>
<div class="quiz-option" data-index="2">Чтобы сервис внутри контейнера стал доступен с хоста или из сети</div>
<div class="quiz-option" data-index="3">Чтобы заменить TCP на UDP</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 17. Что должно входить в минимальный чек-лист перед публикацией приложения?</h4>
<div class="quiz-option" data-index="0">Только параметры пользовательского интерфейса</div>
<div class="quiz-option" data-index="1">Только визуальное оформление страниц приложения</div>
<div class="quiz-option" data-index="2">Только название файла</div>
<div class="quiz-option" data-index="3">Зависимости, настройки, секреты, порты, запуск сервиса, логи и безопасность</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 18. Что лучше всего описывает автоматизацию деплоя?</h4>
<div class="quiz-option" data-index="0">Отказ от повторяемых шагов сборки и запуска</div>
<div class="quiz-option" data-index="1">Случайное копирование файлов вручную</div>
<div class="quiz-option" data-index="2">Повторяемое выполнение шагов сборки, настройки и запуска с минимальным ручным вмешательством</div>
<div class="quiz-option" data-index="3">Ручное изменение файлов без фиксированного сценария запуска</div>
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
