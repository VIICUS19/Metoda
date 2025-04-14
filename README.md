Net1-Open
Visual C – Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\VISUAL_C
SQL – Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\SQLEXPRE
После установки в пуске нахожу SQL Server (manager), тут нужно поставить в Enabled, после этого (где WINN) делаю – Restart
Net1-Admin
Visual C – Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\VISUAL_C
ЦУС сервер - Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\RU_RU
VipNet client - VIPNET_C.5\SOFTWARE\
Заходим в ЦУС вводим IP-адрес (172.16.224.226, проверка подлинности SQL, имя sa, пароль xxXX1234 и проверить подключение, если всё успешно, то продолжаем установку)
Net1-Open
ЦУС клиент - Vipnet_A.7_R\SOFT\___000\CLIEYNT_I\PACKAGES\RU_RU (установка через power shell!)
Net2-Client
Панель управления →часы и регионы → региональные стандарты → дополнительно → изменить язык системы
Visual C – Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\VISUAL_C
VipNet client - VIPNET_C.5\SOFTWARE\
Net1-OperCA
Visual C – Vipnet_A.7_R\SOFT\___000\SERVER_I\PACKAGES\VISUAL_C
VIPNet Client – VIPNET_C.5\SOFTWARE\
Net1 – Admin
УКЦ - Vipnet_A.7_R\SOFT\______\
Net1 – Open
Заходим в ЦУС, входим под IP Admina (172.16.224.225) 
Далее подключаю диск с лицензией (______.ITC)
Net1 – Admin
Захожу в УКЦ, (Вход по IP Open1, SQL-сервер: 172.16.224.226)
Net1 – Open
Создаю координаторов и пользователей по заданию
Координаторы(добавить в межсерв канал, удалить другие роли и добавить роль - Coordinator HW-VA)
Добавление роли для AdminS - Registration Point, Policy Manager, для Node_CR - Registration Point
Создаем связи с пользовтаелями
Сохранение структуры файла в формат html
Net1 – Admin
Заходим в УКЦ, сетевые узлы, выделяем всё ПКМ и выдать новый дистрибутив ключей. 
Теперь на каждой машине захожу в VipNet – Admin – AdminS, OperCA – Node_CR, Net2-Client – Rem_Client
+создать фильтры защищённой и открытой сети
Net1 – Coord
Убрать галочку
Root_Coordinator
UP, Static(тут IP-aдрес), Up, Static(тут IP-адрес), Down(IP-адрес), Off,Off, No,No, Yes, Finish.
Net2 – Coord
Убрать галочку
Sub_Coordinator
UP, Static(тут IP-aдрес), Up, Static(тут IP-адрес), Down(IP-адрес), Off,Off, No,No, Yes, Finish.
Захожу в VipNet на каждую машину
Админ=AdminS (172.16.224.225)
OperCa=Node_CR(172.16.224.227)
Net2-Client=Rem_Client(10.10.20.130)
Net1-Coord=Root_Coordinator(172.16.224.228, 10.8.248.1)
Net2Coord=Sub_Coordinator(10.10.20.129, 10.8.248.2)
