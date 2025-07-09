---
layout: Welcome-layout
colorSchema: light
transition: slide-up
title: Self review
favicon: /public/logos/logo.png
---

<div>
  <h1 
    v-motion 
    :initial="{ x: 0, y: -20, scale: 1.2 }" 
    :enter="final" 
    class="heading mb-3">
    Self Review
  </h1>
  <h3 
    v-motion 
    :initial="{ x: 0, y: 20, scale: 1.2 }" 
    :enter="final" 
    class="heading"
  >
    Сёмкин Виталий
  </h3>
</div>

<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<style>
  .heading {
    font-size: 32px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Hard skills
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="skills" border="rounded" src="/public/img/skills.svg"
  />

  <div>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Хорошо понимаю и разбираюсь в современном стеке разработки web приложений
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Работал c основными современными фреймворками (Vue, React, Nuxt), так и с легаси кодом на Angular-1, jQuery и нативном javaScript
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Разрабатывал встраиваемые виджеты в web приложения на Preact (Такие как: формы обратной связи, внутренний чат с поддержкой)
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Внедрял microfrontend архитектуру на проектах (vite/webpack module federation)
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Занимался разработкой и поддержкой бекенда на C#
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Разрабатывал программных роботов для автоматизации
    </li>
  </div>
</div>

<style>

  .main-container {
    margin: auto 0;
    display: flex;
    align-items: center;
    gap: 40px;

    align-self: center;
  }

  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0.9);
    opacity: 0.3 !important;
  }

  .skills {
    width: 250px;
    height: 200px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Интересные кейсы
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/keyses/Product-groups.jpg"
  />
  <div
    v-motion 
    :initial="{ x: 100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      stiffness: 40,
    }}"
  >
    <h3 class="heading mb-6">
      Раздел "Группы товаров"
    </h3>
    <p class="paragraph mb-3">
      На проекте <ProLoyalty/> реализовал раздел "Группы товаров"
    </p>
    <p class="paragraph mb-3">
      В этом разделе можно создать и отредактировать группы товаров, посмотреть количество товаров, выбрать тип включающий/исключающий набор, и полную информацию о товаре.
    </p>
    <p class="paragraph">
      Сложность заключалась в том, что при редактировании используется 3 модальных окна, которые должны сохранять своё состояние при переключении между ними, а также они должны обмениваться информацией.
    </p>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .paragraph {
    font-size: 12px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Интересные кейсы
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/keyses/catalog.jpg"
  />
  <div
    v-motion 
    :initial="{ x: 100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      stiffness: 40,
    }}"
  >
    <h3 class="heading mb-6">
      Раздел "Каталог товаров"
    </h3>
    <p class="paragraph mb-3">
      На проекте <ProLoyalty/> реализовал раздел "Каталог товаров"
    </p>
    <p class="paragraph mb-3">
      В этом разделе можно посмотреть все товары, выбрать всю группу или подгруппу, а также можно выбирать одиночные товары. Производить поиск, по наименованию, коду и штрихкоду, а также сразу массово выбирать группы товаров по коду. 
    </p>
    <p class="paragraph">
      Сложность заключалась в обработке больших объёмов данных, т.к. количество товаров может составлять несколько тысяч единиц. Благодаря оптимизации, удалось повысить производительность отрисовки товаров.
    </p>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .paragraph {
    font-size: 12px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Интересные кейсы
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/keyses/Campaign.jpg"
  />
  <div
    v-motion 
    :initial="{ x: 100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      stiffness: 40,
    }}"
  >
    <h3 class="heading mb-6">
      Раздел "Кампании"
    </h3>
    <p class="paragraph mb-3">
      На проекте <ProLoyalty/> переписал и оптимизировал раздел "Редактирование Кампании"
    </p>
    <p class="paragraph">
      Полностью пересмотрел и переписал код в разделе кампании, т.к. старая версия была не оптимизирована, на каждое действие создавалось 3 дополнительных модальных окна, что в будущем могло бы повлечь проблемы с производительностью. После улучшения, есть только 1 модальное окно в котором рисуется нужный контент, это позволяет добавлять неограниченное количество действий без потери производительности.
    </p>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .paragraph {
    font-size: 12px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Интересные кейсы
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/img/keys.svg"
  />
  <div
    v-motion 
    :initial="{ x: 100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      stiffness: 40,
    }}"
  >
    <h3 class="heading mb-6">
      Переработан процесс "Авторизации"
    </h3>
    <p class="paragraph mb-2">
      После авторизации, время жизни токена хранилось на стороне клиента, необходимо было изменить данный функционал. Валидность токена проверяется на стороне сервера, поэтому при ошибке запроса валидности токена, необходимо было заново запрашивать новую пару корректных токенов.
    </p>
    <p class="paragraph mb-2">
      Сложные моменты: нужно обрабатывать параллельные запросы, чтобы при невалидном токене, запрос на получение новой пары не отправился несколько раз одновременно. 
    </p>
    <p class="paragraph">
      Решение: после ошибки запроса, остальные запросы помещаются в стек и ожидают получения нового токена. После того как токен получен все запросы продолжают выполняться 
    </p>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .paragraph {
    font-size: 14px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Интересные кейсы
</template>

<div class="main-container">
  <div
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="img__container"
  >
    <img 
      class="img" 
      border="rounded" 
      src="/public/keyses/bug.jpg"
    />
    <img 
      class="img" 
      border="rounded" 
      src="/public/keyses/bug2.jpg"
    />
  </div>
  <div
    v-motion 
    :initial="{ x: 100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      stiffness: 40,
    }}"
  >
    <h3 class="heading mb-6">
      Ошибка запроса, если нет прав доступа
    </h3>
    <p class="paragraph mb-2">
      Если у клиента нет прав доступа к какой либо странице, то при переходе на неё всегда отправлялся запрос на сервер, что некорректно.
    </p>
    <p class="paragraph mb-2">
      Добавлена валидация прав доступа для внутренних маршрутов, как например в в разделе "Клиенты"
    </p>
    <p class="paragraph">
      Благодаря доработке, при отсутствии прав запросы на сервер не отправляются
    </p>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    width: 100%;
    display: flex;
    gap: 40px;
  }

  .img__container {
    display: flex;
    width: 90%;
    align-items: center;
    flex-direction: column;
  }

  .img {
    width: 100%;
    height: 170px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .paragraph {
    font-size: 14px;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Закрытие ИПР
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/img/IPR.svg"
  />
  <div>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      За время работы в компании успешно закрыл ИПР
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Закрепил и применил основные паттерны проектирования SOLID, DRY, KISS
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Углубил знания в различных архитектурных подходах построения современных frontend приложений
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Погрузился в библиотеку ThreeJs для создания сложной анимации, рендеринга и игр
    </li>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0.9);
    opacity: 0.3 !important;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Немного статистики
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/img/statistic.svg"
  />
  <div>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      За время работы создал около 500 Merge Request
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      По статистике из Я.Трекера, закрыто более 200 задач
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Провёл более 200 ревью на <ProLoyalty />
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      В ревью вношу предложения по оптимизации производительности и упрощению кода
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Подхожу к ревью ответственно, всегда сначала погружаюсь в документацию и требование к задаче. Выявляю не только ошибки в коде, но и ошибки дизайна
    </li>
  </div>
</div>

<style>
  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0.9);
    opacity: 0.3 !important;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Командное взаимодействие
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/img/team.svg"
  />
  <div>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Всегда стараюсь помочь коллегам с любым вопросом
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Стараюсь поддерживать позитивную и спокойную атмосферу в команде
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Быстро откликаюсь и серьёзно отношусь к любым вопросам и просьбам о помощи
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      С радостью готов выслушать любую проблему и подставить плечо поддержки на созвоне 😊
    </li>
  </div>
