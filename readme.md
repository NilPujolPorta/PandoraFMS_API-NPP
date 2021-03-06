
# Pandora FMS API-NPP

## Info
- Per executar el programa s'ha de tenir instalat el python versio 3 o mes.
- Requeriments a requirements.txt.
- Configuració de la base de dades a `config/config.yaml`
- Logs de errors a `errorLogs/*txt`
- Executar amb opcio -h per veure mes opcions i funcionalitats.
- El fitxer compilar.bat transforma el .py en .pyc que es mes eficient i rapid.
## Estructura de la base de dades
En una Base de dades que es digui "pandora" un taula anomenada "credencials":
```
"usuari" usuari de pandora

"contrassenya" contrassenya de pandora

"apipassw" contrassenya de la api de pandora (es pot trobar en la vostre interfaç web del pandora)

"host" URL de pandora + /pandora_console/include/api.php
```
## Instal·lació

- Utilitzant pip:

  ```pip install PandoraFMS-API```

- Clonar el repositori
```gh repo clone NilPujolPorta/PandoraFMS_API-NPP```

## Ús
### Maneres d'execució del programa (ordenades per recomenades)
- A la linea de commandes `PandoraFMS-API [opcions]`
- ```python -m PandoraAPI [opcions]```
- ```./PandoraFMS_API-runner.py [opcions] ```
- Executar el fitxer `PandoraFMS_API.py` o `PandoraFMS_API.cpython-39.pyc` amb les opcions adients. Llavors les dades es guardaran a `dadesPandora.json`i si la opcio de excel esta activada tambe es guardara a `PandoraResum.xlsx`



### Opcions
```
usage: PandoraFMS_API.cpython-39.pyc [-h] [-e] [-f RUTA] [-q] [-v] [-w URL]

Una API per a recullir informacio de la web de PandoraFMS.

optional arguments:
  -h, --help            show this help message and exit
  -e, --excel           Guardar la informacio a un excel, per defecte esta desactivat
  -f RUTA, --file RUTA  La ruta(fitxer inclos) a on guardar el excel. Per defecte es: PandoraResum.xlsx
  --json-file RUTA      La ruta(fitxer inclos) a on es guardara el fitxer de dades json. Per defecte es: dadesPandora.json
  -q, --quiet           Nomes mostra els errors i el missatge de acabada per pantalla.
  -v, --versio          Mostra la versio
  -w URL, --web URL     Especificar la web de PandoraFMS a on accedir.
```

### Proximament:
1. Afegir support per altres bases de dades a part de mysql
