# ilarionovdm_infra
ilarionovdm Infra repository

#подключение в одну команду
#ssh -i %HOMEPATH%\.ssh\appuser -A appuser@84.201.173.137 "ssh 10.130.0.32"

#красивое подключение
#set "someinternalhost=-i %HOMEPATH%\.ssh\appuser -A appuser@84.201.173.137 "ssh 10.130.0.32""
#ssh %someinternalhost%

#красивое подключение вариант 2:
#doskey someinternalhost=ssh -i %HOMEPATH%\.ssh\appuser -A appuser@84.201.173.137 "ssh 10.130.0.32"
#someinternalhost

bastion_IP = 84.201.173.137
someinternalhost_IP = 10.130.0.32
