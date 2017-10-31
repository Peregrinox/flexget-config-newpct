# configuracion de descargas automaticas desde newpct1 para usuarios que desean consumir contenidos en Español

funcionando:
- gestion de series en curso (RSS) a traves de listas en trakt.tv
- Tarea para "traducir" los nombres de las series a español mediante thetvdb
- Tarea para mover fichero de video de las series descargadas a directorio de Series

# Ejemplos de uso:

- actualizar lista de series en traktv pero con titulo en español
```
flexget execute --tasks fill-series-list
```

- buscar en rss de newpct1 filtrando con la lista personalizada (entry-list):
```
flexget execute --tasks spaseries
```

# CRON:

```
...
@hourly /home/osmc/bin/flexget execute --tasks spaseries
10 */4 * * * /home/osmc/bin/flexget execute --tasks fill-series-list
...
```
