# Тест 10: LX9 Настройка сетевой среды в Linux

<div class="quiz-meta"><strong>Источник главы:</strong> <a href="https://koroteev.site/os/2/5-network/">https://koroteev.site/os/2/5-network/</a><br><strong>Охват:</strong> IP-адресация, NAT, маршрутизация, OSI/TCP-IP, DNS/DHCP и диагностика сети.<br><strong>Формат:</strong> 18 отобранных вопросов, 4 варианта, один правильный ответ, цветовая проверка выбора.<br><strong>Версия:</strong></div>

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
<h4>Вопрос 1. Что означает частный IPv4-адрес в контексте подключения к Интернету?</h4>
<div class="quiz-option" data-index="0">Адрес, который обязательно принадлежит DNS-серверу</div>
<div class="quiz-option" data-index="1">Адрес, который маршрутизируется в глобальном Интернете без ограничений</div>
<div class="quiz-option" data-index="2">Адрес, используемый только для loopback-интерфейса</div>
<div class="quiz-option" data-index="3">Адрес из специальных диапазонов локальных сетей, обычно выходящий наружу через NAT</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 2. Какой из диапазонов относится к частным IPv4-адресам?</h4>
<div class="quiz-option" data-index="0">100.64.0.0/10</div>
<div class="quiz-option" data-index="1">224.0.0.0/4</div>
<div class="quiz-option" data-index="2">8.8.8.0/24</div>
<div class="quiz-option" data-index="3">172.16.0.0/12</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 3. Почему проверка ping до 127.0.0.1 выполняется в начале диагностики?</h4>
<div class="quiz-option" data-index="0">Она проверяет доступность шлюза провайдера</div>
<div class="quiz-option" data-index="1">Она проверяет только работу внешнего DNS</div>
<div class="quiz-option" data-index="2">Она показывает список открытых TCP-портов</div>
<div class="quiz-option" data-index="3">Она проверяет базовую работоспособность сетевого стека локальной машины</div>
</div>

<div class="quiz-question" data-correct="2">
<h4>Вопрос 4. Что в первую очередь показывает успешный ping до шлюза по умолчанию?</h4>
<div class="quiz-option" data-index="0">DNS обязательно работает корректно</div>
<div class="quiz-option" data-index="1">Веб-сервер на внешнем сайте исправен</div>
<div class="quiz-option" data-index="2">Локальная машина может связаться с маршрутизатором своей сети</div>
<div class="quiz-option" data-index="3">Все TCP-порты открыты</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 5. Почему успешный ping до 8.8.8.8 и неуспешный ping до доменного имени указывают на вероятную DNS-проблему?</h4>
<div class="quiz-option" data-index="0">IP-связность есть, а преобразование имени в IP не работает</div>
<div class="quiz-option" data-index="1">Локальный сетевой интерфейс выключен</div>
<div class="quiz-option" data-index="2">ICMP полностью заблокирован</div>
<div class="quiz-option" data-index="3">Маршрутизатор не включен</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 6. Какая операция используется для определения адреса сети по IP-адресу и маске?</h4>
<div class="quiz-option" data-index="0">Сложение IP-адреса и номера порта</div>
<div class="quiz-option" data-index="1">Сравнение MAC-адресов</div>
<div class="quiz-option" data-index="2">Логическое ИЛИ между IP-адресом и шлюзом</div>
<div class="quiz-option" data-index="3">Логическое И между IP-адресом и маской</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 7. К какой сети относятся адреса 192.168.1.29/24 и 192.168.1.9/24?</h4>
<div class="quiz-option" data-index="0">К публичной сети провайдера</div>
<div class="quiz-option" data-index="1">К одной сети 192.168.1.0/24</div>
<div class="quiz-option" data-index="2">К сети 192.168.0.0/16 только для первого адреса</div>
<div class="quiz-option" data-index="3">К разным сетям: 192.168.1.29 и 192.168.1.9</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 8. Почему адрес 10.52.9.379 некорректен как IPv4-адрес?</h4>
<div class="quiz-option" data-index="0">В нем слишком мало октетов</div>
<div class="quiz-option" data-index="1">Адрес начинается с 10</div>
<div class="quiz-option" data-index="2">В нем нет номера порта</div>
<div class="quiz-option" data-index="3">Октет 379 выходит за допустимый диапазон 0–255</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 9. Какое устройство необходимо для передачи пакетов между разными IP-сетями?</h4>
<div class="quiz-option" data-index="0">Коммутатор уровня 2</div>
<div class="quiz-option" data-index="1">Концентратор</div>
<div class="quiz-option" data-index="2">Пассивный патч-панель</div>
<div class="quiz-option" data-index="3">Маршрутизатор</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 10. Что делает NAT при отправке пакета из локальной сети в Интернет?</h4>
<div class="quiz-option" data-index="0">Создает новый DNS-запрос для каждого пакета</div>
<div class="quiz-option" data-index="1">Меняет адрес отправителя на внешний адрес шлюза и запоминает соответствие</div>
<div class="quiz-option" data-index="2">Выполняет разрешение доменного имени вместо DNS</div>
<div class="quiz-option" data-index="3">Удаляет TCP-заголовок</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 11. Какое ограничение NAT в клиентской сети часто уменьшает доступность компьютера извне?</h4>
<div class="quiz-option" data-index="0">Входящие соединения из Интернета к внутреннему узлу обычно невозможны без проброса портов</div>
<div class="quiz-option" data-index="1">Нельзя использовать DNS</div>
<div class="quiz-option" data-index="2">Все исходящие соединения всегда блокируются</div>
<div class="quiz-option" data-index="3">Нельзя использовать HTTP</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 12. Почему модель TCP/IP часто удобнее при описании реальной работы Интернета, чем OSI?</h4>
<div class="quiz-option" data-index="0">Она описывает только локальные файлы</div>
<div class="quiz-option" data-index="1">Она прямо соответствует стеку реально используемых интернет-протоколов</div>
<div class="quiz-option" data-index="2">Она состоит из семи уровней и полностью совпадает с OSI</div>
<div class="quiz-option" data-index="3">Она описывает только физическую передачу сигналов</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 13. Почему доступность узла по ping не гарантирует исправность веб-сервиса?</h4>
<div class="quiz-option" data-index="0">ping проверяет ICMP-связность, а веб-сервис зависит от TCP-порта, HTTP/HTTPS и приложения</div>
<div class="quiz-option" data-index="1">ping проверяет состояние конкретного HTTP-порта</div>
<div class="quiz-option" data-index="2">ping запускает браузер на сервере</div>
<div class="quiz-option" data-index="3">ping изменяет HTML-страницу</div>
</div>