</div>

<style>

  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0.9);
    opacity: 0.3 !important;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
Обучение и развитие
</template>

<div class="main-container">
  <img 
    v-motion 
    :initial="{ x: -100, y: 0, opacity: 0.5 }" 
    :enter="{ x: 0, y: 0, opacity: 1, transition: {
      type: 'spring',
      damping: 10,
      stiffness: 50,
      mass: 2,
    }}"
    class="product__img" 
    border="rounded" 
    src="/public/img/Learning.svg"
  />
  <div>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Постоянно изучаю новые технологии не только во frontend но и в других областях
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Стараюсь погружаться в исходный код библиотек и фреймворков, чтобы лучше понять их работу
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Смотрю на код коллег, чтобы подчерпнуть различные решения и не стесняюсь обратится к коллегам, чтобы обсудить предложенное решение. 
    </li>
    <li v-click class="slidev-vclick-target slidev-vclick-hidden">
      Самостоятельно изучал C#, Kotlin. Планирую больше погрузиться в backend разработку на nodeJs 
    </li>
  </div>
</div>

<style>

  .main-container {
    margin: auto 0;
    display: flex;
    gap: 40px;

    align-self: center;
  }

  .product__img {
    width: 65%;
    height: 300px;
  }

  .heading {
    font-size: 20px;
    font-weight: bold;
  }

  .slidev-vclick-target {
    transition: all 500ms ease;
  }

  .slidev-vclick-hidden {
    transform: scale(0.9);
    opacity: 0.3 !important;
  }
</style>

---
layout: Main-layout
transition: slide-up
---

<template #heading>
The End
</template>


<div class="container__wrapper">
  <TheEnd />
  <p class="paragraph">
    Спасибо за внимание!
  </p>
</div>

<style>
  .container__wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    gap: 30px;
  }

  .paragraph {
    font-size: 24px;
    font-weight: bold;
    align-text: center;
  }
</style>