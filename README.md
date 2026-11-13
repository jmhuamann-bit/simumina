# SimuMina CAEX · demo web

**Abrir la demo:** https://jmhuamann-bit.github.io/simumina/

Demo del simulador SimuMina para operadores mineros: 27 simulaciones de emergencia en 6 módulos, para el camión minero (CAEX), el cargador frontal y la perforadora, con tutor de IA y reportes de Seguridad y Salud Ocupacional (SSO).

## Simulaciones

**Módulo 1: Fallas de frenos (CAEX)**

- Falla del freno de servicio al bajar la rampa cargado
- Falla del retardador en un descenso largo
- Sobrecalentamiento de frenos (el frenado se pierde poco a poco)
- Pérdida de presión del sistema de frenos
- Falla de frenos en curva
- Falla del freno de estacionamiento en la zona de carga

**Módulo 2: Eventos naturales (CAEX)**

- Tormenta eléctrica durante el acarreo
- Sismo durante la operación
- Caída de rocas o deslizamiento del talud sobre la vía
- Huaico o vía inundada
- Neblina densa repentina

**Módulo 3: Riesgos de tránsito (CAEX)**

- Camioneta en el punto ciego del CAEX
- Equipo detenido en la vía
- Peatón en la vía
- Borde de la berma en la zona de descarga
- Fatiga o microsueño en el turno de noche

**Módulo 4: Motor, llantas y dirección (CAEX)**

- Incendio en el motor
- Reventón de llanta
- Falla de la dirección
- Apagado del motor en plena rampa

**Módulo 5: Cargador frontal**

- Falla de frenos del cargador en pendiente
- Persona en el punto ciego al retroceder
- Traslado con el balde levantado
- Incendio en el cargador

**Módulo 6: Perforadora**

- Tormenta eléctrica con el mástil levantado
- Grietas en la cresta del banco durante el traslado
- Incendio en la perforadora

## Uso

- Se maneja con el teclado: en la portada, **Probar con teclado** en cualquier simulación. `W` acelera, `S` frena, `A` `D` giran, `Espacio` retardador, `B` freno de emergencia, `X` luces de emergencia, `P` freno de parqueo, `H` bocina, `R` (mantener) radio, `1` `2` `3` marcha D · N · R. `F1` muestra todas las teclas de cada simulación.
- Cargador frontal: `U` sube y `J` baja el balde (mantener).
- Perforadora: `K` inicia o detiene la perforación; `U` sube y `J` baja el mástil (mantener).
- En el entrenamiento guiado, el panel del procedimiento muestra al lado de cada paso la tecla que lo cumple. En la evaluación no aparece, porque es una sesión sin ayudas.
- Los registros y reportes que trae son de demostración (operadores ficticios). Lo que haga cada visitante queda solo en su navegador.
- En la estación de la mina, la misma plataforma conecta el visor de realidad virtual, el volante con pedales y el traje háptico.
- El tutor de IA en la nube (informe y chat con Claude) funciona cuando la página se abre dentro de Claude. En otras vistas trabaja el tutor local, sin conexión.
- `C` recorre las cámaras: cabina, exterior, retroceso, cine (cortes automáticos entre planos), dron y planta. En la cabina, el ratón permite mirar los espejos retrovisores.

## Visor 3D (realidad virtual)

**Acceso directo:** https://jmhuamann-bit.github.io/simumina/#/visor abre la falla de frenos lista para el visor (también desde la portada, con **Falla de frenos con visor 3D**). Con `#/visor/<simulación>` se abre otra, por ejemplo `#/visor/cargador-frenos`.

Cada simulación tiene el botón **Conectar visor 3D** en la barra superior y en la pantalla de inicio. Cuando el navegador detecta un visor, el botón pasa a **Entrar al visor 3D**, queda como botón principal y abre la simulación en el visor.

- **Visor conectado a la PC** (Meta Quest con Link o Air Link, o un visor de SteamVR): encienda el visor, deje abierta su aplicación en la PC y abra la demo en Chrome o Edge.
- **Meta Quest sin PC**: abra la demo en el navegador del visor.
- Dentro del visor, el gatillo derecho comienza la sesión y suelta el freno de parqueo, como `W` en el teclado (también comienza con `A`; el instructor puede pulsar **Comenzar**). Durante la sesión: gatillo derecho acelera, gatillo izquierdo frena, agarre derecho aplica el retardador, `A` el freno de emergencia, `B` (mantener) la radio, el stick izquierdo gira (en controles HTC Vive, el panel táctil), `X` el freno de parqueo e `Y` las luces de emergencia.
- Al terminar, el resultado (aprobado o no, puntaje, primera acción, pasos en orden) aparece frente al operador dentro del visor. Con `A` sale del visor y en la pantalla queda el informe del tutor.
- Si el visor no aparece, el botón explica cómo conectarlo y vuelve a buscarlo.

## Gráficos

Un motor visual común aplica a las 27 simulaciones: posproceso HDR con gradación de color por simulación, luz ambiente que rebota del suelo, luz dinámica del fuego y de los rayos, polvo y partículas en el aire, huellas de neumáticos y orugas, suspensión con resortes, frenos que se ponen al rojo y humean, espejos retrovisores funcionales y escenografía propia del cargador (frente de carguío) y de la perforadora (malla de perforación y cresta del banco). El terreno, la cordillera y las rocas se dibujan por sectores y los camiones lejanos usan una versión simplificada. La calidad (Baja, Media, Alta) se elige en la configuración; dentro del visor de RV el detalle se ajusta solo.

Los procedimientos, tiempos y parámetros de las simulaciones son referenciales y deben validarse con los estándares de cada mina. three.js (licencia MIT) se carga desde jsDelivr.

Esta página se generó originalmente con `npm run demo-web` desde el proyecto SimuMina. Las simulaciones, las máquinas y los gráficos nuevos se agregaron directamente en `index.html`: regenerar la página desde ese proyecto los sobrescribiría.
