Al parecer hay un error al asignar los pvc
Entonces lo que se hizo fue creat un archivo storage.yaml en argocd/server y aplicar
En el values primary/persistence se asigna el nombre del pvc 
Ahora se presenta otro problema que es
mariadb_1   | mkdir: cannot create directory '/bitnami/mariadb': Permission denied
esto es porque el pv creado no cuenta con los persmisos correspondientes
entonces para arreglarlo hay que correr esta linea 
 sudo chown -R 1001:1001 /mnt/mariadb/
el path depende del que se haya agregado en el pv
