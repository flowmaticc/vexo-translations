# Vexo - Expansor · Idiomas

Paquetes de idioma de **[Vexo - Expansor](https://github.com/flowmaticc/vexo-releases)** (antes Plantillas Macro), el expansor de texto de [Flowmaticc](https://github.com/flowmaticc).

Vexo los descarga solo: no hace falta bajar nada de aquí a mano.

## 🌍 Idiomas disponibles

| Código | Idioma |
|---|---|
| `esES` | Español (incluido en el programa) |
| `enEN` | English |
| `frFR` | Français |
| `deDE` | Deutsch |
| `itIT` | Italiano |
| `ptPT` | Português |
| `caES` | Català |
| `vaES` | Valencià |
| `ruRU` | Русский |

## ⚙️ Cómo funciona

- Cada paquete se publica como una **release** (`v1`, `v2`… `v11`) con un archivo `.json` por idioma.
- [`idiomas.json`](idiomas.json) es el índice: una entrada por idioma y versión del paquete, con la versión mínima del programa que lo necesita.
- Vexo lee el índice, elige el paquete más reciente compatible con su versión y lo guarda en `%APPDATA%\Vexo\Ajustes\idiomas`.
- Las versiones antiguas del programa siguen usando su paquete: los paquetes viejos nunca se borran.

Formato de una entrada del índice:

```json
{
  "codigo": "enEN",
  "nombre": "English",
  "bandera": "🇬🇧",
  "url": "https://github.com/flowmaticc/vexo-translations/releases/download/v11/enEN.json",
  "version_idioma": "11",
  "version_minima_programa": "3.0.0.21"
}
```

## ➕ Publicar un paquete nuevo

1. Crear la release `vN` con los `.json` de todos los idiomas.
2. **Después**, añadir al final de `idiomas.json` una entrada por idioma con `version_idioma: "N"` y la versión mínima del programa.
3. GitHub puede tardar unos 5 minutos en servir el índice nuevo.

¿Quieres Vexo en tu idioma? Abre un [issue](https://github.com/flowmaticc/flowmaticc.github.io/issues).
