
# Pandora FMS API-NPP

## Info
- Per executar el programa s'ha de tenir instalat el python versio 3 o mes.
- Requeriments a requirements.txt.
- Configuració de la base de dades a `config/config.yaml`
- Logs de errors a `errorLogs/*txt`
- Executar amb opcio -h per veure mes opcions i funcionalitats.
- El fitxer compilar.bat transforma el .py en .pyc que es mes eficient i rapid.
## Estructura de la base de dades
```
"usuari" usuari de pandora

"contrassenya" contrassenya de pandora

"apipassw" contrassenya de la api de pandora (es pot trobar en la vostre interfaç web del pandora)

"host" URL de pandora + /pandora_console/include/api.php
```
## Ús
- Executar el fitxer `PandoraFMS_API.py` o `PandoraFMS_API.cpython-39.pyc` amb les opcions adients. Llavors les dades es guardaran a `dadesPandora.json` i si la opcio de excel esta activada tambe es guardara a `PandoraResum.xlsx`
- Opcions:
```
usage: PandoraFMS_API.cpython-39.pyc [-h] [-e] [-f RUTA] [-q] [-v] [-w URL]

Una API per a recullir informacio de la web de PandoraFMS.

optional arguments:
  -h, --help            show this help message and exit
  -e, --excel           Guardar la informacio a un excel, per defecte esta desactivat
  -f RUTA, --file RUTA  Especificar el fitxer de excel a on guardar. Per defecte es: PandoraResum.xlsx
  -q, --quiet           Nomes mostra els errors i el missatge de acabada per pantalla.
  -v, --versio          Mostra la versio
  -w URL, --web URL     Especificar la web de PandoraFMS a on accedir. Per defecte es: http://pandora.eio.cat/pandora_console/include/api.php
```

### Proximament:
1. Afegir support per altres bases de dades a part de mysql