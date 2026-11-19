# Configurador de equipos de marcaje

Programa de Audisoft para dejar un **terminal de marcaje SV-8396H** marcando en el
**Portal del Colaborador**. Es un solo `.exe` para Windows: no se instala y se
actualiza solo.

<p>
  <a href="https://github.com/AudisoftSPA/audisoft-configurador-autoupdater/releases/latest/download/Configurador-Terminal-SV-8396H.exe"><b>⬇ Descargar el configurador (última versión)</b></a>
</p>

---

## Instructivo: terminal recién llegado

Son **dos partes**: primero el terminal se conecta al Wi-Fi (en el propio equipo)
y después el configurador, desde un computador en esa **misma red Wi-Fi**, lo
conecta al portal.

```mermaid
flowchart LR
    A["📦 Terminal nuevo<br/>enchufado"] --> B["📶 Parte 1<br/>Conectarlo al Wi-Fi<br/>(en el terminal)"]
    B --> C["💻 Parte 2<br/>Abrir el configurador<br/>(mismo Wi-Fi)"]
    C --> D["✅ Marcando en el<br/>Portal del Colaborador"]
```

### Antes de empezar

| Qué | Para qué |
|---|---|
| El terminal enchufado a la corriente | Que encienda (tarda cerca de un minuto). |
| Nombre y clave del Wi-Fi donde quedará instalado | El terminal se conecta a esa red. |
| Un computador con Windows **en ese mismo Wi-Fi** | Desde ahí se usa el configurador. |
| La **dirección del terminal** que entrega el portal *(recomendado)* | En el portal: **Configuración → Dispositivos de marcaje → Terminales v2** → botón «Dirección» → «Copiar». Si el terminal aún no está en el portal, basta con el RUT de la empresa (ver paso 2.4). |

> La red tiene que tener **salida a internet**: el terminal habla directo con el portal.

---

### Parte 1 · Conectar el terminal al Wi-Fi

Se hace tocando la pantalla del terminal. Las imágenes son del manual del
fabricante (en inglés); en el equipo los nombres pueden verse en español. Lo
que hay que tocar va marcado en rojo.

<table>
  <tr>
    <th>1.1 Abrir el menú</th>
    <th>1.2 Comunicación</th>
    <th>1.3 Wi-Fi</th>
    <th>1.4 Elegir la red</th>
  </tr>
  <tr>
    <td><img src="docs/terminal-1-inicio.png" width="180" alt="Pantalla de inicio del terminal con la esquina inferior izquierda marcada"></td>
    <td><img src="docs/terminal-2-menu.png" width="180" alt="Menú del terminal con Comm marcado"></td>
    <td><img src="docs/terminal-3-comunicacion.png" width="180" alt="Menú Comunicación con Wifi marcado"></td>
    <td><img src="docs/terminal-4-wifi.png" width="180" alt="Lista de redes Wi-Fi con el interruptor y una red marcados"></td>
  </tr>
  <tr valign="top">
    <td>Tocar la <b>esquina de abajo a la izquierda</b> (donde dice la versión). Un terminal nuevo no pide clave; si la pide, entrar como administrador.</td>
    <td>Tocar <b>Comm</b> (Comunicación).</td>
    <td>Tocar <b>Wifi</b>.</td>
    <td>Encender <b>Wi-Fi</b>, tocar la red y escribir su clave. Si la red no aparece, «Add WIFI to hand action» permite escribir el nombre a mano.</td>
  </tr>
</table>

**1.5 (Recomendado) Ver la IP en la pantalla.** En **Comm → Local Setting**
activar **Show IP address**. Así la pantalla de inicio muestra la dirección del
terminal en la red (por ejemplo `192.168.1.27`), que sirve si el configurador no
lo encuentra solo.

<img src="docs/terminal-5-mostrar-ip.png" width="180" alt="Local Setting con Show IP address marcado">

Listo: el terminal ya está en el Wi-Fi. Todo lo demás (dirección del portal,
idioma, hora de Chile, personas, nombre e imágenes) lo hace el configurador y el
portal; **no hace falta tocar nada más en el terminal**.

---

### Parte 2 · Conectarlo al portal con el configurador

