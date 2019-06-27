# k8s-shogun-helm

## install
### dry run
`helm upgrade --install terrestris-shogun --dry-run --debug ./shogun`

### install
`helm upgrade --install terrestris-shogun ./shogun`

## remove 
`helm del terrestris-shogun --purge`

## Create DB and schema
`kubectl exec -it postgis-85dfb4f76b-9dj69 -- psql -Upostgres -c "CREATE DATABASE shogun2webapp WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'de_DE.UTF-8' LC_CTYPE = 'de_DE.UTF-8';"`

`kubectl exec -it postgis-85dfb4f76b-9dj69 -- psql -Upostgres shogun2webapp -c "CREATE SCHEMA shogun;"`