## Профили для сборки LibPortablePlus версии 21.10.02+

### Профиль Native Tabs Fx
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/Firefox.91.ESR.LPP.profile-ntfex_220224.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/ntfex-screen.md)  
  
### Профиль Tree Style Tab
[Скачать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/Firefox.91.ESR.LPP.profile-tstex_220219.7z)  -  [Почитать](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-Readme.md)  -  [Посмотреть](https://github.com/wvxwxvw/LibPortablePlus_Profiles/blob/main/tstex-screen.md)  
  
===========================================================================  

Большая часть кнопок выведенных на панели имеют подробные подсказки.
Наведите курсор на интересующую вас кнопку и читайте.

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
Может быть полезно тем кто использует горячие клавиши с этим модификатором при работе с текстом.  
  
===========================================================================
