# Equipo 4 — Elixir
## Exposición: Introducción a lenguajes funcionales · Unidad 1

## Integrantes y roles

| Rol | Estudiante | Responsabilidad |
|:-:|:--|:--|
| 1 | ESPAÑA PEREZ, MIGUEL ANGEL | Contexto e historia |
| 2 | ESTRADA RODRIGUEZ, MELANI | Modelo de cómputo y sintaxis |
| 3 | FUENTES MONTAÑO, AXEL | Sistema de tipos / runtime |
| 4 | GARCIA CARO, CARLOS ALEJANDRO | Demo en vivo + caso real |

## Datos del lenguaje

- **Año / origen:** primer commit el 9 de enero de 2011, Brasil; primeras versiones públicas en 2012; versión 1.0 publicada el 18 de septiembre de 2014.
- **Creador(es):** José Valim, quien inició Elixir como un proyecto de investigación y desarrollo dentro de Plataformatec.
- **Modelo de evaluación:** estricto; `Stream` para evaluación diferida
- **Sistema de tipos:** dinámico; se ejecuta sobre la máquina virtual BEAM
- **REPL / herramienta:** `iex` como consola interactiva y `mix` para crear, compilar y administrar proyectos
- **Caso real verificado (obligatorio en pantalla):** Discord — infraestructura de presencia migrada de Go a Elixir (2017). _(fuente IEEE abajo)_

## Guion (12–15 min)

1. **Contexto (2 min)** — Elixir como capa ergonómica sobre Erlang/BEAM.
2. **Modelo de cómputo (3 min)** — inmutabilidad, operador `|>`, `Enum` vs `Stream`, *pattern matching*.
3. **Tipos / runtime (3 min)** — procesos, GenServer, supervisión; qué se descubre en runtime.
4. **Demo en vivo (4 min)** — `iex` + "Hola Paradigma" (1..10) + 2.º ejemplo idiomático (pipeline con `|>`).
5. **Caso real + cierre (2 min)** — Discord con referencia IEEE; conexión con Erlang y Gleam.

## Comandos exactos del demo

```bash
# Instalación
brew install elixir      # macOS
sudo apt install elixir  # Linux

# Hola Paradigma (imprimir 1..10)
iex
iex> Enum.each(1..10, &IO.puts/1)

# Segundo ejemplo idiomático
iex> 1..10 |> Enum.filter(&(rem(&1, 2) == 0)) |> Enum.map(&(&1 * &1))
```

Salida esperada:

```
1
2
3
4
5
6
7
8
9
10
[4, 16, 36, 64, 100]
```

## Grabación de respaldo (asciinema cloud)

- URL: _(pegar la URL de asciinema.org tras `asciinema upload`)_
- Cómo: `asciinema rec demo.cast` → `asciinema upload demo.cast`

## Diapositivas

- `slides.pdf` — 5–8 diapositivas, subir a esta carpeta **antes** de la sesión.

## Bibliografía (IEEE)

1. Elixir Team, “Development,” Elixir Programming Language. [En línea]. Disponible en: https://elixir-lang.org/development/. [Consultado: 17-sep-2026].
2. J. Valim, “Elixir Design Goals,” Elixir Programming Language, 8-ago-2013. [En línea]. Disponible en: https://elixir-lang.org/blog/2013/08/08/elixir-design-goals/. [Consultado: 17-sep-2026].
3. J. Valim, “Elixir v1.0.0 released,” Elixir Programming Language, 18-sep-2014. [En línea]. Disponible en: https://elixir-lang.org/blog/2014/09/18/elixir-v1-0-0-released/. [Consultado: 17-sep-2026].
4. J. Valim, “Elixir v0.5.0 released,” Elixir Programming Language, 25-may-2012. [En línea]. Disponible en: https://elixir-lang.org/blog/2012/05/25/elixir-v0-5-0-released/. [Consultado: 17-sep-2026].

---

Rúbrica, medio de presentación y reglas: [`../TEMAS-INTRO-LENGUAJES-FUNCIONALES-40.md`](../TEMAS-INTRO-LENGUAJES-FUNCIONALES-40.md)
