

```
systemctl list-units --type service --all — просмотр всех юнитов в системе
systemctl list-unit-files --type service
systemctl start name    — запустить сервис
systemctl stop name    — остановить сервис
systemctl restart name    — перезапустить сервис
systemctl status name — посмотреть статус сервиса
systemctl reload name    — перечитать конфигурацию
systemctl daemon-reload   — перечитать конфигурацию для всех
systemctl try-restart name    — перезапустить, если запущен
systemctl enable name    — включить автозапуск сервиса
systemctl disable name    — отключить автозапуск сервиса
systemctl list-unit-files --type service — список установленных юнит-файлов сервисов
```

Директории /lib/systemd/system/ /usr/lib/systemd/user/, /usr/lib/systemd/system/, в зависимости от дистрибутива, это стандартное место складирования юнит-файлов для установленных пакетов. Существующие там юнит-файлы изменять не рекомендуется. Есть ещё директория /etc/systemd/system/ — место для дополнительных юнит-файлов, расширяющих сервис. Их приоритет выше, чем у любых других юнит-файлов в системе. Если посмотришь внимательно, заметишь, что также там лежат ссылки на юнит-файлы из стандартной директории. Ссылка создаётся, когда ты делаешь systemctl enable unit-name
