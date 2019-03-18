Dev environment for working with SQL + Jupyter notebooks

## Installation
### Do once - create volume 
this will help to persist data when spinning up / down container

`docker create -v /var/lib/postgresql/data --name PostgresData alpine`

### running postgre
`docker run -p 5432:5432 --name postgreDB -e POSTGRES_PASSWORD=yourPassword -d --volumes-from PostgresData postgres`


### Jupyter Lab
activate environment run

`jupyter lab`
### Issues
At the time of writing this there is a problem with the default installation. Follow instructions here:
https://github.com/jupyter/notebook/issues/4467