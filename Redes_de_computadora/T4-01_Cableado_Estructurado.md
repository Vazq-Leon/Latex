# Actividad T4-01: Investigación sobre normas y estándares de cableado estructurado

Documento de trabajo (conceptos, ideas y fuentes). Fecha límite: 28 de octubre de 2026, 23:59. Entrega en equipo; se permiten varios envíos.

Leyenda de marcas usadas en este archivo:

- `[URL]` enlace a fuente oficial o primaria.
- `[VERIFICAR]` dato que debe confirmarse en la fuente antes de citarlo (edición vigente, número de página, valor exacto).
- `[PENDIENTE]` espacio para que el equipo complete.

Nota importante: los textos completos de las normas ANSI/TIA e ISO/IEC son de pago. Lo que se puede citar libremente son las páginas oficiales de cada organismo, los resúmenes públicos y documentos de fabricantes que las interpretan. Hay que indicar en el trabajo cuándo se usó una fuente secundaria.

---

## 0. Estructura exigida por la actividad

Checklist del entregable:

- [ ] Portada
- [ ] Introducción
- [ ] Desarrollo (6 temas, ver sección 2 a 7 de este archivo)
- [ ] Tabla comparativa
- [ ] Ejemplos de aplicación
- [ ] Conclusiones
- [ ] Referencias en formato APA 7

Datos de portada `[PENDIENTE]`: institución, carrera, materia (Redes de Computadoras), nombre de la actividad, integrantes del equipo, docente, fecha.

---

## 1. Introducción (ideas para redactar)

Ideas a cubrir en 1 o 2 párrafos:

- Toda red (LAN, Wi-Fi, VoIP, videovigilancia, IoT) depende de una infraestructura física; si esa base es desordenada, la red es difícil de mantener y de crecer.
- El cableado estructurado responde a eso: un sistema normalizado, independiente de la aplicación y del fabricante.
- Las normas dan un lenguaje común entre diseñadores, instaladores, fabricantes y administradores.
- Objetivo del trabajo: describir el concepto, las normas, las configuraciones T568A/T568B, las categorías de cable, los componentes y un caso de aplicación.

---

## 2. Concepto, características y beneficios del cableado estructurado

### 2.1 Concepto

Un sistema de cableado estructurado es un conjunto de cables, conectores, hardware de conexión y canalizaciones, diseñado bajo normas, que ofrece una infraestructura de telecomunicaciones genérica y flexible para voz, datos, video y sistemas de control de un edificio o campus.

Idea clave: se instala una sola vez una infraestructura estándar y después se asigna el servicio (datos, voz, cámaras) mediante cambios en el panel de parcheo, sin recablear.

### 2.2 Subsistemas (según el modelo de TIA-568 / ISO 11801)

| Subsistema | Descripción breve |
|---|---|
| Área de trabajo | Salida de telecomunicaciones (jack) y cordón hacia el equipo del usuario |
| Cableado horizontal | Del área de trabajo al cuarto de telecomunicaciones; máximo 90 m de enlace permanente |
| Cuarto de telecomunicaciones (TR / IDF) | Alberga patch panels, switches y equipo activo por piso |
| Cableado vertical o backbone | Une cuartos de telecomunicaciones, sala de equipos y entrada de servicios |
| Sala de equipos (ER / MDF) | Equipos principales: servidores, core, enrutadores |
| Entrada de servicios | Punto donde llegan los proveedores externos (ISP, telefonía) |
| Administración | Etiquetado, registros y documentación (TIA-606) |

`[PENDIENTE]` Incluir un diagrama propio de la topología en estrella jerárquica (MDF - IDF - área de trabajo).

### 2.3 Características

- Topología en estrella jerárquica.
- Independiente del fabricante y de la aplicación.
- Modular y escalable.
- Longitudes máximas normalizadas: 90 m de enlace permanente más hasta 10 m de cordones, para un canal de 100 m en cable de par trenzado.
- Pruebas de certificación con equipo especializado (por ejemplo, parámetros de pérdida de inserción, NEXT, pérdida de retorno).
- Documentación y etiquetado obligatorios.
- Vida útil esperada alta (tradicionalmente se menciona de 10 a 15 años o más) `[VERIFICAR en fuente de fabricante o norma]`.

