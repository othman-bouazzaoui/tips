*************************************************************************************************
This command displays all tables with the status "column in_use if 1=locked :
- show open tables
*************************************************************************************************
This command displays all processing or processes that are executing "column command=query" :
- show full processlist;
*************************************************************************************************
to kill a process
- call mysql.az_kill([id])
*************************************************************************************************
for all the processes, it is necessary to build several queries with all the process IDs :
SELECT CONCAT('call mysql.az_kill(',id,');') 
   FROM 
 information_schema.processlist isp
   where isp.id != [id_of_the_treatment_that_we_would_not_kill(example of a liquibase treatment)]
*************************************************************************************************
Important: the syntaxes differ between mysql local and azure & aws
__________________________________________________________________
* If you are using your local mysql run :
- kill ID_process

*If you are using your mysql aws use store procedure :
- call mysql. rds_kill(id)

*If you are using your mysql azure use store procedure:
- call mysql.az_kill(id)
*************************************************************************************************