<div class="quiz-question" data-correct="1">
<h4>Вопрос 14. Что показывает таблица маршрутизации?</h4>
<div class="quiz-option" data-index="0">Историю команд терминала</div>
<div class="quiz-option" data-index="1">Правила выбора следующего узла для доставки пакетов в разные сети</div>
<div class="quiz-option" data-index="2">Содержимое DNS-кэша браузера</div>
<div class="quiz-option" data-index="3">Список пользователей Linux</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 15. Какая последовательность диагностики сети наиболее логична?</h4>
<div class="quiz-option" data-index="0">Порт 80 → переустановка ОС → loopback</div>
<div class="quiz-option" data-index="1">DNS-имя → внешний сайт → свой IP → шлюз</div>
<div class="quiz-option" data-index="2">Внешний сайт → удаление маршрута → свой IP</div>
<div class="quiz-option" data-index="3">localhost → свой IP → шлюз → внешний IP → DNS-имя</div>
</div>

<div class="quiz-question" data-correct="3">
<h4>Вопрос 16. На каких уровнях модели OSI в типичном сетевом обмене используются MAC-адрес, IP-адрес и номер порта?</h4>
<div class="quiz-option" data-index="0">MAC — транспортный уровень, IP — сеансовый уровень, порт — представительный уровень</div>
<div class="quiz-option" data-index="1">MAC — прикладной уровень, IP — физический уровень, порт — сетевой уровень</div>
<div class="quiz-option" data-index="2">Все три используются только на прикладном уровне</div>
<div class="quiz-option" data-index="3">MAC — канальный уровень, IP — сетевой уровень, порт — транспортный уровень</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 17. Какой выбор протоколов наиболее логичен для передачи файла и для видеозвонка?</h4>
<div class="quiz-option" data-index="0">Файл — TCP, видеозвонок часто использует UDP или протоколы поверх UDP</div>
<div class="quiz-option" data-index="1">Для обеих задач достаточно только службы разрешения имен</div>
<div class="quiz-option" data-index="2">Файл — UDP без контроля, видеозвонок — обязательно FTP</div>
<div class="quiz-option" data-index="3">Файл — только ICMP, видеозвонок — только ARP</div>
</div>

<div class="quiz-question" data-correct="0">
<h4>Вопрос 18. Чем в обычной локальной сети различаются функции DNS и DHCP?</h4>
<div class="quiz-option" data-index="0">DNS сопоставляет имена с адресами, DHCP выдает клиенту сетевые параметры</div>
<div class="quiz-option" data-index="1">DNS назначает адрес клиенту, а DHCP преобразует доменные имена</div>
<div class="quiz-option" data-index="2">Оба протокола делают одно и то же: передают файлы</div>
<div class="quiz-option" data-index="3">DNS выдает MAC-адрес сетевой карте, DHCP шифрует веб-страницы</div>
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