### 2.4 Beneficios

- Facilidad de administración: movimientos, altas y cambios (MAC) rápidos.
- Menor tiempo de diagnóstico de fallas gracias al etiquetado y la topología.
- Escalabilidad: se soportan nuevas velocidades con el mismo diseño al cambiar la categoría.
- Rendimiento predecible y certificable.
- Compatibilidad multiproveedor.
- Mejor estética y seguridad (orden, menos riesgos de tropiezo, mejor flujo de aire en gabinetes).
- Menor costo total a largo plazo frente a cableado improvisado.

Contraste útil para el trabajo: cableado no estructurado (punto a punto, sin etiquetas, distintos cables por servicio) frente a estructurado.

### 2.5 Fuentes sugeridas para esta sección

- TIA, página de estándares: https://tiaonline.org/products-and-services/tia-standards/ `[VERIFICAR ruta exacta]`
- ISO/IEC 11801-1:2017, ficha oficial: https://www.iso.org/standard/66182.html `[VERIFICAR]`
- Libros de texto de redes (ver sección de referencias), por ejemplo Forouzan o Tanenbaum, para el concepto general.

---

## 3. Normas y estándares: ANSI/TIA-568, ISO/IEC 11801 y ANSI/TIA-606

### 3.1 ANSI/TIA-568

Organismo: Telecommunications Industry Association (TIA), acreditada por ANSI (American National Standards Institute). Región de influencia principal: América.

Es una familia de documentos `[VERIFICAR edición vigente de cada uno en https://tiaonline.org y https://webstore.ansi.org]`:

| Parte | Tema |
|---|---|
| ANSI/TIA-568.0 | Requisitos genéricos de cableado de telecomunicaciones para instalaciones de clientes |
| ANSI/TIA-568.1 | Cableado de telecomunicaciones para edificios comerciales |
| ANSI/TIA-568.2 | Cableado y componentes de par trenzado balanceado (aquí se definen Cat 5e, 6, 6A y los requisitos de pruebas) |
| ANSI/TIA-568.3 | Cableado y componentes de fibra óptica |
| ANSI/TIA-568.4 | Cableado y componentes de banda ancha (coaxial) |
| ANSI/TIA-568.5 | Cableado de par trenzado de un solo par (Single Pair Ethernet) `[VERIFICAR]` |

Ideas a desarrollar: qué define (topología, distancias, medios reconocidos, conectores, rendimiento, pruebas), y que el esquema de pines T568A/T568B pertenece a esta familia.

Normas relacionadas de TIA que conviene mencionar brevemente:

- ANSI/TIA-569: rutas y espacios de telecomunicaciones (canalizaciones).
- ANSI/TIA-607: puesta a tierra y conexión equipotencial.
- ANSI/TIA-942: infraestructura de centros de datos.

### 3.2 ISO/IEC 11801

Organismo: ISO (International Organization for Standardization) en conjunto con IEC (International Electrotechnical Commission). Alcance internacional.

- ISO/IEC 11801-1: requisitos generales de cableado genérico para instalaciones de clientes.
- ISO/IEC 11801-2: edificios de oficinas.
- ISO/IEC 11801-3: entornos industriales.
- ISO/IEC 11801-4: viviendas unifamiliares.
- ISO/IEC 11801-5: centros de datos.
- ISO/IEC 11801-6: sistemas distribuidos de servicios de edificio.

`[VERIFICAR]` la lista y años de edición en la ficha oficial: https://www.iso.org/standard/66182.html y en el catálogo del comité ISO/IEC JTC 1/SC 25: https://www.iso.org/committee/45374.html `[VERIFICAR]`.

Diferencia de nomenclatura que conviene explicar:

