Документація для Налаштування Вебсайту "DRIVE Auto Dealership"

Вітаю! Цей посібник містить чіткі інструкції щодо редагування та фіналізації вашого преміального шаблону "DRIVE Auto Dealership" перед його передачею кінцевому клієнту.

Усі зміни вносяться безпосередньо у файл index.html.

1. Персоналізація Контенту та Бренда

Ці кроки стосуються заміни мок-даних на реальну інформацію від клієнта.

1.1. Кольорова Схема (Золотий Акцент)

Щоб змінити золотий акцент на інший колір (наприклад, червоний або сріблястий), змініть лише один рядок у секції <script> у <head>:

Знайдіть:

'accent-gold': '#ffbf00', /* Gold accent */


Дія: Замініть #ffbf00 (HEX-код золотого) на новий HEX-код кольору, щоб він застосувався до всіх кнопок, заголовків та акцентів.

1.2. Оновлення Тексту та Заголовків

Назва (Title): Змініть текст у тегу <title> на назву автосалону клієнта.

Секція Hero: Оновіть головний заголовок (<h1>) та підзаголовок (<p>) на унікальний маркетинговий текст клієнта.

1.3. Секція Featured Models (Інвентар)

Кожна картка автомобіля має містити актуальні дані:

Зображення-Заглушки: Замініть URL у тегу <img> на реальні фотографії автомобілів клієнта.

<img src="[https://placehold.co/600x400/262d3a/FFFFFF?text=Sports+Sedan](https://placehold.co/600x400/262d3a/FFFFFF?text=Sports+Sedan)" 
     alt="Sports Sedan" 
     class="w-full h-48 object-cover object-center">



Дані: Оновіть модель, опис, ціну та статус (New/Pre-Owned):

<h3 class="text-xl font-bold mb-2 text-accent-gold">Sportiva S-500</h3>
<p class="text-gray-400 mb-4 text-sm">High performance and flawless style. 0-60 mph in 4.0 seconds.</p>
<span class="text-2xl font-extrabold text-white">$95,000</span>



2. Фіналізація та Передача Клієнту (Продаж)

Ці кроки гарантують, що сайт є повністю власністю клієнта і не містить вашої робочої атрибуції.

2.1. Видалення Вашої Атрибуції у Футері

Видаливши цей елемент, ви робите сайт "чистим" для продажу. Ваша професійна атрибуція в коментарях (Author/Developer: Vladyslav Baklytskyi) залишається у коді, підтверджуючи ваше авторство.

Знайдіть рядок у секції <footer>:

<!-- Custom Attribution Line (Client instructions: REMOVE this line or replace with client's business name after sale) -->
<p class="mt-1 text-sm text-accent-gold">--- REMOVE THIS LINE OR REPLACE WITH CLIENT'S NAME ---</p>



Дія: Видаліть увесь цей блок <p> повністю, або замініть текст на назву компанії клієнта.

2.2. Підключення Форми Контактів (Критично)

Форма "Get in Touch" зараз лише імітує відправку, але не надсилає реальні листи. Для клієнта це має бути функціонально!

Рекомендований метод: Використання Formspree

Створіть URL для форми клієнта на Formspree (наприклад, https://formspree.io/f/xyza123).

Знайдіть тег <form> у секції #contact.

Видаліть з тегу атрибут onsubmit="handleFormSubmit(event)"

Додайте атрибут action та method="POST":

<form id="contact-form" method="POST" action="[https://formspree.io/](https://formspree.io/)">
    <!-- Поля форми залишаються незмінними -->
    ...
</form>



Дія: Видаліть функцію handleFormSubmit та увесь тег <script> у кінці файлу, оскільки Formspree обробляє відправку самостійно.
