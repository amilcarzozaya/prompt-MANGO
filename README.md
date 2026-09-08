# Prompt MANGO — Skill para Claude

**Prompt MANGO** convierte una intención del usuario en un prompt completo usando:

- **M** — Meta clara
- **A** — Audiencia específica
- **N** — Nivel de detalle
- **G** — Guía contextual
- **O** — Opciones y formato

La skill detecta qué datos ya dio el usuario, pregunta únicamente por los faltantes y entrega un prompt final listo para usar en Claude o copiar en otro LLM o generador.

## Capacidades

- Prompts para texto, análisis, investigación y código.
- Prompts para imágenes.
- Prompts para video.
- Prompts para música y audio.
- Conversión de ideas vagas en instrucciones estructuradas.
- Mejora de prompts existentes.
- Formato portable entre modelos.
- Adaptación a un modelo específico cuando el usuario lo indica.

## Estructura del repositorio

```text
prompt-mango-claude/
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── .claude/
│   └── skills/
│       └── prompt-mango/
│           └── SKILL.md
├── skills/
│   └── prompt-mango/
│       ├── SKILL.md
│       └── references/
│           └── multimodal.md
├── LICENSE
└── README.md
```

La carpeta `skills/prompt-mango/` sirve al plugin. La copia en `.claude/skills/prompt-mango/` facilita el uso directo cuando el repositorio se monta como proyecto.

## Instalación desde GitHub en Claude Code

Después de publicar esta carpeta como repositorio público en GitHub:

```text
/plugin marketplace add TU-USUARIO/prompt-mango-claude
```

Después:

```text
/plugin install prompt-mango@prompt-mango-marketplace
```

Reemplaza `TU-USUARIO` por tu usuario u organización de GitHub.

> Nota: la sintaxis exacta disponible puede variar por versión de Claude Code. El repositorio incluye `marketplace.json` y `plugin.json` para ajustarse al formato actual de plugins/marketplaces.

## Uso

Puedes invocarla directamente:

```text
/prompt-mango Quiero crear una campaña para lanzar mi nuevo curso de IA.
```

O simplemente pedir:

```text
Ayúdame a convertir esta idea en un Prompt MANGO.
```

### Ejemplo de interacción

Usuario:

```text
Quiero una imagen para LinkedIn de un mango futurista.
```

Prompt MANGO detectará la Meta y parte de la Guía/Formato, y preguntará únicamente por los componentes que realmente falten, por ejemplo audiencia, nivel visual o especificaciones finales.

## Publicación en GitHub

1. Crea un repositorio, por ejemplo `prompt-mango-claude`.
2. Sube todo el contenido de esta carpeta a la raíz del repositorio.
3. Reemplaza `TU-USUARIO` en `.claude-plugin/plugin.json` por el usuario u organización real.
4. Publica el repositorio.
5. Instálalo desde Claude Code usando el marketplace del repositorio.

## Versión

1.0.0

## Autor

Método MANGO — Amílcar Zozaya

## Propiedad intelectual

El Método MANGO y su denominación pertenecen a su autor. Revisa `LICENSE` antes de redistribuir o modificar esta skill.