| Concepto | TIA (América) | ISO/IEC (internacional) |
|---|---|---|
| Nivel de rendimiento de componentes | Categoría (Cat 5e, 6, 6A) | Categoría de componente (Cat 5, 6, 6A) |
| Nivel de rendimiento de canal/enlace | Se expresa con la misma categoría | Clase (D, E, EA, F, FA) |
| Cuarto principal | MDF / ER | Distribuidor de campus o de edificio |
| Cuarto por piso | IDF / TR | Distribuidor de piso |

Equivalencias habituales: Cat 5e corresponde a Clase D; Cat 6 a Clase E; Cat 6A a Clase EA. `[VERIFICAR en documento de fabricante o ficha de norma]`

### 3.3 ANSI/TIA-606

Título: norma de administración para infraestructura de telecomunicaciones. Edición citada con frecuencia: ANSI/TIA-606-C (2017) `[VERIFICAR si existe edición posterior]`.

Ideas a desarrollar:

- Define cómo identificar y documentar: cables, paneles, puertos, espacios, canalizaciones, tierras.
- Esquema de identificadores (por ejemplo, formato cuarto-panel-puerto).
- Reglas de etiquetado (legibilidad, durabilidad, ubicación).
- Registros: planos, hojas de cálculo o software de administración de infraestructura.
- Clases de administración (de menor a mayor complejidad según el tamaño de la instalación) `[VERIFICAR número de clases y definición]`.
- Código de color de etiquetas/campos para tipos de terminación `[VERIFICAR]`.

### 3.4 Fuentes para esta sección

- TIA (sitio oficial): https://tiaonline.org
- ANSI Webstore (compra y fichas de normas): https://webstore.ansi.org
- ISO (ficha de ISO/IEC 11801-1): https://www.iso.org/standard/66182.html `[VERIFICAR]`
- IEC Webstore: https://webstore.iec.ch `[VERIFICAR ruta de la ficha]`
- Documentos técnicos de fabricantes (CommScope, Panduit, Belden, Siemon) que resumen las normas; útiles como fuente secundaria `[PENDIENTE elegir 1 o 2 y copiar URL exacta]`.

---

## 4. Configuraciones T568A y T568B

### 4.1 Idea general

Ambas definen el orden de los 8 hilos (4 pares) en el conector RJ45 / jack de 8 posiciones. Los pares se identifican por color: verde, naranja, azul y marrón; cada par tiene un hilo de color sólido y otro blanco con franja del mismo color.

Los dos esquemas son eléctricamente equivalentes; solo se intercambian los pares naranja y verde. Lo importante es usar el mismo en toda la instalación y en ambos extremos de un cable directo.

### 4.2 Tabla de pines (conector RJ45 visto de frente, clip hacia abajo, pin 1 a la izquierda)

| Pin | T568A | T568B |
|---|---|---|
| 1 | Blanco/Verde | Blanco/Naranja |
| 2 | Verde | Naranja |
| 3 | Blanco/Naranja | Blanco/Verde |
| 4 | Azul | Azul |
| 5 | Blanco/Azul | Blanco/Azul |
| 6 | Naranja | Verde |
| 7 | Blanco/Marrón | Blanco/Marrón |
| 8 | Marrón | Marrón |

`[VERIFICAR contra la norma o una hoja de fabricante antes de entregar]`

### 4.3 Diagrama sugerido (ASCII, para reemplazar por imagen propia)

```
Pin:        1     2     3     4     5     6     7     8
T568A:    b-ver  ver  b-nar  azul  b-azul nar  b-mar  mar
T568B:    b-nar  nar  b-ver  azul  b-azul ver  b-mar  mar

Pares (T568B):  Par 1 = 4,5 (azul)   Par 2 = 1,2 (naranja)
                Par 3 = 3,6 (verde)  Par 4 = 7,8 (marrón)
```

`[PENDIENTE]` Hacer un diagrama gráfico propio (puede hacerse con TikZ en el repositorio LaTeX o con draw.io) para evitar problemas de derechos de imagen, y citar la norma como fuente del esquema.

