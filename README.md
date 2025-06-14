# LeoTranslate

This is an add-on for the Firefox and Firefox for Android browsers that helps you translate words from your chosen language into Russian and lets you add these words to your dictionary. You can choose the source language (for example, English or Portuguese) in the settings.
 
## Installation
[Get the Firefox Add-on from AMO gallery](https://addons.mozilla.org/en-US/firefox/addon/leo-translate/)

Also you can build the add-on by yourself. The building process is described below.

### Requirements
* [Node.js 6+](https://nodejs.org/en/)

### Build the extension

All the paths are specified relatively to the root of this repository.

* First of all you need to install dependencies:
    * `npm install`
* Next, you need to translate all the vue components to plain javascript code with the command:
    * `npm run build`
* Next, you need to pack the extension into zip-file:
    * `npm run web-ext:build`


# LeoTranslate

Расширение для браузеров Firefox и Firefox for Android, которое позволяет переводить слова c Английского на Русский на web-сайтах и добавлять переводы в словарь на Lingualeo.

## Установка
[Скачать дополнение из каталога AMO](https://addons.mozilla.org/en-US/firefox/addon/leo-translate/)

Также, вы можете собрать расширение самостоятельно. Ниже описан процесс сборки расширения.

### Для сборки требуется установить:
* [Node.js 6+](https://nodejs.org/en/)

### Сборка

Все пути указаны относительно папки расширения.

* Сначала нужно установить зависимости:
    * `npm install`
* Далее выполнить сборку js-modules и транслировать *.vue файлы в js командой:
    * `npm run build`
* Далее собрать расширение в архив:
    * `npm run web-ext:build`

После выполнения этих команд, в `extension/web-ext-artifacts/` должен появиться файл расширения: `leo_translate-{Номер версии}.zip`

Чтобы установить расширение из файла, нужно подписать его в addons.mozilla.org или (не рекомендуется!) переключить в Firefox на странице about:config параметр `xpinstall.signatures.required` в `false`  
