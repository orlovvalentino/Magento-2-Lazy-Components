# Magento 2 Lazy Components

Этот подход для ленивой инициализации компонентов Magento.

В этотм подходе используется [Intersection Observer](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API).

## Installing

Для использования, достаточно :
1. заменить в вашем коде ```data-mage-init``` на ```data-mage-init-lazy```
2. добавить фаил `main-mixin.js`
3. подключить этот фаил в  `requirejs-config.js`

## Profit
1. Меньше фаилов грузится при открытии страницы. (или менше размер бандла)
2. Меньше выполнения JS кода, значит больше очков googledpeedtest

Так же можно использовать этот подход для `text/x-magento-init` скриптов. Нужно заменить `text/x-magento-init` на `text/x-magento-init-lazy`.
Добавить `scripts-mixin.js` и подключить его в `requirejs-config.js`. Но я не рекомендую исползлвать этот метод. Лучше использовать толко 'data-mage-init-lazy'.
