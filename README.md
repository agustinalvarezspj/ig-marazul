# Tablero IG orgánico — Mar Azul Suites

Seguimiento semanal de campañas de IG orgánico: cortes acumulados por mes, métricas del
período, reservas, facturación, ROAS y el análisis de cada corte. Mismo esquema que
el pickup de ocupación.

## Cómo funciona

- `index.html` — el tablero, con la pantalla de acceso.
- `datos.json` — los datos publicados, **cifrados**. Es lo único que se toca semana a semana.
- `publicar.bat` — sube el `datos.json` nuevo al repo.
- `robots.txt` — mantiene el sitio fuera de los buscadores.
- `README-SEGURIDAD.md` — leelo antes de crear tu contraseña.

El equipo abre la URL y ve siempre lo último publicado. Cuando **vos** cargás un corte,
queda como borrador en tu navegador ("● borrador sin publicar" arriba a la derecha)
hasta que lo publiques. Nadie más lo ve hasta ese momento.

## Puesta en marcha (una sola vez)

1. Cloná o bajá esta carpeta a tu computadora.
2. Abrí `index.html` con doble clic (desde tu compu, no desde la web) → **Primer acceso**:
   creá tu usuario con una frase larga.
3. Botón **Importar** → elegí `semilla-ig.json` (te lo pasa Claude por el chat; **nunca
   lo subas al repo**: tiene los datos sin cifrar). Entran los cortes históricos.
4. **Publicar cambios** → descarga `datos.json` cifrado → doble clic en `publicar.bat`.
5. En GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
   En un par de minutos queda en `https://USUARIO.github.io/ig-marazul/`.
6. Entrá a la URL, botón **Equipo**, y creá un usuario para cada persona.

## Rutina de cada viernes

1. En Meta Business Suite / panel profesional de IG: exportar las métricas en CSV
   (Alcance, Visualizaciones, Interacciones, Clics en el enlace, Visitas, Seguidores,
   el export por publicación y — cuando quieras refrescar la audiencia — el de Público).
   Sirve cualquier rango que incluya los días nuevos: el tablero fusiona por fecha.
2. Abrir la URL del tablero, entrar, `+ Nuevo viernes`.
3. Arrastrar TODOS los CSVs a la zona de carga. El tablero los lee solo
   (series diarias, publicaciones y audiencia; las historias se ignoran).
4. Revisar el rango sugerido (desde el día siguiente al último corte, hasta el último
   día con datos) y la vista previa de métricas calculadas.
5. Pegar el análisis del corte (pedírselo a Claude con los mismos números) y guardar.
6. `Publicar cambios` (con token: directo; sin token: descarga `datos.json` → `publicar.bat`).

## Qué muestra

- **Cortes de los viernes**: las 6 métricas del período calculadas desde los datos
  diarios, con flechas vs. el ritmo diario del corte anterior, top publicaciones del
  período y el análisis.
- **Mes a mes**: alcance + seguidores, mediana por reel + cadencia, y clics — calculado
  en vivo desde los datos cargados, se extiende solo con cada export nuevo.
- **Audiencia**: seguidores, sexo/edad, ciudades y países — se actualiza subiendo el
  export "Público".

## Ojo con esto

- Cargá siempre desde la **misma computadora y el mismo navegador**. El borrador vive ahí.
- Si abrís el tablero en otra máquina con un borrador viejo sin publicar, vas a ver ese
  borrador en vez de lo publicado. `Descartar borrador` lo arregla.
- Los datos van cifrados, así que el repo puede ser público sin drama. Lo que
  no se puede es recuperar una contraseña perdida. Ver `README-SEGURIDAD.md`.
- Exportá el **CSV** de vez en cuando: es tu respaldo en claro, guardalo fuera del repo.
