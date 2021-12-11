1. Находим информацию по коммиту с помощью команды  
git show aefea  
hash: aefead2207ef7e2aa5dc81a34aedf0cad4c32545  
comment: Update CHANGELOG.md
2. Способом из пункта 1 находим информацию по коммиту  
tag: v0.12.23
3. Находим инормацию о родителях с помощью команды  
git show b8d720^  
У коммита b8d720 два родителя  
родитель1: 58dcac4b7  
родитель2: ffbcf5581  
В задании не было написано про необходимость указывать полные хэши, из-за написал сокращенные7
4. Получаю список комммитов с помощью команды  
git log --oneline v0.12.23..v0.12.24  
Коммит с тегом v0.12.24 отбрасываю, т.к. нужны коммиты между  
b14b74c49 [Website] vmc provider links  
3f235065b Update CHANGELOG.md  
6ae64e247 registry: Fix panic when server is unreachable  
5c619ca1b website: Remove links to the getting started guide's old location  
06275647e Update CHANGELOG.md  
d5f9411f5 command: Fix bug when using terraform login on Windows  
4b6d06cc5 Update CHANGELOG.md  
dd01a3507 Update CHANGELOG.md  
225466bc3 Cleanup after v0.12.23 release  
5. Находим список коммитов со подстрокой "func providerSource(" с помощью команды  
git log --oneline -S "func providerSource("  
Находим всего один коммит - 8c928e835, логично что это может быть только коммит создания, но для чистоты эксперемента, смотрим изменения с помощью команды git show и находим строку:  
+func providerSource(services *disco.Disco) getproviders.Source {
6. Находим все коммиты с подстрокой "globalPluginDirs" c помощью команды:
git log --oneline -S "globalPluginDirs"  
35a058fb3  
c0b176109  
8364383c3  
7. Выполняя действия аналогичные пункту 5, находим список коммитов с подстрокой "func synchronizedWriters(" и далее находим коммит с текстом:  
+func synchronizedWriters(targets ...io.Writer) []io.Writer {  
Смотрим автора коммита:  
Martin Atkins <mart@degeneration.co.uk>

