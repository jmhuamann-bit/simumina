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
- Los registros y reportes que trae son de demostración (operadores ficticios). Lo que haga cada visitante queda solo en su navegador.
- En la estación de la mina, la misma plataforma conecta el visor de realidad virtual, el volante con pedales y el traje háptico.
- El tutor de IA en la nube (informe y chat con Claude) funciona cuando la página se abre dentro de Claude. En otras vistas trabaja el tutor local, sin conexión.

Los procedimientos, tiempos y parámetros de las simulaciones son referenciales y deben validarse con los estándares de cada mina. three.js (licencia MIT) se carga desde jsDelivr.

Esta página se generó originalmente con `npm run demo-web` desde el proyecto SimuMina. Las simulaciones, las máquinas y los gráficos nuevos se agregaron directamente en `index.html`: regenerar la página desde ese proyecto los sobrescribiría.