### 4.4 Tipos de cable según el uso

| Tipo | Extremo 1 | Extremo 2 | Uso clásico |
|---|---|---|---|
| Directo | T568B | T568B | PC a switch, switch a router |
| Cruzado | T568A | T568B | Equipos iguales (hoy poco necesario por Auto-MDI/MDI-X) |

Idea: la mayoría de las interfaces Gigabit actuales implementan Auto-MDI/MDI-X, por lo que el cable cruzado dejó de ser necesario. `[VERIFICAR con IEEE 802.3, cláusula de Auto-Negotiation / MDI-X]`

### 4.5 Por qué hay dos

- T568A fue el esquema recomendado en la versión original por compatibilidad con cableado telefónico USOC en ciertos entornos y es el requerido en instalaciones del gobierno de EE. UU.
- T568B proviene del esquema AT&T 258A y es el más usado comercialmente en América. `[VERIFICAR historia en fuente secundaria confiable]`

### 4.6 Fuentes

- Norma ANSI/TIA-568.2 (esquemas de terminación): https://webstore.ansi.org `[VERIFICAR ficha]`
- IEEE 802.3 (Ethernet), página oficial: https://standards.ieee.org/ieee/802.3/ `[VERIFICAR]`
- Guías de terminación de fabricantes (Panduit, Siemon, Belden) con diagramas `[PENDIENTE URL]`.

---

## 5. Categorías de cable de par trenzado: Cat 5e, Cat 6 y Cat 6A

### 5.1 Datos técnicos de referencia

| Característica | Cat 5e | Cat 6 | Cat 6A |
|---|---|---|---|
| Clase ISO/IEC equivalente | D | E | EA |
| Ancho de banda especificado | 100 MHz | 250 MHz | 500 MHz |
| Velocidad típica soportada a 100 m | 1 Gbps (1000BASE-T) | 1 Gbps (1000BASE-T); 10 Gbps en tramos cortos (aprox. 37 a 55 m según ruido alienígena) | 10 Gbps (10GBASE-T) a 100 m |
| Estándar Ethernet asociado | IEEE 802.3ab | IEEE 802.3ab / 802.3an (distancia reducida) | IEEE 802.3an |
| Diámetro y rigidez | Menor | Mayor (a veces con separador) | Mayor aún |
| Blindaje | UTP, o F/UTP | UTP, F/UTP, S/FTP | UTP o blindado (F/UTP, U/FTP, S/FTP) |
| Costo relativo | Bajo | Medio | Alto |
| Uso recomendado hoy | Instalaciones básicas, ampliaciones | Estándar general de oficinas | Instalaciones nuevas con vista a futuro, Wi-Fi 6/6E/7, PoE de alta potencia |

`[VERIFICAR todos los valores contra ANSI/TIA-568.2 o ficha técnica de fabricante]`

### 5.2 Ideas a desarrollar

- Par trenzado: el trenzado reduce la interferencia y la diafonía (crosstalk).
- Parámetros: atenuación (pérdida de inserción), NEXT/FEXT, pérdida de retorno, ACR, ruido alienígena (AXT) en 10GBASE-T.
- UTP frente a blindados: notación U/UTP, F/UTP, U/FTP, S/FTP (norma ISO/IEC 11801 y 24739).
- Conductor sólido (cableado horizontal) frente a trenzado de hilos (patch cords).
- Distancia máxima: 100 m de canal para Ethernet de par trenzado.
- PoE (IEEE 802.3af/at/bt): más potencia genera más calentamiento en haces de cable, lo que favorece a Cat 6A. `[VERIFICAR]`
- Categorías superiores (Cat 7, 8) solo mencionarlas como nota; el alcance del trabajo es 5e, 6 y 6A. Cat 7 es una categoría ISO/IEC y no está reconocida por TIA. `[VERIFICAR]`

### 5.3 Fuentes

