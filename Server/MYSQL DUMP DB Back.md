### Dump From Local PC
```
mysqldump -u root -p database_name > C:\Users\HP\Desktop\igm.sql
```
### Dump From a Host (along with password)
```
mysqldump -u hasan -p 'Hs_3605#' -h 103.5.233.163 bbts_erp > ~/Desktop/DBs/bbts/backup_local_$(date +%Y_%m_%d_%H_%M_%S).sql
```
### Dump with current date and time. 
```
mysqldump -u hasan -p 'Hs_3605#' db_hrlines > /var/www/hrlinesvms.com/storage/backup_$(date +%Y_%m_%d_%H_%M_%S).sql
```
