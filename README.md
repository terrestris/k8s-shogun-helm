# k8s-geoserver-helm

## install
### dry run
`helm upgrade --install terrestris-geoserver --dry-run --debug ./shogun`

### install
`helm upgrade --install terrestris-geoserver ./shogun`

## remove 
`helm del terrestris-geoserver --purge`

`kubectl exec -it postgis-85dfb4f76b-9dj69 -- psql -Upostgres -c "CREATE DATABASE shogun2webapp WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'de_DE.UTF-8' LC_CTYPE = 'de_DE.UTF-8';"`

`kubectl exec -it postgis-85dfb4f76b-9dj69 -- psql -Upostgres shogun2webapp -c "CREATE SCHEMA shogun;"`