ProGuardDeobfuscator - небольшая модификация программы ProGuard, превращающая ее в квази-деобфускатор. В процессе обработки короткие обфусцированные имена пакетов, классов, полей и методов заменяются на более осмысленные и уникальные в пределах Jar файла.

Для деобфускации программы просто перетащите ее Jar на файл "deobfuscate.bat". В результате будет создана папка с именем программы, в которой будет находиться собственно деобфусцированный Jar, а также карта переименования и протокол работы деобфускатора.

Для корректной деобфускации необходимо поместить в папку "lib" все библиотеки, которые используются в обрабатываемой программе. В архив с ProGuardDeobfuscator включена большая часть библиотек для MIDP2.1.

Переименование производится по следующей схеме:

пакеты -> "pkg_n"
классы -> "Class_n"
поля -> "var_n"
методы -> "sub_n"

где n - случайно возрастающее шестнадцатеричное число (например 10, 23, 3b, 5a, 76, 9f, f4, 140, 18d, 1e5, и т.д.)

По умолчанию используются параметры для деобфускации J2ME мидлетов. Эти параметры можно изменить, отредактировав скрипт "deobfuscate.bat".

--
(C) SilentKnight


ProGuardDeobfuscator is slightly modified version of ProGuard, which was turned into a quasi deobfuscator. During file processing short obfuscated packages', classes', fields' and methods' names are replaced with more meaningful and unique across Jar file ones.

To deobfuscate a program just drag-and-drop it's Jar onto "deobfuscate.bat" file. As the result a folder with application's name will be created where deobfuscated Jar will be placed, as well as rename map and deobfuscator's log.

In order for deobfuscation to complete correctly, all libraries used by the processed program must be placed into "lib" folder. Most of the MIDP2.1 libraries are included in ProGuardDeobfuscator package.

Renaming is carried out according to following scheme:

packages -> "pkg_n"
classes -> "Class_n"
fields -> "var_n"
methods -> "sub_n"

where n is randomly increasing hexadecimal number (e.g. 10, 23, 3b, 5a, 76, 9f, f4, 140, 18d, 1e5, etc.)

By default parameters for deobfuscation J2ME midlets are used. These parameters might be changed by editing the "deobfuscate.bat" script.

--
(C) SilentKnight
