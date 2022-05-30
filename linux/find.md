- Рекурсивное изменение прав на директории
```bash
find . -type d -exec chmod 0750 {} \;
```
- Поиск и удаление файлов старше 1440 минут (24 ч)
``` bash
find ./somedir -mmin +1440 -exec rm {} \;
```

- Поиск и удаление файлов старше 7 дней
``` bash
find ./somedir -mtime +7 -exec rm {} \;
```

- Поиск и удаление файлов старше 60 дней
``` bash
find ./somedir -mtime +60 -exec rm {} \;
```

- Поиск и удаление файлов старше года
``` bash
find ./somedir -mtime +365 -exec rm {} \;
```


