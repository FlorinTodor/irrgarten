# Irrgarten: the same game in Java and in Ruby

**English** · [Español](#irrgarten-el-mismo-juego-en-java-y-en-ruby)

A turn-based labyrinth game built twice from the same class diagram, once in Java and once
in Ruby, to compare how each language solves the same object-oriented design.

[![Demo: a real game of the Ruby version in the terminal](https://florintodor.dev/media/poster/irrgarten.jpg)](https://florintodor.dev/en/proyectos/irrgarten/)

**Demo video and project page:** [florintodor.dev/en/proyectos/irrgarten](https://florintodor.dev/en/proyectos/irrgarten/)

## Design

- **Domain model:** `Game`, `Labyrinth`, `Player`, `Monster`, `Weapon`, `Shield`,
  `GameState` and `Dice`, which concentrates every random decision.
- **Inheritance:** `Player` and `Monster` extend the abstract `LabyrinthCharacter`;
  `Weapon` and `Shield` extend the abstract `CombatElement`.
- **Polymorphism:** a player who dies may resurrect as a `FuzzyPlayer`, a `Player`
  subclass that overrides `move`, `attack` and `defensiveEnergy` to add randomness to its
  decisions.
- **Generics:** `CardDeck<T>`, with `WeaponCardDeck` and `ShieldCardDeck` as subclasses,
  hands out rewards.
- **MVC:** a `Controller` between the game and a `UI` interface with two implementations
  in Java, `TextUI` (terminal) and `GameUI` (Swing); Ruby has the text interface.

## Where the code is

| | |
|---|---|
| Java | `PDOO_PRACTICAS/Irrgarten_trabajo/java_original.zip` (NetBeans project, `irrgarten.Main.Main`) |
| Ruby | `PDOO_PRACTICAS/Irrgarten_trabajo/ruby_original.zip` (`ruby Main/main.rb`) |

The rest of the repository is course material: theory, notes and exam exercises.

Coursework for Object-Oriented Programming and Design (PDOO), University of Granada,
2023-24.

---

# Irrgarten: el mismo juego en Java y en Ruby

[English](#irrgarten-the-same-game-in-java-and-in-ruby) · **Español**

Videojuego de laberinto por turnos implementado dos veces a partir del mismo diagrama de
clases, una en Java y otra en Ruby, para comparar cómo resuelve cada lenguaje el mismo
diseño orientado a objetos.

**Vídeo de la demo y ficha del proyecto:** [florintodor.dev/proyectos/irrgarten](https://florintodor.dev/proyectos/irrgarten/)

## Diseño

- **Modelo de dominio:** `Game`, `Labyrinth`, `Player`, `Monster`, `Weapon`, `Shield`,
  `GameState` y `Dice`, que concentra todas las decisiones aleatorias.
- **Herencia:** `Player` y `Monster` heredan de la clase abstracta `LabyrinthCharacter`;
  `Weapon` y `Shield`, de la clase abstracta `CombatElement`.
- **Polimorfismo:** un jugador que muere puede resucitar como `FuzzyPlayer`, una subclase
  de `Player` que redefine `move`, `attack` y `defensiveEnergy` para meter aleatoriedad en
  sus decisiones.
- **Genéricos:** `CardDeck<T>`, con `WeaponCardDeck` y `ShieldCardDeck` como subclases,
  reparte las recompensas.
- **MVC:** un `Controller` entre el juego y una interfaz `UI` con dos implementaciones en
  Java, `TextUI` (terminal) y `GameUI` (Swing); en Ruby, la de texto.

## Dónde está el código

| | |
|---|---|
| Java | `PDOO_PRACTICAS/Irrgarten_trabajo/java_original.zip` (proyecto de NetBeans, `irrgarten.Main.Main`) |
| Ruby | `PDOO_PRACTICAS/Irrgarten_trabajo/ruby_original.zip` (`ruby Main/main.rb`) |

El resto del repositorio es material de la asignatura: teoría, apuntes y ejercicios de
examen.

Trabajo de la asignatura Programación y Diseño Orientado a Objetos (PDOO), Universidad de
Granada, 2023-24.
