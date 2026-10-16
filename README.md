# EstadoChain
### Cada cambio público deja una huella.

Propuesta para la **Ideathon Avalanche** enfocada en la trazabilidad de modificaciones de contratos públicos: qué cambió, por qué, quién lo propuso y quiénes lo aprobaron.

> **Estado actual:** este repositorio contiene la presentación del proyecto. La demo navegable y la integración con Avalanche son etapas pendientes. El prototipo previsto utilizará datos ficticios y registros simulados, sin backend ni blockchain real.

## El problema

Un contrato público puede cambiar de monto, plazo o alcance por razones legítimas. Revisar esas modificaciones exige reunir versiones, justificaciones y aprobaciones que pueden estar dispersas.

EstadoChain propone un historial consultable para comparar cambios e identificar a sus responsables, facilitando el trabajo de ciudadanía y fiscalizadores.

## La propuesta

Cada modificación reúne:

- La versión anterior y los cambios solicitados.
- Una justificación y referencias a documentos de respaldo.
- Dos decisiones de revisión, emitidas por roles distintos.
- El resultado: pendiente, aprobada o rechazada.
- Una huella de la versión aprobada para posteriores comparaciones de integridad.

## Cómo funcionaría

1. **Proponer:** un responsable solicita modificar monto, plazo o alcance y presenta su justificación.
2. **Comparar:** la interfaz muestra los valores anteriores y los propuestos.
3. **Revisar:** un rol técnico y un rol de control aprueban o rechazan. El proponente no puede aprobar su propia solicitud.
4. **Resolver:** una aprobación mantiene la propuesta pendiente; dos aprobaciones generan una nueva versión. Un rechazo conserva la versión vigente y registra el motivo.
5. **Registrar:** se conserva la relación entre versiones, decisiones y huellas.
6. **Auditar:** se compara una copia del documento con la referencia aprobada para detectar diferencias.

## Un ejemplo

**Caso ficticio: Mejoramiento de Plaza Los Aromos**

| Dato | Contrato vigente | Modificación propuesta |
| --- | --- | --- |
| Monto | $120.000.000 CLP | $132.000.000 CLP |
| Plazo | 90 días | 105 días |
| Versión | v1 | v2, solo después de ambas aprobaciones |

La propuesta incorpora drenaje adicional y debe acompañarse de una justificación. Mientras esté pendiente o sea rechazada, el contrato vigente conserva su monto y plazo.

Si una copia posterior muestra otro monto, la comparación con la referencia aprobada puede señalar la diferencia para su investigación.

## Demo prevista

Mockup web navegable, en español, adaptado a celulares, con diseño oscuro y acento rojo.

El recorrido previsto incluye:

- Listado y detalle de contratos ficticios.
- Formulario de modificación y comparación antes/después.
- Selector de roles para demostrar dos aprobaciones independientes.
- Rechazo con motivo obligatorio e historial de decisiones.
- Comprobante claramente identificado como **simulado**.
- Simulación de una alteración y comparación de integridad.
- Reinicio de la demo.

El selector de roles será una herramienta de demostración, no autenticación real. Las aprobaciones simuladas tampoco serán firmas electrónicas.

## El papel de Avalanche

La integración futura propuesta utilizaría Avalanche para registrar huellas de versiones y eventos asociados a sus aprobaciones. Los documentos permanecerían fuera de la cadena, con custodia, permisos y protección de datos adecuados.

Una huella permitiría comprobar si un contenido coincide con la referencia registrada. Para que esa comparación sea útil, también habrá que definir cómo se representa el documento, cómo se identifica a los responsables y cómo se verifica el registro.

**La integración todavía no está implementada.** El prototipo previsto no enviará transacciones, conectará wallets ni utilizará fondos. Todo comprobante deberá indicar “Registro en Avalanche: simulado”.

## Alcance y límites

- Blockchain **no garantiza que un contrato sea verdadero, legal o correcto**.
- Dos aprobadores podrían coludirse; la doble aprobación no elimina ese riesgo.
- Detectar una diferencia no demuestra por sí solo fraude: requiere revisión y contexto.
- Una referencia guardada únicamente en el navegador también puede manipularse.
- El proyecto complementa la fiscalización y los controles legales y administrativos; no los reemplaza.
- No deben publicarse datos personales ni documentos sensibles en una blockchain.

La autenticidad de los respaldos, la identidad de los participantes y la calidad de la revisión requieren controles adicionales.

## Próximas etapas

- [x] Definir el concepto, el flujo y sus límites.
- [ ] Incorporar la demo navegable con datos ficticios.
- [ ] Validar los recorridos de aprobación, rechazo y auditoría.
- [ ] Diseñar identidad, permisos, custodia documental y recuperación.
- [ ] Implementar y probar una integración en una red de pruebas de Avalanche.
- [ ] Evaluar el modelo con usuarios y responsables de fiscalización.

## Cómo explorar este repositorio

Actualmente puedes revisar esta propuesta en el README. Aún no hay código ejecutable ni instrucciones de instalación; se incorporarán junto con la demo.

---

**EstadoChain: cambios explicables, responsables identificables y versiones que se pueden comparar.**

Proyecto conceptual para la Ideathon Avalanche. No implica aval oficial de Avalanche ni de una institución pública.
