# Тест 13: NP1 Использование сокетов

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/4/1-sockets/">https://koroteev.site/os/4/1-sockets/</a><br><strong>Охват:</strong> Клиент-серверная модель, TCP/UDP-сокеты, порты, bind/listen/accept, echo-сервер и сериализация.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br>.</div>

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
<h4>Вопрос 1. Какая пара ролей лежит в основе простейшей клиент-серверной схемы?</h4>
<div class="quiz-option" data-index="0">Клиент отправляет запрос, сервер принимает его и отвечает</div>
<div class="quiz-option" data-index="1">Клиент хранит все данные сервера постоянно</div>
<div class="quiz-option" data-index="2">Оба узла только читают локальные файлы</div>
<div class="quiz-option" data-index="3">Сервер нужен только для локальных программ без сети</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 2. Что такое сокет в сетевом программировании?</h4>
<div class="quiz-option" data-index="0">Конечная точка сетевого обмена, связанная с адресом, портом и протоколом</div>
<div class="quiz-option" data-index="1">Тип виртуальной машины</div>
<div class="quiz-option" data-index="2">Файл только для изображений</div>
<div class="quiz-option" data-index="3">Файл конфигурации, в котором хранится только имя сервера</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 3. Почему для сетевого приложения недостаточно знать только IP-адрес сервера?</h4>
<div class="quiz-option" data-index="0">Нужен еще номер порта, чтобы ОС передала данные нужной программе</div>
<div class="quiz-option" data-index="1">IP-адрес сам выбирает нужную программу на сервере</div>
<div class="quiz-option" data-index="2">IP используется только в локальных файлах</div>
<div class="quiz-option" data-index="3">Порт используется вместо IP-адреса для маршрутизации между сетями</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 4. Какой протокол устанавливает соединение перед обменом данными?</h4>
<div class="quiz-option" data-index="0">ICMP</div>
<div class="quiz-option" data-index="1">TCP</div>
<div class="quiz-option" data-index="2">DNS как транспорт</div>
<div class="quiz-option" data-index="3">UDP</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 5. Что характерно для UDP-сокета?</h4>
<div class="quiz-option" data-index="0">Он требует трехстороннего рукопожатия</div>
<div class="quiz-option" data-index="1">Он гарантирует доставку и порядок сообщений так же, как TCP</div>
<div class="quiz-option" data-index="2">Он передает датаграммы без гарантии доставки и без установления соединения</div>
<div class="quiz-option" data-index="3">Он работает только с HTML</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 6. Какая последовательность действий типична для TCP-сервера?</h4>
<div class="quiz-option" data-index="0">socket → bind → listen → accept → recv/send</div>
<div class="quiz-option" data-index="1">commit → push → pull → merge</div>
<div class="quiz-option" data-index="2">ping → traceroute → nslookup → zip</div>
<div class="quiz-option" data-index="3">socket → fork → chmod → rm</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 7. Какая последовательность действий типична для TCP-клиента?</h4>
<div class="quiz-option" data-index="0">bind → listen → accept без connect</div>
<div class="quiz-option" data-index="1">socket → connect → send/recv → close</div>
<div class="quiz-option" data-index="2">chmod → chown → mount</div>
<div class="quiz-option" data-index="3">docker build → docker run → docker push</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 8. Что делает метод accept() в TCP-сервере?</h4>
<div class="quiz-option" data-index="0">Преобразует доменное имя в IP</div>
<div class="quiz-option" data-index="1">Запускает Git-коммит</div>
<div class="quiz-option" data-index="2">Ожидает входящее соединение и возвращает новый сокет клиента</div>
<div class="quiz-option" data-index="3">Удаляет порт из системы</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 9. Что лучше выбрать для надежного учебного echo-приложения, где важен гарантированный ответ?</h4>
<div class="quiz-option" data-index="0">ARP</div>
<div class="quiz-option" data-index="1">UDP</div>
<div class="quiz-option" data-index="2">ICMP</div>
<div class="quiz-option" data-index="3">TCP</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 10. Что означает потоковый характер TCP?</h4>
<div class="quiz-option" data-index="0">TCP не использует порты</div>
<div class="quiz-option" data-index="1">Данные приходят как непрерывный поток байтов, а не как готовые сообщения приложения</div>
<div class="quiz-option" data-index="2">TCP передает только текст UTF-8</div>
<div class="quiz-option" data-index="3">Каждое сообщение TCP сохраняет исходные границы отправки</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 11. Почему при передаче объектов по сокетам нужна сериализация?</h4>
<div class="quiz-option" data-index="0">Сеть передает байты, а объект нужно преобразовать в байтовое представление</div>
<div class="quiz-option" data-index="1">Сериализация заменяет сетевой протокол прикладным портом</div>
<div class="quiz-option" data-index="2">Сериализация нужна только для текстовых файлов</div>
<div class="quiz-option" data-index="3">Сокет принимает только изображения</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 12. Какой риск возникает при небезопасной десериализации данных от неизвестного клиента?</h4>
<div class="quiz-option" data-index="0">Смена MAC-адреса</div>
<div class="quiz-option" data-index="1">Отключение IP</div>
<div class="quiz-option" data-index="2">Автоматическое ускорение сервера</div>
<div class="quiz-option" data-index="3">Возможное выполнение вредоносного кода или повреждение данных</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 13. Какая особенность усложняет сервер, обслуживающий много клиентов одновременно?</h4>
<div class="quiz-option" data-index="0">Все клиенты имеют один и тот же порт назначения на своей машине</div>
<div class="quiz-option" data-index="1">HTTP не работает через TCP</div>
<div class="quiz-option" data-index="2">Один клиент может блокировать поток выполнения, пока сервер ждет данные</div>
<div class="quiz-option" data-index="3">IP-адрес сервера разрешает только одно соединение</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 14. Что означает bind('0.0.0.0', port) для сервера?</h4>
<div class="quiz-option" data-index="0">Слушать только loopback 127.0.0.1</div>
<div class="quiz-option" data-index="1">Ограничить сервер только заранее указанным внешним IP</div>
<div class="quiz-option" data-index="2">Отключить IPv4</div>
<div class="quiz-option" data-index="3">Слушать указанный порт на всех доступных сетевых интерфейсах</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 15. Почему важно закрывать сокеты после завершения обмена?</h4>
<div class="quiz-option" data-index="0">Чтобы очистить историю браузера</div>
<div class="quiz-option" data-index="1">Чтобы удалить исходный код</div>
<div class="quiz-option" data-index="2">Чтобы изменить маску подсети</div>
<div class="quiz-option" data-index="3">Чтобы освободить системные ресурсы и корректно завершить соединение</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 16. Какая комбинация обычно точнее всего определяет сетевое соединение приложения?</h4>
<div class="quiz-option" data-index="0">Только MAC-адрес сетевого адаптера клиента</div>
<div class="quiz-option" data-index="1">Только имя файла программы</div>
<div class="quiz-option" data-index="2">IP-адреса, номера портов и транспортный протокол</div>
<div class="quiz-option" data-index="3">Только объем памяти, выделенный серверному процессу</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 17. Почему в TCP-приложении нельзя считать, что один send всегда соответствует одному recv?</h4>
<div class="quiz-option" data-index="0">send и recv работают только в UDP</div>
<div class="quiz-option" data-index="1">TCP передает поток байтов, а границы сообщений должно определять приложение</div>
<div class="quiz-option" data-index="2">TCP сохраняет границы каждого прикладного сообщения</div>
<div class="quiz-option" data-index="3">recv возвращает только MAC-адрес</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 18. Что происходит, если сервер слушает порт только на 127.0.0.1?</h4>
<div class="quiz-option" data-index="0">Он доступен только с локальной машины, а не с других узлов сети</div>
<div class="quiz-option" data-index="1">Он начинает принимать только UDP без TCP</div>
<div class="quiz-option" data-index="2">Он становится доступен всем узлам локальной сети</div>
<div class="quiz-option" data-index="3">Он принимает только UDP-пакеты от внешних клиентов</div>
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
