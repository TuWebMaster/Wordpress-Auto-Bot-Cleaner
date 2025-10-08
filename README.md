# Auto Bot Cleaner

**Auto Bot Cleaner** es un snippet PHP para WordPress que permite identificar y eliminar automáticamente usuarios sospechosos (bots) basándose en la longitud de los campos de registro y roles asignados. Esta herramienta limpia registros automáticos no deseados sin afectar a los usuarios reales.

---

## Características

- Escanea usuarios por longitud de campos: `user_login`, `display_name`, `user_nicename`, `first_name`, `last_name`, `nickname`.
- Permite definir roles específicos a revisar (por ejemplo, `subscriber`, `customer`).
- Pre-Scan: muestra cuántos usuarios cumplen con los criterios antes de borrarlos.
- Auto-borrado por tandas con límite configurable (`batch_size`) y seguimiento en tiempo real.
- Protección para evitar borrar al usuario administrador actual.
- Interfaz simple dentro del backend de WordPress.

---

## Cómo usarlo

### Opción 1: Insertar como snippet
1. Instala un plugin para gestionar snippets, como [Code Snippets](https://wordpress.org/plugins/code-snippets/).
2. Crea un nuevo snippet y pega el código de **Auto Bot Cleaner**.
3. Guarda y activa el snippet.  

### Opción 2: Crear un plugin
1. Crea un archivo PHP con el código de **Auto Bot Cleaner** (por ejemplo, `auto-bot-cleaner.php`).
2. Comprime el archivo en un ZIP (`auto-bot-cleaner.zip`).
3. Instálalo desde WordPress: `Plugins > Añadir nuevo > Subir plugin`.
4. Activa el plugin.

---

## Dónde encontrarlo en WordPress

Una vez activo, la opción estará disponible en el menú de administración:

**Usuarios > Auto Bot Cleaner**

Desde allí podrás:

- Configurar el mínimo de caracteres para identificar bots.
- Seleccionar los roles a revisar.
- Definir la cantidad de usuarios por tanda (`batch_size`).
- Ejecutar **Pre-Scan** o **Auto-borrado por tandas**.

---

## Cómo funciona

Esta herramienta nació de la necesidad de eliminar bots registrados en WordPress que compartían un patrón: presencia de publicidad o contenido sospechoso en alguno de los campos del registro. Para diferenciarlos de los usuarios reales, se utiliza un contador de caracteres en campos clave, permitiendo eliminar únicamente los registros sospechosos.

---

## Créditos

Desarrollado por [TuWebmaster](https://www.tuwebmaster.com.ar).  
Si necesitas adaptar esta herramienta a tus necesidades específicas, comunicate con nosotros.

---

## Licencia

Disponible bajo [MIT License](https://opensource.org/licenses/MIT) o la licencia que prefieras aplicar.