- ANSI/TIA-568.2: https://webstore.ansi.org `[VERIFICAR ficha]`
- IEEE 802.3 (1000BASE-T, 10GBASE-T): https://standards.ieee.org/ieee/802.3/ `[VERIFICAR]`
- Páginas técnicas de fabricantes con tablas de categorías `[PENDIENTE URL]`.

---

## 6. Componentes de una instalación

### 6.1 Lista y descripción

| Componente | Función | Puntos a mencionar |
|---|---|---|
| Cable horizontal (UTP/STP) | Enlace entre cuarto de telecomunicaciones y área de trabajo | Sólido, hasta 90 m, LSZH o CMR/CMP según el recorrido (plenum) |
| Patch panel | Punto de terminación de cables horizontales en el rack | Terminación tipo 110 / punch-down, 24 o 48 puertos, 1U o 2U, categoría debe coincidir con el cable |
| Jack (keystone / salida de telecomunicaciones) | Terminación en el área de trabajo y en el panel | Esquema T568A/B marcado en el jack, tipo keystone, categoría |
| Faceplate / caja de pared | Soporte del jack | 1, 2 o 4 puertos |
| Conector RJ45 (8P8C) | Terminación de patch cords | Macho modular, versión para hilo sólido o trenzado |
| Patch cord (cordón de parcheo) | Conecta equipo con jack o panel con switch | Hecho de fábrica, hilo trenzado, máximo 5 m en área de trabajo y 5 m en TR aprox. `[VERIFICAR]` |
| Canalizaciones | Protegen y organizan el cableado | Charola (cable tray), tubería conduit EMT/PVC, canaleta, ducto bajo piso, ducto plafón |
| Gabinete / rack | Alojan equipos y paneles | 19 pulgadas, unidades de rack (U), organizadores horizontales y verticales |
| Organizadores de cable | Mantienen radios de curvatura y orden | Radio mínimo habitual 4 veces el diámetro del cable para UTP `[VERIFICAR]` |
| Sistema de puesta a tierra | Seguridad y reducción de ruido | TIA-607 `[VERIFICAR edición]` |
| Firestop (sellos cortafuego) | Mantienen compartimentación de incendio | Pasos por muros y pisos |

### 6.2 Ideas a desarrollar

- Mostrar el recorrido completo de una señal: PC, patch cord, jack, cable horizontal, patch panel, patch cord, switch.
- Mencionar el canal frente al enlace permanente: el enlace permanente excluye los patch cords; el canal los incluye.
- Mencionar separación entre cableado de datos y de energía eléctrica `[VERIFICAR distancias en TIA-569 o NOM]`.
- Contexto México: la instalación eléctrica y de telecomunicaciones también se rige por normas locales (NOM-001-SEDE para instalaciones eléctricas). `[VERIFICAR si aplica a lo investigado]`

### 6.3 Fuentes

- ANSI/TIA-569 (rutas y espacios): https://webstore.ansi.org `[VERIFICAR ficha]`
- ANSI/TIA-568.2 y 568.1 para jacks, patch cords y longitudes.
- Catálogos y guías de instalación de fabricantes `[PENDIENTE URL]`.

---

## 7. Ejemplo de aplicación: red LAN de una institución educativa

Propuesta de caso (el equipo puede ajustar los números): un plantel de 3 edificios.

### 7.1 Escenario `[PENDIENTE adaptar]`

- Edificio A (administración): 2 plantas, 40 salidas de usuario.
- Edificio B (aulas): 3 plantas, 90 salidas (incluye puntos para access points).
- Edificio C (laboratorios de cómputo): 2 plantas, 80 salidas.
- Sala de servidores principal en el Edificio A.

### 7.2 Mapa de aplicación de los estándares

