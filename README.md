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

testapp_IP = 130.193.51.207
testapp_port = 9292

#deploy одной командой
 yc compute instance create `
>>  --name reddit-app2 `
>>  --hostname reddit-app2 `
>>  --memory=4 `
>>  --create-boot-disk image-folder-id=standard-images,image-family=ubuntu-1604-lts,size=10GB `
>>  --network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4 `
>>  --metadata serial-port-enable=1 `
>>  --metadata-from-file user-data=test.yaml `
>>  --preemptible


#для rebuild3
