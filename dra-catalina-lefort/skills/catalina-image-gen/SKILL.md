---
name: catalina-image-gen
description: Genera imágenes de anuncios para Dra. Catalina Lefort usando Kie.ai. Actívate cuando se piden imágenes, visuales, fotos para anuncios o contenido.
---

# Generador de Imágenes — Dra. Catalina Lefort

## Estilo Visual de Marca
- **Tono:** Cálido, profesional-pero-accesible, esperanzador — nunca frío ni hospitalario
- **Paleta:** Verdes suaves, blanco clínico, tonos tierra, luz natural de ventana
- **Sujeto principal:** Mujer latinoamericana 30–45 años, articulada, moderna, saludable
- **Ambientes:** Cocina con plantas, escritorio con luz natural, exterior soleado, consulta médica acogedora
- **Evitar:** Hospital frío, jeringa, emergencia, imágenes de antes/después del cuerpo, propaganda vegana

## Proceso

**Paso 1 — Identificar ángulo y etapa:**
Determinar el tema del anuncio (fatiga, proteína, exámenes, sueño, etc.) y si es TOFU/MOFU/BOFU.

**Paso 2 — Construir el prompt JSON (Nano Banana):**

{
  "angle": "[nombre del ángulo]",
  "funnel_stage": "TOFU / MOFU / BOFU",
  "subject": "[descripción detallada del sujeto]",
  "scene": "[descripción de la escena]",
  "lighting": "[tipo de luz — natural, cálida, de ventana]",
  "style": "photorealistic, warm, professional, approachable",
  "colors": "[paleta específica]",
  "text_overlay": "[texto en imagen si aplica, o 'none']",
  "aspect_ratio": "1:1",
  "negative_prompt": "cold, clinical, aggressive, hospital, syringe, vegan propaganda, before-after body transformation, fast food"
}

**Paso 3 — Ejecutar generación con Kie.ai:**

python _tools/generate_kie.py --prompt '[prompt json aquí]'
(Devuelve un taskId)

**Paso 4 — Recuperar imagen:**

python _tools/get_kie_image.py --task-id [taskId]
(Guarda imagen en images/[angle-name].jpg)

Si los scripts no están disponibles: entregar el prompt JSON completo para uso manual.

## Templates por Ángulo

**TOFU — Fatiga / Energía:**
{
  "subject": "Chilean woman, 35-40 years old, professional, sitting at desk, tired but hopeful expression",
  "scene": "modern bright home office, morning, plants on windowsill, coffee nearby",
  "lighting": "warm natural window light",
  "style": "photorealistic, warm, hopeful undertone",
  "colors": "warm whites, soft greens, earth tones",
  "text_overlay": "none",
  "aspect_ratio": "1:1",
  "negative_prompt": "cold, aggressive, medical emergency, before-after body, vegan propaganda"
}

**MOFU — Proteína / Nutrición:**
{
  "subject": "Latin American woman, 30-45, preparing colorful plant-based meal, thoughtful confident expression",
  "scene": "modern kitchen, legumes, leafy greens, colorful vegetables visible, clean aesthetic",
  "lighting": "bright natural light, inviting kitchen atmosphere",
  "style": "photorealistic, lifestyle photography, warm and inviting",
  "colors": "fresh greens, warm reds, natural wood tones",
  "text_overlay": "none",
  "aspect_ratio": "1:1",
  "negative_prompt": "processed food, cold, clinical, restrictive diet imagery"
}

**BOFU — Consulta / Sesión:**
{
  "subject": "Female doctor, warm professional smile, modern tablet in hand, welcoming posture",
  "scene": "clean modern consultation space, plants, warm lighting, non-intimidating professional environment",
  "lighting": "warm professional interior lighting",
  "style": "photorealistic, trustworthy, approachable professional",
  "colors": "white, soft green accents, warm neutral tones",
  "text_overlay": "none",
  "aspect_ratio": "1:1",
  "negative_prompt": "cold clinical hospital, aggressive, intimidating, white coat only"
}

**TOFU — Sueño:**
{
  "subject": "Latin American woman, 35-40, waking up gently, natural morning light on face, peaceful but slightly tired",
  "scene": "cozy modern bedroom, white linens, plant on bedside table, morning sun through curtains",
  "lighting": "soft golden morning light",
  "style": "photorealistic, peaceful, lifestyle photography",
  "colors": "warm whites, soft golds, natural greens",
  "text_overlay": "none",
  "aspect_ratio": "1:1",
  "negative_prompt": "hospital, cold, clinical, insomnia horror aesthetic"
}

## Ejemplos de Activación
- "Crea una imagen de mujer cansada" → TOFU fatiga template + ejecutar
- "Imagen para el anuncio de proteína" → MOFU nutrición template + ejecutar
- "Foto para la sesión médica" → BOFU consulta template + ejecutar
- "Imagen de una mujer por la mañana" → TOFU sueño template + ejecutar
