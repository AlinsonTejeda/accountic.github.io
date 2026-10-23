# Accountic

Sitio web oficial de **Accountic**, servicios de constitución de empresas (SRL) e igualas de contabilidad en República Dominicana, con atención a emprendedores locales y extranjeros.

🌐 **Sitio en vivo:** https://alinsontejeda.github.io/accountic.github.io/

---

## Contenido del sitio

- **Inicio:** propuesta de valor, botones de contacto y precios de referencia.
- **Por qué Accountic:** acompañamiento personalizado, claridad en procesos y precios, atención a clientes locales y extranjeros, y orientación fiscal y administrativa.
- **Extranjeros:** información para quienes desean constituir una empresa en el país.
- **Constitución de empresa SRL:** Plan Básico y Plan Premium, con comparación completa de servicios.
- **Registro de nombre comercial:** servicio adicional.
- **Igualas de contabilidad:** Básica, Microempresas y Pro, con comparación completa.
- **Cómo funciona:** proceso de contratación en cuatro pasos.
- **Preguntas frecuentes** en formato desplegable.
- **Sobre Accountic y contacto:** WhatsApp, correo e Instagram.

## Características

- Sitio **bilingüe (español / inglés)** con selector ES/EN. El idioma se recuerda entre visitas y se detecta según el navegador.
- **Moneda automática según el idioma:** en español los precios se muestran en pesos dominicanos (RD$) y en inglés se convierten a dólares (US$) con una tasa de referencia configurable.
- **Diseño adaptable** a computadoras, tabletas y celulares.
- Compatible con **modo claro y modo oscuro** del dispositivo.
- Botones de **WhatsApp** con mensajes precargados según el plan o servicio elegido.
- Animaciones sutiles que se desactivan si el usuario tiene activada la opción de movimiento reducido.
- Pensado para accesibilidad: navegación por teclado, contraste adecuado y textos alternativos.

## Tecnología

Es un sitio estático de **un solo archivo**:

- HTML, CSS y JavaScript puro (sin frameworks ni dependencias de instalación).
- Logotipos e imágenes incrustados en el propio archivo.
- Tipografías [Figtree](https://fonts.google.com/specimen/Figtree) y [Sora](https://fonts.google.com/specimen/Sora) desde Google Fonts.

```
accountic.github.io/
├── index.html   # Toda la página (estilos, scripts, imágenes y textos)
└── README.md    # Este archivo
```

## Cómo publicarlo con GitHub Pages

1. Sube `index.html` a la raíz del repositorio.
2. Ve a **Settings → Pages**.
3. En **Source** elige **Deploy from a branch**, selecciona la rama `main` y la carpeta `/ (root)`, y guarda.
4. Espera uno o dos minutos. El sitio quedará disponible en la dirección indicada arriba.

Para actualizarlo, reemplaza `index.html` con la versión nueva y confirma el cambio (**Commit changes**). Si no ves el cambio, recarga con `Ctrl + F5`.

## Cómo editar el contenido

Todo está dentro de `index.html`. Estos son los puntos más comunes:

### Tasa de cambio (RD$ → US$)

Al inicio del bloque `<script>` está la configuración de moneda:

```js
var DOP_PER_USD=60;  // Tasa de referencia configurable (no es una tasa oficial)
var USD_FIXED={};    // Opcional: precios fijos en USD por monto en DOP. Ej.: {24000:400}
```

- Cambia `DOP_PER_USD` para actualizar la conversión de todos los precios.
- Usa `USD_FIXED` si prefieres definir precios fijos en dólares en lugar de conversiones automáticas.
- Los precios en dólares son una referencia basada en esa tasa, no una tarifa oficial.

### Precios y planes

Los precios originales siempre se escriben en pesos dominicanos con el formato `RD$ 24,000`. Para cambiarlos, busca `RD$` dentro de `index.html`: aparecen en las tarjetas de la parte superior, en los planes de constitución e igualas (variables `SRL` e `IG` del script), en el servicio de nombre comercial y en las preguntas frecuentes. Mantén el mismo formato para que la conversión a dólares siga funcionando.

### Textos en inglés

Las traducciones están en el objeto `EN` del script. Cada texto de la página tiene un atributo `data-t` que lo enlaza con su traducción: si cambias un texto en español, actualiza también su equivalente en `EN`.

### Contacto

Los números de WhatsApp, el correo y el enlace de Instagram se encuentran en la sección de contacto y en los botones con atributo `data-wa`.

## Contacto

- 📍 Verón, Bávaro, Punta Cana, República Dominicana
- 📧 aartejeda@hotmail.com
- 💬 WhatsApp: 849-655-8702 / 829-945-1328
- 📸 Instagram: [@mt_accountic](https://www.instagram.com/mt_accountic/)

## Derechos

© Accountic. Todos los derechos reservados. El contenido, los logotipos y los textos de este sitio no pueden copiarse ni reutilizarse sin autorización.