| Elemento de diseño | Norma o criterio aplicado |
|---|---|
| Topología en estrella jerárquica | ANSI/TIA-568.0 y 568.1 |
| Horizontal: Cat 6A, enlaces menores a 90 m | ANSI/TIA-568.2 |
| Backbone entre edificios: fibra óptica monomodo/multimodo | ANSI/TIA-568.3 `[VERIFICAR tipo de fibra recomendado]` |
| Esquema de terminación T568B en todos los jacks y paneles | ANSI/TIA-568.2 |
| Charolas y ductos, espacios para cuartos de telecomunicaciones | ANSI/TIA-569 |
| Puesta a tierra de racks y charolas | ANSI/TIA-607 |
| Etiquetado, planos y hoja de registro | ANSI/TIA-606 |
| Certificación del enlace con equipo de prueba | ANSI/TIA-568.2, reporte por punto |
| Referencia internacional equivalente (Clase EA) | ISO/IEC 11801 |

### 7.3 Propuesta de diseño

- Un MDF en el Edificio A y un IDF por planta o por edificio.
- Dos salidas (jacks) por área de trabajo: una para datos y otra de respaldo/telefonía IP.
- Puntos adicionales en techo para access points (con PoE), Cat 6A.
- Etiquetado de ejemplo según TIA-606: `B2-IDF1-PP1-24` (edificio B, nivel 2, rack 1, panel 1, puerto 24) `[PENDIENTE: adaptar al formato de TIA-606]`.
- Documentación entregable: planos, tabla de etiquetas, reportes de pruebas.

### 7.4 Diagrama sugerido

`[PENDIENTE]` Diagrama de bloques: Entrada de servicios, MDF, fibra a IDF-B y IDF-C, horizontal a salidas, access points.

### 7.5 Ejemplo alternativo (empresa)

Una oficina de 50 usuarios en un solo piso, con un cuarto de telecomunicaciones, Cat 6, 2 salidas por puesto, switch PoE para teléfonos IP y cámaras. Puede usarse como segundo ejemplo si se pide más de uno ("ejemplos de aplicación").

---

## 8. Tabla comparativa (propuesta para el entregable)

### 8.1 Comparativa de normas

| Aspecto | ANSI/TIA-568 | ISO/IEC 11801 | ANSI/TIA-606 |
|---|---|---|---|
| Organismo | TIA / ANSI | ISO / IEC | TIA / ANSI |
| Alcance geográfico | Principalmente América | Internacional | Principalmente América |
| Enfoque | Diseño, componentes, rendimiento y pruebas | Cableado genérico para instalaciones de clientes | Administración, etiquetado y documentación |
| Unidad de rendimiento | Categoría (5e, 6, 6A) | Clase (D, E, EA) y categoría de componentes | No aplica |
| Cubre medios | Par trenzado, fibra, coaxial | Par trenzado, fibra | Cualquier medio instalado |
| Ejemplo de contenido | Pines T568A/T568B, 90 m + 10 m | Clases de enlace, tipos de distribuidores | Esquema de identificadores y registros |

### 8.2 Comparativa de configuraciones

| Aspecto | T568A | T568B |
|---|---|---|
| Par naranja | Pines 3 y 6 | Pines 1 y 2 |
| Par verde | Pines 1 y 2 | Pines 3 y 6 |
| Uso típico | Gobierno de EE. UU., instalaciones nuevas residenciales | Entornos comerciales en general |
| Compatibilidad eléctrica | Equivalente | Equivalente |

### 8.3 Comparativa de categorías

Reutilizar la tabla de la sección 5.1.

---

## 9. Conclusiones (ideas para redactar)

- El cableado estructurado es la base física que determina la vida útil, el rendimiento y la facilidad de gestión de una red.
- Las normas no compiten sino que se complementan: TIA-568 y ISO/IEC 11801 definen cómo construir; TIA-606 cómo administrar; TIA-569 y 607 los espacios y la tierra.
- T568A y T568B son equivalentes; lo crítico es la coherencia en toda la instalación.
- La elección de categoría es un balance entre costo y proyección a futuro; hoy Cat 6A es la opción más sensata para instalaciones nuevas con Wi-Fi moderno y PoE, y Cat 5e solo para casos limitados. `[Opinión del equipo: justificar]`
- La certificación y la documentación son tan importantes como el cable mismo.
- `[PENDIENTE]` Aprendizaje personal del equipo y dificultades al investigar (por ejemplo, normas de pago).

