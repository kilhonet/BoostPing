# BoostPing

**Una herramienta gratuita que ajusta la configuración de red de Windows para juegos con un solo botón y mejora la respuesta de los juegos en línea.**

[English](README.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · Español · [Português (Brasil)](README.pt-BR.md) · [Français](README.fr.md)

> Este documento es una traducción. Si hay alguna diferencia, la [versión coreana](README.ko.md) es la que prevalece.

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20(64--bit)-0078D4)
![License](https://img.shields.io/badge/license-Freeware-brightgreen)
[![Download](https://img.shields.io/badge/download-kilho.net-orange)](https://down.kilho.net/boostping?lang=es)

![Pantalla de BoostPing](images/boostping-en.png)

## Descripción general

De forma predeterminada, Windows acumula los datos de red durante un instante y los envía en bloque. Es eficiente para descargar archivos o navegar por la web, pero en los juegos en línea —donde cada pulsación de tecla debe llegar al servidor de inmediato— hace que el juego responda más tarde.

BoostPing cambia cinco de estos ajustes para adaptarlos a los juegos. Pulse **Iniciar boost** y encontrará la red con la que está conectado a internet, aplicará los ajustes y volverá a conectar la red. Pulse **Apagar boost** y restaurará exactamente los valores que tenía antes. Usted elige qué elementos cambiar, y los que deje sin marcar nunca se tocan.

## Funciones principales

- **Un solo botón** — Sin configuraciones complicadas; basta con pulsar Iniciar boost una vez.
- **Detecta automáticamente la red en uso** — Elige el adaptador realmente conectado a internet y muestra su nombre e IP en la parte inferior de la ventana. Los adaptadores de red virtuales se omiten.
- **Cinco elementos, aplicados a su elección** — ACK inmediato, Sin retraso de ACK, Desactivar el algoritmo de Nagle, Quitar limitación de red, Prioridad a los juegos.
- **Restauración exacta** — Recuerda los valores de antes del boost y los devuelve al apagarlo. Los ajustes que no existían se eliminan, y los valores que usted había cambiado vuelven a esos valores.
- **Sigue activo aunque lo cierre** — Los ajustes se aplican a Windows, así que el efecto continúa tras cerrar la ventana o reiniciar. Al volver a abrirlo, muestra el estado aplicado tal cual.
- **9 idiomas** — Coreano · Inglés · Japonés · Chino · Ruso · Italiano · Francés · Árabe · Español. Sigue el idioma de visualización de Windows.

## Descarga / Instalación

| Tipo | Enlace |
|---|---|
| Instalador | [Descargar](https://down.kilho.net/boostping?lang=es) |
| Portable (ZIP) | [Descargar](https://down.kilho.net/boostping?lang=es&nosetup) |

La versión instalable se inicia en cuanto termina la instalación. Para la versión portable, descomprima el ZIP y ejecute `BoostPing.exe`. En ambos casos solicita **derechos de administrador**.

## Uso

### Primeros pasos

1. Ejecute BoostPing. Como cambia ajustes de Windows, aparece una ventana de confirmación de permisos de administrador: pulse **Sí**.
2. Compruebe que en la línea inferior aparecen el nombre y la IP de la red que está usando. (p. ej. `Ethernet (Realtek PCIe GbE Family Controller) · 192.168.0.10`)
3. Para elegir qué elementos cambiar, pulse el **icono de ajustes** arriba a la derecha y se abrirá la pantalla **TUNING**. Al principio los cinco están activados.
4. Pulse **Iniciar boost**. El estado cambia a **BOOST** y aparece «Reconectando la red…». En ese momento internet se corta brevemente y se vuelve a conectar.
5. Cuando vuelve internet, el estado cambia a **ON** con «Optimización aplicada». Ya puede iniciar su juego.
6. Para volver a como estaba todo, pulse **Apagar boost**. La red se reconecta una vez más y el estado vuelve a **READY**.

### Elementos de la pantalla

**Pantalla principal**

| Elemento | Descripción |
|---|---|
| Logotipo **BOOST//PING** | Abre la página de BoostPing |
| Icono de ajustes (arriba a la derecha) | Abre la pantalla TUNING |
| **STATUS** | **READY** = en espera, **BOOST** = aplicando, **ON** = aplicado |
| 5 barras · **%d / 5 elementos** | Número de elementos activados; una barra por elemento |
| **Iniciar boost** / **Apagar boost** | Aplicar / restaurar los ajustes originales |
| Línea inferior | Nombre · IP de la red en uso, versión del programa |

**Pantalla TUNING** — Pulse un elemento para activarlo o desactivarlo. Los cambios se guardan al instante.

| Elemento | Qué hace |
|---|---|
| **ACK inmediato** | Envía las confirmaciones al instante sin agruparlas |
| **Sin retraso de ACK** | Pone a 0 el temporizador de confirmación diferida |
| **Desactivar el algoritmo de Nagle** | Envía los paquetes pequeños al instante sin agruparlos |
| **Quitar limitación de red** | Quita el límite de transferencia durante la reproducción |
| **Prioridad a los juegos** | Deja de reservar CPU para tareas en segundo plano |

### Situaciones habituales

**Cuando sus acciones en el juego se sienten un poco tarde**
Pulse Iniciar boost en BoostPing antes de abrir el juego. Los juegos en línea que intercambian pequeños datos con frecuencia son donde más se nota. Como internet se reconecta brevemente al aplicar el boost, conviene activarlo **antes** de entrar en una partida.

**Cuando quiere activarlo una vez y dejarlo así**
Después de activar el boost, puede cerrar la ventana de BoostPing. Los ajustes se quedan en Windows, así que siguen aplicados incluso después de reiniciar. Al volver a abrir BoostPing, el estado aparece como **ON**.

**Cuando juega con música o un directo de fondo**
Windows limita las transferencias de red mientras se reproduce contenido multimedia. Con **Quitar limitación de red** activado, ese límite no se aplica aunque tenga música o vídeo en marcha.

**Cuando solo quiere algunos elementos**
Con el boost apagado (READY), vaya al icono de ajustes → pantalla TUNING y pulse los elementos que no quiera para desactivarlos. Las barras y **%d / 5 elementos** de la pantalla principal cambian al momento. Los elementos desactivados no se tocan nunca, ni al iniciar ni al apagar.

**Cuando quiere cambiar elementos con el boost activado**
Mientras el boost está activado, la pantalla TUNING queda bloqueada y muestra «Puedes cambiarlo después de apagar el boost.». Hágalo en este orden: Apagar boost → cambiar elementos → Iniciar boost.

**Cuando quiere comparar la diferencia**
Juegue una partida en el estado original con Apagar boost y otra con Iniciar boost. Al apagarlo se restauran exactamente los valores de antes, así que puede alternar y comparar tantas veces como quiera.

**Cuando antes había cambiado usted mismo la configuración de red**
BoostPing recuerda los valores actuales antes de empezar. Al apagarlo, vuelve a **los valores que usted había puesto**, no a los predeterminados de Windows.

**Cuando alterna entre Wi‑Fi y cable en un portátil**
El boost se aplica a la red que estaba en uso al iniciarlo. Si ha cambiado de red, pulse Apagar boost, cierre BoostPing y vuelva a abrirlo. Cuando la nueva red aparezca en la línea inferior, pulse Iniciar boost. Al apagarlo, siempre restaura la red a la que se aplicó al principio, aunque haya cambiado de red después.

**Cuando termina de jugar y quiere dejar todo como estaba**
Abra BoostPing y pulse Apagar boost. Antes de desinstalar el programa, apague también el boost primero.

**Cuando no ve la ventana de BoostPing**
Solo puede haber un BoostPing en ejecución a la vez. Si lo ejecuta de nuevo cuando ya está abierto, la ventana existente pasa al frente (y se restaura si estaba minimizada).

## Configuración

Se cambia en la pantalla TUNING y se guarda al instante. Los ajustes se conservan al actualizar.

| Elemento | Valor predeterminado |
|---|---|
| ACK inmediato | Activado |
| Sin retraso de ACK | Activado |
| Desactivar el algoritmo de Nagle | Activado |
| Quitar limitación de red | Activado |
| Prioridad a los juegos | Activado |

El idioma de la interfaz sigue el idioma de visualización de Windows (coreano · inglés · japonés · chino · ruso · italiano · francés · árabe · español; inglés en los demás casos). El árabe se muestra de derecha a izquierda.

## Requisitos

- Windows 10 · Windows 11 (64 bits)
- Derechos de administrador — como cambia la configuración de red de Windows, aparece una ventana de confirmación de permisos al iniciarlo.
- No necesita ningún runtime adicional.

## Actualizaciones

BoostPing **no** se actualiza solo. Al iniciarse comprueba si hay una versión nueva y muestra un aviso; al pulsar **Sí** se abre la página de descarga y el programa se cierra. Las nuevas versiones se publican manualmente tras una verificación interna y se anuncian en la [página de BoostPing](https://kilho.net/boostping). Consulte el [aviso sobre la política de actualizaciones](https://en.kilho.net/archives/notice/2940).

## Licencia

BoostPing es **freeware**. Puede usarlo gratis en cualquier lugar —en el trabajo, en casa, en organismos públicos o en centros educativos— y redistribuirlo libremente.

## Enlaces

- Sitio web: <https://kilho.net/boostping>
- Foro: <https://kilho.top/forum/qna>
- X (Twitter): <https://www.twitter.com/kilhonet>

© KILHO.NET
