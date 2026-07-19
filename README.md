# 🌋 Observatorio Vulcanológico Virtual

**Simulador interactivo de erupciones volcánicas** — una herramienta educativa que representa el ascenso del magma y los productos que un volcán puede generar en superficie.

[![Ver simulador](https://img.shields.io/badge/▶_Abrir_simulador-en_vivo-ec6021?style=for-the-badge)](https://jorgealpala.github.io/observatorio-vulcanologico-virtual/)

[![HTML5](https://img.shields.io/badge/HTML5-single_file-e34f26?logo=html5&logoColor=white)](#tecnologías)
[![Three.js](https://img.shields.io/badge/Three.js-r128-000000?logo=three.js&logoColor=white)](#tecnologías)
[![Sin dependencias](https://img.shields.io/badge/build-no%20requiere-52d6cf)](#uso-local)
[![Uso académico](https://img.shields.io/badge/uso-académico-f7b733)](#alcance-y-limitaciones)
[![Licencia: MIT](https://img.shields.io/badge/licencia-MIT-9aa6b8)](LICENSE)

🔗 **Acceso directo:** <https://jorgealpala.github.io/observatorio-vulcanologico-virtual/>

---

## Descripción

El *Observatorio Vulcanológico Virtual* simula, de forma esquemática e interactiva, el comportamiento de un volcán desde el reposo hasta el declive de una erupción. La interfaz reproduce el aspecto de una consola de monitoreo geofísico y permite modificar en tiempo real los parámetros del magma y de la atmósfera para observar cómo cambian los productos emitidos, su alcance y el estado de alerta.

Está pensado como **apoyo docente y de divulgación** en temas de vulcanología y gestión del riesgo: no es un modelo de pronóstico ni una evaluación oficial de amenaza.

---

## Captura

> Añade una captura de la interfaz en `docs/captura.png` y descomenta la línea siguiente:
>
> <!-- ![Interfaz del simulador](docs/captura.png) -->

---

## Características

### Vistas sincronizadas

Todas las vistas comparten un mismo motor de simulación, de modo que responden simultáneamente a los mismos parámetros.

| Vista | Contenido |
|---|---|
| **Perfil** | Corte vertical del edificio volcánico: cámara magmática, conducto, cráter, columna eruptiva y productos en superficie. |
| **Planta** | Vista cenital con dispersión de ceniza (isópacas), alcances en kilómetros, drenajes y proyección de la cámara magmática. |
| **3D** | Edificio volcánico procedural con órbita manual (arrastrar para rotar, rueda para acercar), pluma de partículas y flujos sobre la ladera. |
| **Completa** | Las tres vistas anteriores de forma simultánea. |
| **Conceptos** | Glosario técnico de apoyo (ver más abajo). |

### Controles

- **Escenarios predefinidos:** volcán efusivo, estratovolcán explosivo, volcán con glaciar, erupción pliniana mayor y configuración personalizada.
- **Estilos eruptivos:** hawaiana, estromboliana, vulcaniana y pliniana.
- **Parámetros del magma:** índice de explosividad (VEI 0–6), viscosidad/composición (basáltico → riolítico) y contenido de volátiles (0–100 %).
- **Condiciones del terreno y la atmósfera:** casquete glaciar (habilita lahares), dirección del viento mediante dial y velocidad (0–140 km/h).
- **Control de la erupción:** iniciar ascenso de magma, desencadenar erupción, **pausar/reanudar** y reiniciar.

### Fenómenos representados

- Dispersión de piroclastos por el viento (caída de ceniza)
- Proyección balística (bloques y bombas)
- Corrientes de densidad piroclástica (CDP), diluidas y concentradas
- Flujos de lava
- Lahares
- Emisión de gases

### Panel de telemetría

Altura de la columna, VEI, temperatura del magma, alcance de las CDP, sismicidad/tremor en tiempo real, productos activos en superficie y **estado de alerta** según el esquema de cuatro colores del Servicio Geológico Colombiano.

### Glosario integrado

La pestaña **Conceptos** reúne definiciones breves organizadas en ocho bloques: terminología general, características del magma, procesos o fenómenos, depósitos, estilos eruptivos, erupción, monitoreo y estados de alerta, y notas sobre la simulación.

---

## Base científica

El comportamiento del simulador sigue principios establecidos de la vulcanología:

- La escala de intensidad corresponde al **Índice de Explosividad Volcánica (VEI)**.
- La distribución espacial de los peligros (balísticos proximales, CDP a distancias intermedias, lahares y ceniza a mayor distancia) reproduce el patrón documentado en el registro global de víctimas volcánicas.
- Los **estados de alerta** siguen el esquema vigente del Servicio Geológico Colombiano (cuatro colores, sin numeración, desde 2023).

### Referencias

- Newhall, C. G., & Self, S. (1982). The Volcanic Explosivity Index (VEI): An estimate of explosive magnitude for historical volcanism. *Journal of Geophysical Research, 87*(C2), 1231–1238. <https://doi.org/10.1029/JC087iC02p01231>
- Brown, S. K., Jenkins, S. F., Sparks, R. S. J., Odbert, H., & Auker, M. R. (2017). Volcanic fatalities database: analysis of volcanic threat with distance and victim classification. *Journal of Applied Volcanology, 6*, 15. <https://doi.org/10.1186/s13617-017-0067-4>
- Auker, M. R., Sparks, R. S. J., Siebert, L., Crosweller, H. S., & Ewert, J. (2013). A statistical analysis of the global historical volcanic fatalities record. *Journal of Applied Volcanology, 2*, 2. <https://doi.org/10.1186/2191-5040-2-2>
- Servicio Geológico Colombiano. *Estados de alerta por actividad volcánica en Colombia.* <https://www2.sgc.gov.co/Paginas/estados-de-alerta-volcanes.aspx>

---

## Alcance y limitaciones

> [!IMPORTANT]
> Este simulador es un **recurso educativo de visualización conceptual**, con fines exclusivamente académicos y de divulgación.
>
> - Las vistas y magnitudes son representaciones **esquemáticas**; no reproducen valores cuantitativos validados.
> - **No constituye pronóstico ni evaluación oficial de amenaza volcánica.**
> - La separación direccional de algunos flujos (por ejemplo, CDP y lahares en sectores distintos de la vista en planta) es una elección de visualización para facilitar la lectura, no un comportamiento natural de estos fenómenos.
> - Para información oficial sobre volcanes en Colombia, consulte al [Servicio Geológico Colombiano](https://www2.sgc.gov.co/).

---

## Uso local

No requiere instalación, compilación ni servidor: es un único archivo HTML autocontenido.

```bash
git clone https://github.com/jorgealpala/observatorio-vulcanologico-virtual.git
cd observatorio-vulcanologico-virtual
```

Luego abre `index.html` en cualquier navegador moderno (Chrome, Firefox, Edge o Safari).

> **Nota sobre conectividad:** las vistas de perfil, planta y conceptos funcionan completamente sin conexión. La vista 3D carga Three.js desde CDN; si no hay acceso a internet, esa pestaña muestra un aviso y el resto de la aplicación sigue operando con normalidad.

### Despliegue en GitHub Pages

1. El archivo principal debe llamarse **`index.html`** en la raíz del repositorio.
2. En el repositorio: *Settings → Pages → Source: Deploy from a branch*, seleccionando la rama `main` y la carpeta `/ (root)`.
3. El sitio queda publicado en `https://<usuario>.github.io/<repositorio>/`.

---

## Estructura del repositorio

```
observatorio-vulcanologico-virtual/
├── index.html      # Aplicación completa (HTML + CSS + JavaScript)
├── README.md
├── LICENSE         # Licencia MIT
└── docs/
    └── captura.png # (opcional) captura para el README
```

---

## Tecnologías

- **HTML5, CSS3 y JavaScript (ES6+)** sin frameworks ni proceso de compilación.
- **Canvas 2D** para las vistas de perfil y planta, con motor de partículas propio.
- **Three.js r128** (vía CDN) para la vista tridimensional, con degradación elegante si no está disponible.
- Tipografías: Space Grotesk, JetBrains Mono e Inter.

---

## Cómo citar

Alpala Aguilar, J. A. (2026). *Observatorio Vulcanológico Virtual — Simulador de erupciones volcánicas* [Software]. <https://jorgealpala.github.io/observatorio-vulcanologico-virtual/>

<details>
<summary>BibTeX</summary>

```bibtex
@software{alpala2026observatorio,
  author  = {Alpala Aguilar, Jorge Armando},
  title   = {Observatorio Vulcanológico Virtual — Simulador de erupciones volcánicas},
  year    = {2026},
  url     = {https://jorgealpala.github.io/observatorio-vulcanologico-virtual/},
  note    = {Recurso educativo de visualización conceptual}
}
```

</details>

---

## Contacto

**Jorge Armando Alpala Aguilar**
📧 [jorge.alpala.1987@gmail.com](mailto:jorge.alpala.1987@gmail.com)

¿Sugerencias, correcciones técnicas o ideas para nuevas funcionalidades? Puedes abrir un [issue](https://github.com/jorgealpala/observatorio-vulcanologico-virtual/issues) o escribir directamente.

---

## Licencia

Distribuido bajo la **Licencia MIT**. Consulta el archivo [`LICENSE`](LICENSE) para el texto completo.

En términos prácticos, puedes usar, copiar, modificar y redistribuir el software —incluso con fines comerciales— siempre que conserves el aviso de copyright y la nota de licencia. El software se entrega «tal cual», sin garantías de ningún tipo, lo que es coherente con su carácter de recurso educativo descrito en [Alcance y limitaciones](#alcance-y-limitaciones).

© 2026 Jorge Armando Alpala Aguilar
