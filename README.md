## Профили для сборки LibPortablePlus версии 21.10.02
Если захотите использовать с более новой версией сборки 91 версии, то следует взять некоторые взаимосуществующие компоненты из сборки, а не из профиля, а именно:  
`user.js` и `QuickToggleAboutConfig_Damby_ucf.js`  
В версиях Firefox от 100 корректно работать точно не будет.  
  
В ближайшее время (как лень пройдет) выложу новый профиль под текущую версию сборки.

### Профиль Native Tabs Fx
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile-ntfex_220322.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-screen.md)  
  
### Профиль Tree Style Tab
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile-tstex_220322.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-screen.md)  
  
===========================================================================  

Большая часть кнопок выведенных на панели имеют подробные подсказки.  
Наведите курсор на интересующую вас кнопку и читайте.

===========================================================================  

### NoScript
Новый стиль, намного лучше чем старый, да и старый уже не работает в текущих версиях.
Обратите внимание, что в старом стиле в `userContent_dark_addons.css` NoScript занимает три секции, следует заменить их все, а в новом стиле во всех трех секциях прописать ваш UUID NoScript. Всего пять раз.
  
```
/*------ NOSCRIPT ADDON SETTINGS AND PROMPT PAGE ------*/
@-moz-document url-prefix(moz-extension://uuid/ui/options.html),
url-prefix(moz-extension://uuid/ui/prompt.html),
url-prefix(moz-extension://uuid/ui/siteInfo.html) {
h1 {
    color: #ddd !important;
}
.flextabs__toggle[aria-expanded="true"] {
    background: #2A2A36 !important;
    color: #ddd !important;
}
.flextabs__toggle[aria-expanded="false"] {
    background: #333333 !important;
    color: #aaa !important;
}
button:not(.flextabs__toggle) {
    color: #ddd !important;
    border: none !important;
    background: #333 !important;
}
.buttons button:hover {
    background: #3F3E47 !important;
}
#presets :is(.presets input.preset + label, .customizer-controls) {
    box-shadow: 0 0 .2em transparent !important
}
.customizing input.preset:checked {
    --extra-preset-width: 0.1em !important;
    color: #fff !important;
    border-bottom: none !important;
}
.customizer-controls {
    margin: -1px 0 0 0!important;
}
}
/* ---------- NOSCRIPT ADDON POPUP ------*/
@-moz-document url-prefix(moz-extension://uuid/ui/popup.html) {
#message {
    --hilite-color: #777777 !important;
    background-color: #282828 !important;
}
body {
    margin: 0 !important;
    padding: 0 !important;
}
/* Верхняя панель */
#top {
    border-bottom: 1px solid #555 !important;
    height: 2.4em !important;
    padding: 0 0 0 0 !important;
}
#top .icon {
    width: 2em !important;
    height: 2em !important;
}
:not([data-theme="light"]) :is(input.preset, .icon) {
    filter: none !important;
}
}
/* ---------- NOSCRIPT GLOBAL ------*/
@-moz-document url-prefix(moz-extension://uuid/ui/) {
/* Пресеты */
.presets input.preset {
    width: 1.6em !important;
    height: 1.6em !important;
    margin: 0 0 0.14em 0.3em !important;
    background: rgba(30,30,30,0.2) !important; /* шапито */
    box-shadow: inset 0 1px 3px #000 !important;
    border-radius: 0 0 0 0 !important;
}
.presets input.preset:checked {
    background-color: rgba(50,50,50,0.50) !important;
    min-width: calc(var(--preset-label-width) + var(--line-size) * 1.5 + var(--extra-preset-width)) !important;
}
.presets input.preset:checked + label.preset {
    border-radius: 0 !important;
}
input.preset:checked ~ input.temp {
    height: 1.3em !important;
    top: 0.08em !important;
    right: 0.01em !important;
    margin-right: 2px !important;
    background-color: none !important;
}
.preset label.preset {
    min-width: calc(var(--preset-label-width) + var(--line-size) * 0 + var(--extra-preset-width)) !important;
    padding: 0.1em 0 0 2.3em !important;
    margin: 0 0.4em 0 0.4em !important;
    color: #fff !important;
    text-shadow: #000 !important;
    font-size: 0.9em !important;
}
/* Контуры пресетов */
.preset.DEFAULT input.preset {
    border: 1px solid #666 !important;
}
.preset.T_TRUSTED input.preset {
    border: 1px solid yellow !important;
}
.preset.TRUSTED input.preset {
    border: 1px solid green !important;
}
.preset.UNTRUSTED input.preset {
    border: 1px solid #FF3333!important;
}
.preset.CUSTOM input.preset {
    border: 1px solid orange !important;
}
/***/
.preset.DEFAULT input.preset:hover {
    border-color: #0084ff !important;
}
.preset.T_TRUSTED input.preset:hover {
    box-shadow: inset 0 0 2px yellow !important;
    border-color: yellow !important;
}
.preset.TRUSTED input.preset:hover {
    box-shadow: inset 0 0 2px green !important;
    border-color: green !important;
}
.preset.UNTRUSTED input.preset:hover {
    box-shadow: inset 0 0 2px #FF3333 !important;
    border-color: #FF3333 !important;
}
.preset.CUSTOM input.preset:hover {
    box-shadow: inset 0 0 2px orange !important;
    border-color: orange !important;
}
/* Пресет ИНДИВИДУАЛЬНАЯ */
.customizer fieldset {
    padding: 4px 2px 0px 8px !important;
    background-color: #333333 !important;
}
span.cap.needed {
    background-color: rgba(255,165,0,0.3) !important;
}
.customizer-controls fieldset {
    outline: 1px solid orange !important;
}
.capsContext select {
    height: 2.2em !important;
    font-size: 0.9em !important;
}
.capsContext button.reset {
    height: 2.2em !important;
    font-size: 0.9em !important;
}
button {
    background-color: transparent !important;
    color: #ddd !important;
}
/* URL сайтов */
#https-only {
    margin-top: 0.1em !important;
}
#sites .sites .site td.url span {
    color: #ddd !important;
}
span {
    color: #ddd !important;
}
.sites > tr.site:first-of-type:not(:hover) {
    background: #333 !important;
}
.sites > tr.site:nth-of-type(2n):not(:hover) {
    background-color: #2B2A27 !important;
}
.sites > tr.site:nth-of-type(2n+1):not(:hover) {
    background: #333 !important;
}
.sites tr:hover {
    background: rgba(150,150,150,0.2) !important;
}
/* Checkbox coloring */
input[type="checkbox"] {
    -moz-appearance: none !important;
    border: 1px solid #666 !important;
    background-color: #3F3E47 !important;
    transition: color 0.3s;
    min-width: 18px !important;
    min-height: 18px !important;
    max-width: 18px !important;
    max-height: 18px !important;
    margin-bottom: 0 !important;
}
input[type="checkbox"]:not([disabled]):hover {
    box-shadow: 0 0 4px #0084ff !important;
    border-color: #0084ff !important;
}
input[type="checkbox"]:not(.temp):checked {
    background: #3F3E47 url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="15px" height="15px" viewBox="0 0 16 16" ><path fill="rgb(200,200,200)" d="M 13.09,2.87 C 13.09,2.87 6.00,11.00 6.00,11.00 6.00,11.00 2.00,9.00 2.00,9.00 4.25,12.81 7.00,14.00 7.00,14.00 9.24,10.42 12.04,7.39 13.09,2.87 Z" /></svg>') no-repeat center center !important;
}
}
```