---

## 10. Referencias en formato APA 7

### 10.1 Plantillas APA 7 para este trabajo

Norma o estándar (autor = organización):

```
Telecommunications Industry Association. (Año). Título de la norma (ANSI/TIA-XXX-X). Editorial/URL.
```

Página web de organización:

```
Organización. (Año, día mes). Título de la página. Nombre del sitio. URL
```

Libro:

```
Apellido, A. A. (Año). Título del libro en cursiva (n.ª ed.). Editorial.
```

Reglas rápidas: sangría francesa, orden alfabético por autor, citas en texto como (Telecommunications Industry Association [TIA], 2018) la primera vez y (TIA, 2018) después. Si no hay fecha: (s. f.).

### 10.2 Borrador de referencias `[VERIFICAR años, números de edición y URLs antes de entregar]`

```
American National Standards Institute. (s. f.). ANSI webstore. https://webstore.ansi.org

Institute of Electrical and Electronics Engineers. (s. f.). IEEE 802.3 Ethernet working group. https://standards.ieee.org/ieee/802.3/  [VERIFICAR]

International Organization for Standardization. (2017). Information technology: Generic cabling for customer premises. Part 1: General requirements (ISO/IEC 11801-1:2017). https://www.iso.org/standard/66182.html  [VERIFICAR]

Telecommunications Industry Association. (s. f.). TIA standards. https://tiaonline.org

Telecommunications Industry Association. (2017). Administration standard for telecommunications infrastructure (ANSI/TIA-606-C). [VERIFICAR editorial y URL]

Telecommunications Industry Association. (2018). Balanced twisted-pair telecommunications cabling and components standard (ANSI/TIA-568.2-D). [VERIFICAR año, editorial y URL]

Telecommunications Industry Association. (2018). Generic telecommunications cabling for customer premises (ANSI/TIA-568.0-D). [VERIFICAR año, edición y URL]
```

Si se usa una fuente secundaria (libro o fabricante), agregarla en el mismo formato:

```
[PENDIENTE] Forouzan, B. A. (Año). Data communications and networking (n.ª ed.). McGraw-Hill.
[PENDIENTE] Fabricante. (Año). Título del documento técnico. URL
```

---

## 11. Plan de trabajo sugerido para el equipo

| Tarea | Responsable | Estado |
|---|---|---|
| Portada e introducción | [PENDIENTE] | |
| Sección 2: concepto y beneficios | [PENDIENTE] | |
| Sección 3: normas | [PENDIENTE] | |
| Sección 4: T568A/T568B y diagramas | [PENDIENTE] | |
| Sección 5: categorías | [PENDIENTE] | |
| Sección 6: componentes | [PENDIENTE] | |
| Sección 7: caso de aplicación y diagrama | [PENDIENTE] | |
| Tabla comparativa y conclusiones | [PENDIENTE] | |
| Referencias APA 7 y revisión final | [PENDIENTE] | |

Recomendación de formato final: como el repositorio ya usa LaTeX, este contenido puede pasarse a un `.tex` (portada, secciones, `tabular` para las tablas, TikZ para el diagrama T568A/B y `biblatex` con estilo APA para las referencias). `[Opcional]`

---

## 12. Lista de URLs de consulta

| Recurso | URL |
|---|---|
| TIA (Telecommunications Industry Association) | https://tiaonline.org |
| ANSI Webstore (fichas de normas TIA) | https://webstore.ansi.org |
| ISO/IEC 11801-1:2017 | https://www.iso.org/standard/66182.html `[VERIFICAR]` |
| IEC Webstore | https://webstore.iec.ch |
| IEEE 802.3 Ethernet | https://standards.ieee.org/ieee/802.3/ `[VERIFICAR]` |
| Guía de estilo APA 7 (APA oficial) | https://apastyle.apa.org |
