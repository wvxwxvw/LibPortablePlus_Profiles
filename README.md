## Профили для сборки LibPortablePlus версии 21.10.02
Если захотите использовать с более новой версией сборки, то следует взять некоторые взаимосуществующие компоненты из сборки, а не из профиля, а именно:  
`user.js` и `QuickToggleAboutConfig_Damby_ucf.js`

### Профиль Native Tabs Fx
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile-ntfex_220322.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-screen.md)  
  
### Профиль Tree Style Tab
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/raw/main/Firefox.91.ESR.LPP.profile-tstex_220322.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-screen.md)  
  
===========================================================================  

Большая часть кнопок выведенных на панели имеют подробные подсказки.  
Наведите курсор на интересующую вас кнопку и читайте.

===========================================================================  

### NoScript

В профилях от 220322 я внес правки для версии 11.4, но в 11.4.1 подвезли нового.  
Пока приступ не кончится, кому надо, редактируйте самостоятельно файл  
`...\profile\chrome\userContent_dark_addons.css`  
  
После секции `.presets input.preset:checked {` добавьте секцию:  
```
:not(#presets) > .sites .site:not(.customizing) .presets input.preset:checked + label.preset {
	background-image: none !important;
}
```
а в секцию `.presets input.preset + label {` добавьте строки:  
```
	background-image: none !important; /* 11.4.1 */
	margin-top: 2px !important; /* 11.4.3 */
```
Это уберет градиент и дурацкую фактурность у выбранного пресета (в попапе и на странице правил).  
  
=========================================================================== 
  
### Отключить появление главного меню по Alt  
  
В файле `profile\chrome\user_chrome_files\custom_styles\main_window.css`  
сразу после строки
```
/* Классическое меню - показывать при наведении или при нажатии клавиши "Alt" --> */
```
добавить секцию
```
#titlebar > #toolbar-menubar:not(:hover) #main-menubar {
    display: none !important; /* !!! отключение вызова меню по Alt */
}
```
Может быть полезно тем кто использует горячие клавиши с этим модификатором.  
  
===========================================================================