**2.0 Abrir el configurador.** Descargar
[`Configurador-Terminal-SV-8396H.exe`](https://github.com/AudisoftSPA/audisoft-configurador-autoupdater/releases/latest/download/Configurador-Terminal-SV-8396H.exe)
y abrirlo con doble clic, en un computador conectado al **mismo Wi-Fi que el
terminal**. Si Windows muestra «Windows protegió su PC», hacer clic en
**Más información → Ejecutar de todas formas** (el programa no va firmado).

<table>
  <tr>
    <td width="50%"><img src="docs/configurador-1_inicio.png" alt="Pantalla de inicio del configurador"></td>
    <td width="50%"><img src="docs/configurador-2_bienvenida.png" alt="Bienvenida del asistente"></td>
  </tr>
  <tr valign="top">
    <td><b>2.1</b> Elegir <b>Configurar huellero</b>.</td>
    <td><b>2.2</b> La bienvenida resume lo que se va a hacer. <b>Siguiente</b>.</td>
  </tr>
  <tr>
    <td><img src="docs/configurador-3_buscar.png" alt="Búsqueda del terminal en la red"></td>
    <td><img src="docs/configurador-4_clave.png" alt="Clave de administrador opcional"></td>
  </tr>
  <tr valign="top">
    <td><b>2.3 Buscar el terminal.</b> Aparece como «Terminal de marcaje SV-8396H» con su número de serie (el de la etiqueta de atrás del equipo). Si no aparece, escribir la IP que muestra su pantalla (paso 1.5) y <b>Probar</b>.</td>
    <td><b>2.4 Clave del terminal.</b> Un terminal nuevo viene sin clave: se puede dejar en blanco o definir una de 4 a 8 dígitos (si se define, <b>anotarla</b>: se pide para volver a configurarlo).</td>
  </tr>
  <tr>
    <td><img src="docs/configurador-5_portal.png" alt="Conexión al portal"></td>
    <td><img src="docs/configurador-6_configurar.png" alt="Revisar y configurar"></td>
  </tr>
  <tr valign="top">
    <td><b>2.5 Conexión al portal.</b> Pegar la <b>dirección</b> copiada del portal (recomendado). Si el terminal aún no está en el portal, elegir «generar un código», el servidor y el RUT de la empresa.</td>
    <td><b>2.6 Revisar y configurar.</b> Muestra lo que se escribirá en el terminal. <b>Configurar terminal</b> y esperar los ✔.</td>
  </tr>
  <tr>
    <td><img src="docs/configurador-7_listo.png" alt="Terminal conectado"></td>
    <td valign="top">
      <b>2.7 ¡Terminal conectado!</b><br><br>
      En menos de un minuto el terminal recibe las personas de su sucursal, el
      idioma, la hora de Chile, su nombre y las imágenes de Audisoft.<br><br>
      <b>Si se usó «generar un código»:</b> falta un paso. En el portal,
      <b>Configuración → Dispositivos de marcaje → Terminales v2 → «Agregar terminal»</b>,
      pegar el código, ponerle nombre y elegir la sucursal. Guardar bien el código:
      funciona como clave del terminal y el configurador no lo vuelve a mostrar.
    </td>
  </tr>
</table>

**Último paso:** enrolar a cada persona en el propio terminal
(menú → **User** / Usuarios): rostro, huella o tarjeta.

---

### Si algo no funciona

| Problema | Qué hacer |
|---|---|
| El configurador no encuentra el terminal | Revisar que el computador y el terminal estén en el **mismo Wi-Fi** (no en la red de invitados). Escribir la IP que muestra la pantalla del terminal (paso 1.5) y **Probar**. |
| Pide una clave que nadie conoce | El terminal ya fue configurado antes con clave. Pedirla a quien lo configuró o a soporte de Audisoft. |
| Termina, pero «el terminal aún no informa conexión» | El Wi-Fi no tiene salida a internet o la bloquea. Probar con otra red. Si se usó un código, primero hay que agregarlo en el portal. |
| El portal no muestra el terminal como conectado | Esperar un minuto (se reporta cada 20 segundos) y revisar en **Configuración → Dispositivos de marcaje → Terminales v2**. |
| Cambió el Wi-Fi del lugar | Repetir solo la **Parte 1** en el terminal. La conexión al portal se mantiene. |

---

## Actualizaciones del configurador

Este repositorio guarda **solo las versiones publicadas del `.exe`**
(pestaña [Releases](https://github.com/AudisoftSPA/audisoft-configurador-autoupdater/releases)).
Al abrirse, el configurador revisa si hay una versión nueva y, en la pantalla de
inicio, ofrece **Actualizar ahora** o **Más tarde**. Sin internet sigue
funcionando igual. La versión en uso se ve abajo a la izquierda y en el título
de la ventana.

El código fuente está en un repositorio privado de Audisoft.
