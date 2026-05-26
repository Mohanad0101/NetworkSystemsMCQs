# Тест 14: NP2 Асинхронное программирование

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/4/2-async/">https://koroteev.site/os/4/2-async/</a><br><strong>Охват:</strong> Потоки, процессы, GIL, race condition, deadlock, синхронизация, asyncio и event loop.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br><strong>Версия:</strong> v6 — только ключевые и информативные вопросы.</div>

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
<h4>Вопрос 1. Что называется блокировкой потока?</h4>
<div class="quiz-option" data-index="0">Ситуация, когда выполнение останавливается в ожидании медленной операции ввода-вывода или другого события</div>
<div class="quiz-option" data-index="1">Компиляция Python-кода в байт-код</div>
<div class="quiz-option" data-index="2">Удаление потока из операционной системы</div>
<div class="quiz-option" data-index="3">Состояние, когда поток ожидает завершения вычисления другого потока</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 2. Откуда часто берется прирост производительности в сетевых многозадачных программах?</h4>
<div class="quiz-option" data-index="0">Операционная система увеличивает частоту процессора для каждого потока</div>
<div class="quiz-option" data-index="1">TCP перестает проверять ошибки</div>
<div class="quiz-option" data-index="2">Процессор начинает выполнять один поток быстрее частоты</div>
<div class="quiz-option" data-index="3">Ожидание ввода-вывода одного клиента перекрывается работой с другими клиентами</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 3. Чем процесс отличается от потока?</h4>
<div class="quiz-option" data-index="0">Поток имеет отдельное адресное пространство, как самостоятельный процесс</div>
<div class="quiz-option" data-index="1">Процесс имеет более изолированную память, потоки одного процесса разделяют память</div>
<div class="quiz-option" data-index="2">Поток не использует стек</div>
<div class="quiz-option" data-index="3">Процесс не может выполнять код</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 4. Почему общая память потоков одновременно удобна и опасна?</h4>
<div class="quiz-option" data-index="0">Она исключает необходимость контролировать доступ к общим данным</div>
<div class="quiz-option" data-index="1">Она делает все операции атомарными</div>
<div class="quiz-option" data-index="2">Она упрощает обмен данными, но может вызывать гонки при одновременном доступе</div>
<div class="quiz-option" data-index="3">Она полностью исключает ошибки</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 5. Что такое race condition?</h4>
<div class="quiz-option" data-index="0">Способ установки Linux</div>
<div class="quiz-option" data-index="1">Успешное завершение всех потоков</div>
<div class="quiz-option" data-index="2">Тип DNS-запроса</div>
<div class="quiz-option" data-index="3">Ошибка, когда результат зависит от непредсказуемого порядка выполнения потоков</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 6. Что такое deadlock?</h4>
<div class="quiz-option" data-index="0">Команда Git для слияния</div>
<div class="quiz-option" data-index="1">Успешное завершение процесса</div>
<div class="quiz-option" data-index="2">Взаимная блокировка, когда задачи ждут ресурсы друг друга и не могут продолжить работу</div>
<div class="quiz-option" data-index="3">Обычный timeout сокета</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 7. Для чего используется Lock в потоках?</h4>
<div class="quiz-option" data-index="0">Чтобы открыть сетевой порт</div>
<div class="quiz-option" data-index="1">Чтобы ограничить одновременный доступ к критическому ресурсу</div>
<div class="quiz-option" data-index="2">Чтобы удалить процесс</div>
<div class="quiz-option" data-index="3">Чтобы создать HTML-страницу</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 8. Какое утверждение о GIL в CPython наиболее корректно?</h4>
<div class="quiz-option" data-index="0">Он не позволяет создавать несколько потоков в программе</div>
<div class="quiz-option" data-index="1">Он ограничивает одновременное выполнение Python-байт-кода несколькими потоками, но не отменяет необходимости синхронизации</div>
<div class="quiz-option" data-index="2">Он делает все операции над общими данными атомарными</div>
<div class="quiz-option" data-index="3">Он делает все программы однопроцессными</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 9. Почему потоки в Python все равно полезны для сетевого сервера?</h4>
<div class="quiz-option" data-index="0">GIL ускоряет CPU-bound вычисления во всех потоках</div>
<div class="quiz-option" data-index="1">Во время ожидания ввода-вывода поток может освобождать выполнение для других задач</div>
<div class="quiz-option" data-index="2">Потоки заменяют маршрутизатор</div>
<div class="quiz-option" data-index="3">Потоки отключают TCP</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 10. Когда multiprocessing обычно предпочтительнее threading?</h4>
<div class="quiz-option" data-index="0">Для изменения имени хоста</div>
<div class="quiz-option" data-index="1">Для CPU-bound вычислений, где нужна параллельная работа нескольких ядер</div>
<div class="quiz-option" data-index="2">Для простой отправки одного UDP-пакета</div>
<div class="quiz-option" data-index="3">Для хранения CSS</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 11. Что такое корутина в Python asyncio?</h4>
<div class="quiz-option" data-index="0">Сетевой кабель</div>
<div class="quiz-option" data-index="1">Функция async, выполнение которой может приостанавливаться на await без блокировки всего потока</div>
<div class="quiz-option" data-index="2">Файл конфигурации Nginx</div>
<div class="quiz-option" data-index="3">Функция, которая выполняется только в отдельном процессе</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 12. Какую роль выполняет event loop в asyncio?</h4>
<div class="quiz-option" data-index="0">Планирует выполнение корутин и возобновляет их при готовности операций</div>
<div class="quiz-option" data-index="1">Хранит историю Git</div>
<div class="quiz-option" data-index="2">Компилирует Dockerfile</div>
<div class="quiz-option" data-index="3">Назначает IP-адрес</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 13. Почему asyncio хорошо подходит для большого числа сетевых ожиданий?</h4>
<div class="quiz-option" data-index="0">Оно ускоряет вычисления за счет параллельного выполнения байткода на ядрах CPU</div>
<div class="quiz-option" data-index="1">Оно гарантирует отсутствие сетевых тайм-аутов</div>
<div class="quiz-option" data-index="2">Оно обслуживает много операций ожидания без создания большого числа потоков</div>
<div class="quiz-option" data-index="3">Оно работает только с локальными файлами</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 14. Что делает ключевое слово await?</h4>
<div class="quiz-option" data-index="0">Блокирует всю операционную систему</div>
<div class="quiz-option" data-index="1">Создает новый процесс</div>
<div class="quiz-option" data-index="2">Удаляет сокет</div>
<div class="quiz-option" data-index="3">Приостанавливает текущую корутину до готовности результата и возвращает управление циклу событий</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 15. Какая ошибка типична при смешивании блокирующего кода и asyncio?</h4>
<div class="quiz-option" data-index="0">Git теряет историю</div>
<div class="quiz-option" data-index="1">Все TCP-порты закрываются</div>
<div class="quiz-option" data-index="2">Цикл событий начинает выполнять все операции параллельно на отдельных ядрах</div>
<div class="quiz-option" data-index="3">Блокирующая операция останавливает event loop и мешает другим корутинам</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 16. Какой критерий помогает выбрать между потоками, процессами и asyncio?</h4>
<div class="quiz-option" data-index="0">Только название проекта</div>
<div class="quiz-option" data-index="1">Только предпочитаемый стиль форматирования кода</div>
<div class="quiz-option" data-index="2">Тип нагрузки: I/O-bound, CPU-bound, требования к изоляции и сложность синхронизации</div>
<div class="quiz-option" data-index="3">Наличие README</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 17. Что является хорошей практикой при работе с замками?</h4>
<div class="quiz-option" data-index="0">Держать замок во время всех сетевых ожиданий</div>
<div class="quiz-option" data-index="1">Удерживать замок во всех частях программы как можно дольше</div>
<div class="quiz-option" data-index="2">Использовать замки вместо всех переменных</div>
<div class="quiz-option" data-index="3">Держать критическую секцию короткой и захватывать ресурсы в согласованном порядке</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 18. Какая ситуация типично приводит к deadlock?</h4>
<div class="quiz-option" data-index="0">Один поток завершил работу без ошибок</div>
<div class="quiz-option" data-index="1">Клиент получил HTTP 200</div>
<div class="quiz-option" data-index="2">Поток A держит ресурс 1 и ждет ресурс 2, а поток B держит ресурс 2 и ждет ресурс 1</div>
<div class="quiz-option" data-index="3">DNS успешно вернул IP-адрес</div>
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