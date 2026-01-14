<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Пополнение UC PUBG</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #1a1a2e;
      color: #ddd;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }
    header {
      background: #2e1a47;
      padding: 20px;
      text-align: center;
      font-size: 1.8em;
      font-weight: 700;
      color: #c084fc;
      letter-spacing: 1.5px;
    }
    main {
      flex: 1;
      padding: 20px;
      max-width: 900px;
      margin: 0 auto;
      width: 100%;
    }
    section {
      margin-bottom: 40px;
      background: #241d3a;
      border-radius: 8px;
      padding: 20px;
      box-shadow: 0 0 10px #6a4c93aa;
    }
    h2 {
      color: #c084fc;
      margin-bottom: 15px;
      border-bottom: 2px solid #6a4c93;
      padding-bottom: 8px;
    }
    form label {
      display: block;
      margin-bottom: 8px;
      font-weight: 600;
    }
    form input, form select, form button {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: none;
      font-size: 1em;
    }
    form input, form select {
      background: #3a2d5d;
      color: #eee;
    }
    form button {
      background-color: #9b59b6;
      color: white;
      cursor: pointer;
      font-weight: 700;
      transition: background-color 0.3s ease;
    }
    form button:hover {
      background-color: #7d3c98;
    }
    .reviews {
      max-height: 200px;
      overflow-y: auto;
      background: #2a2241;
      padding: 10px;
      border-radius: 5px;
      color: #bbb;
    }
    .review {
      margin-bottom: 15px;
      border-bottom: 1px solid #6a4c93;
      padding-bottom: 10px;
    }
    .facts ul {
      list-style: none;
      padding-left: 0;
      color: #c9a0dc;
    }
    .facts ul li {
      margin-bottom: 10px;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #2e1a47;
      color: #c084fc;
      font-size: 0.9em;
    }
  </style>
</head>
<body>

<header>Пополнение UC и Премиум PUBG</header>

<main>
  <section id="top-up">
    <h2>Пополнение UC</h2>
    <form id="topUpForm">
      <label for="region">Выберите регион</label>
      <select id="region" required>
        <option value="">-- Выберите регион --</option>
        <option value="KZ">Казахстан</option>
        <option value="US">США</option>
        <option value="EU">Европа</option>
        <option value="AS">Азия</option>
      </select>
      <label for="amount">Сумма UC</label>
      <input type="number" id="amount" min="100" max="10000" step="100" placeholder="Введите сумму UC" required />
      <button type="submit">Пополнить</button>
    </form>
    <p id="formMessage" style="color:#e74c3c;"></p>
  </section>

  <section id="premium">
    <h2>Покупка премиум аккаунтов</h2>
    <p>Здесь будет каталог с описаниями и ценами.</p>
  </section>

  <section id="reviews">
    <h2>Отзывы наших клиентов</h2>
    <div class="reviews" id="reviewsList">
      <div class="review">
        <strong>Алексей:</strong> Отличный сервис, быстро и удобно!
      </div>
      <div class="review">
        <strong>Марина:</strong> Рада, что смогла быстро пополнить UC для своего аккаунта.
      </div>
    </div>
  </section>

  <section class="facts">
    <h2>Интересные факты о PUBG</h2>
    <ul>
      <li>Первый релиз PUBG состоялся в марте 2017 года.</li>
      <li>Игра быстро стала одной из самых популярных в жанре battle royale.</li>
      <li>На пике популярности число одновременных игроков превысило 3 миллиона.</li>
      <li>В PUBG есть множество карт, каждая со своими особенностями и стратегиями.</li>
      <li>В 2019 году вышла мобильная версия PUBG Mobile, которая стала мегапопулярной в Азии.</li>
    </ul>
  </section>
</main>

<footer>© 2026 PUBG Top-Up Service. Все права защищены.</footer>

<script>
  const form = document.getElementById('topUpForm');
  const message = document.getElementById('formMessage');

  form.addEventListener('submit', (e) => {
    e.preventDefault();
    const region = form.region.value;
    const amount = form.amount.value;

    if (!region) {
      message.textContent = 'Пожалуйста, выберите регион.';
      return;
    }
    if (amount < 100 || amount > 10000) {
      message.textContent = 'Сумма должна быть от 100 до 10000 UC.';
      return;
    }
    message.style.color = '#2ecc71';
    message.textContent = `Запрос на пополнение ${amount} UC для региона ${region} принят! (Демо)`;
  });
</script>

</body>
</html>
