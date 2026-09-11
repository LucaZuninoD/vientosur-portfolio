# Luca Zunino — Portfolio

> Desarrollador Full Stack · Java / Spring Boot · Angular
> Córdoba, Argentina · disponible para posiciones full-time

**→ [Ver el portfolio](https://vientosur-portfolio.vercel.app/)**

> Si estás leyendo esto en local, abrí `index.html` directamente en el navegador: es una sola
> página estática, sin build ni dependencias que instalar.

---

## Qué es

El portfolio de Luca Zunino. Su eje es **VientoSur** ([vientosur.tech](https://vientosur.tech)),
una plataforma de empleo y ATS con matching por IA **en producción** — proyecto propio,
cofundado con dos socios y autofinanciado, del que Luca escribió la totalidad del código.

La página incluye una **demo interactiva real**: una reimplementación en JavaScript del heurístico
de afinidad que corre en producción (`SuggestionService.getSuggestedOffers`), con los mismos pesos
por señal —área, tecnologías, modalidad, ubicación, jornada, salario y el bonus combinado— y el
mismo techo de 110 puntos. No es una captura ni un video: es el cálculo corriendo en el navegador.

## Secciones

| Sección | Qué contesta |
|---|---|
| Hero | Quién es y qué construyó, con el enlace a la plataforma en línea |
| Sobre mí | Trayectoria académica y profesional, idiomas |
| Habilidades | Lo que usa, agrupado por capa — sólo lo que está puesto en un proyecto real |
| VientoSur | Cifras del sistema, funcionalidades, el tablero del producto y el stack por capa |
| Demo en vivo | El motor de matching, interactivo |
| Desafíos | Cuatro decisiones técnicas, incluida una que estuvo mal tres despliegues seguidos |
| Cómo trabajo | Specs, documentación verificada, registro de deuda, suite en verde |
| Otro proyecto | Sistema de Gestión de Consorcios (UTN, Stripe/MercadoPago, Scrum) |

## De dónde salen las cifras

Las cifras de la sección VientoSur **no se escriben a mano**: salen del inventario que genera
`.kiro/scripts/inventario.mjs` del workspace de VientoSur contra el código, más el conteo de
endpoints del paquete `controller` y el baseline de tests del repo meta.

**Última verificación: 11/09/2026.** Al actualizarlas, re-verificar —no copiar de una versión
anterior de esta página—:

```bash
node .kiro/scripts/inventario.mjs --check
```

## Identidad visual

El portfolio usa **el mismo sistema de diseño que la landing de VientoSur**, no una imitación:
los tokens del bloque `:root` de `index.html` son un port literal de
`vientosur-frontend/src/app/styles/_vs-public.scss` — las mismas dos familias tipográficas
(**Archivo** display + **Work Sans** texto), el mismo gradiente `#667eea → #764ba2`, los mismos
radios, sombras y bandas de sección con hairline.

Eso es deliberado: hoy VientoSur es la carta de presentación de Luca, y conviene que el portfolio
y el producto se lean como una sola marca. Si el sistema de diseño de la plataforma cambia, este
archivo es el lugar donde mirar para saber qué hay que sincronizar.

Igual que la landing v3, la página **no usa figuras decorativas** —auroras, orbes, blobs—: el color
lo aportan el tinte de las bandas y el gradiente de marca.

## Stack de VientoSur (lo que la página describe)

| Capa | Tecnologías |
|---|---|
| Backend | Java 21, Spring Boot 3.2.4, Spring Security (JWT access + refresh), Bucket4j, Apache PDFBox / Tika / iText, AWS SDK, Google Calendar API, OWASP Dependency-Check |
| Frontend | Angular 22 (standalone + SSR), TypeScript, RxJS, Bootstrap 5 + SCSS |
| Base de datos | PostgreSQL 17 — 79 entidades JPA, 71 repositorios |
| IA | Cohere (chat LLM, con prefiltrado heurístico propio) · Gemini Live (entrevista por voz vía WebRTC) |
| Infraestructura | Docker + Compose, Nginx, AWS S3, desplegado sobre Coolify |

## Archivos

```
index.html            # la página entera: markup, estilos y la demo. Sin build.
CV-Luca-Zunino.pdf    # el CV que enlaza el botón "Descargar CV"
logo2.png             # logo de VientoSur (favicon + tarjeta del hero)
screenshots/          # capturas del producto — no se usan en la página (están desactualizadas)
```

## Contacto

**Luca Zunino** — lucazuninod@gmail.com
[LinkedIn](https://www.linkedin.com/in/lucazuninod/) · [GitHub](https://github.com/LucaZuninoD) · [VientoSur](https://vientosur.tech)
