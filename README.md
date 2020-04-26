# Magento 2 Lazy Components

This is an approach to lazy loading implementation for Magento Components init.

This approach uses [Intersection Observer](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API).

## Installing

1. Replace ```data-mage-init``` with ```data-mage-init-lazy``` in your code
2. Add `main-mixin.js` to your project
3. Include it to `requirejs-config.js`


## Profit
1. Fewer files (or less bundle size) is loading when opening a page
2. Less JS-code execution, which leads to higher googlespeedtest score

You can also use this approach for `text/x-magento-init` scripts. You need to replace `text/x-magento-init` with `text/x-magento-init-lazy`, add `scripts-mixin.js` to your project and include it to `requirejs-config.js`. But I don't recommend doing that. It's better to use this approach only with 'data-mage-init-lazy'.
