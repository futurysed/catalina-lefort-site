---
name: catalina-funnel
description: Diseña funnels de reservas en Perspective.co para Dra. Catalina Lefort. Actívate cuando se pide un funnel, embudo, flujo de reservas, o proceso de captación de leads.
---

# Diseñador de Funnel — Dra. Catalina Lefort

## Contexto de la Oferta
- **Producto:** Sesión 1:1 — Evaluación Integral de Salud (60 min)
- **Precio:** $59.91 USD / ~55.000 CLP
- **Objetivo del funnel:** Captar leads calificados → reserva directa en calendario
- **Plataforma de funnel:** Perspective.co (mobile-first)
- **Audiencia que llega:** Mujeres chilenas 25–50 desde anuncios de Meta

## Estructura Estándar (7 páginas)

### Página 1 — Hook (portada)
- **Objetivo:** Captar atención, dar contexto, invitar a continuar
- **Headline:** Adaptar al ángulo del anuncio que trajo a la persona
  - TOFU fatiga: "¿Cansada sin razón? Puede que tus exámenes tengan la respuesta."
  - MOFU proteína: "¿Cómo obtener proteína suficiente en una dieta plant-based? La respuesta médica."
  - BOFU reserva: "Reserva tu evaluación integral de salud con Dra. Catalina Lefort"
- **Subhéader:** "Evaluación de 60 min · Online · Con una médica que realmente explica tus exámenes"
- **Tiempo estimado:** "3 preguntas · 2 minutos"
- **CTA:** "Comenzar →"

### Página 2 — Pregunta Calificadora 1 (situación actual)
- **Tipo:** Selección única (iconos + texto)
- **Pregunta:** "¿Cuál de estas describe mejor cómo te sientes ahora?"
- **Opciones:**
  - Siempre cansada, aunque duermo bien
  - Tengo exámenes recientes que no entiendo
  - Quiero cambiar mi alimentación pero no sé cómo
  - Tengo miedo de tener deficiencias con plantas
- **Mapeo CRM:** situation_current
- **Lógica:** Todas califican → continuar a Página 3

### Página 3 — Pregunta Calificadora 2 (urgencia)
- **Tipo:** Selección única
- **Pregunta:** "¿Cuánto tiempo llevas con este problema?"
- **Opciones:** Menos de 3 meses / 3–12 meses / Más de 1 año / Desde siempre
- **Mapeo CRM:** time_with_problem
- **Lógica:** Todas califican → continuar. (Dato de segmentación, no de descalificación.)

### Página 4 — Pregunta Calificadora 3 (objetivo)
- **Tipo:** Selección única
- **Pregunta:** "¿Qué es lo más importante para ti ahora mismo?"
- **Opciones:**
  - Tener más energía durante el día
  - Entender mis exámenes de sangre por fin
  - Hacer la transición plant-based sin sufrir deficiencias
  - Mejorar mi salud a largo plazo, sin depender de medicamentos
- **Mapeo CRM:** primary_goal
- **Lógica:** Todas califican → continuar a captura de contacto

### Página 5 — Captura de Contacto
- **Headline:** "Casi listo — ¿dónde te enviamos los detalles de tu sesión?"
- **Campos:** Nombre (texto) / Email (obligatorio) / Teléfono WhatsApp (opcional)
- **Consentimiento:** "Acepto recibir información sobre la sesión de Dra. Catalina Lefort" (checkbox obligatorio)
- **Microcopy:** "No spam. Solo lo que necesitas para tu sesión."
- **Mapeo CRM:** first_name, email, phone, consent_date

### Página 6 — Reserva de Sesión
- **Headline:** "Elige tu horario"
- **Subhéader:** "Cupos limitados — sesiones disponibles esta semana"
- **Contenido:** Calendario embebido (Calendly / Cal.com)
- **Microcopy debajo:** "60 min · Online · $59.91 USD"
- **Evento Pixel:** CompleteRegistration al completar reserva

### Página 7 — Gracias
- **Headline:** "¡Tu sesión está reservada!"
- **Subhéader:** "Revisa tu email — tienes todos los detalles allí"
- **Copy:** "Recibirás un email con el link de videollamada y un breve formulario previo para aprovechar al máximo tu sesión."
- **WhatsApp CTA:** "¿Tienes preguntas? Escríbeme por WhatsApp"
- **Próximos pasos:** Revisa tu email · Completa el formulario previo · Prepara tus exámenes recientes si los tienes

### Página Descalificación
- **Headline:** "Gracias por tu honestidad"
- **Copy:** "Parece que tu situación puede necesitar atención más inmediata. Te recomiendo contactar a tu médico de confianza primero."
- **CTA suave:** "Mientras tanto, te invito a seguirme en Instagram → @dra.catalinalefort"

## Tracking y Configuración Técnica
- **Meta Pixel:** PageView página 1, Lead al completar captura, CompleteRegistration al reservar
- **UTM capture:** utm_source, utm_medium, utm_campaign, utm_content en URL de entrada
- **WhatsApp T+0:** "Hola {first_name}, confirmo tu sesión con Dra. Catalina. Te llegó el email con los detalles. ¿Tienes alguna pregunta?"

## Entregable
Producir la especificación completa página por página lista para construir en Perspective.co, con todo el copy, preguntas, opciones, lógica de ramificación y mapeo CRM.

## Ejemplos de Activación
- "Necesito un funnel para conseguir reservas" → spec completa del funnel estándar
- "Crea un funnel para el ángulo de proteína" → spec con hook adaptado a ángulo proteína
- "Funnel para anuncios de fatiga" → spec con hook TOFU fatiga
