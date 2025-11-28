Sistema de Gestión para Laboratorio de Análisis Clínicos
-------------------------------------------------------------------------------
Trabajo Final – Programación II
Universidad Tecnológica Nacional – Facultad Regional General Pacheco (UTN-FRGP)
-------------------------------------------------------------------------------
--Descripción del proyecto

Este proyecto consiste en un sistema de gestión integral para un Laboratorio de Análisis Clínicos.
Permite administrar toda la información relacionada con:

  -Pacientes

  -Bioquímicos

  -Estudios / Análisis

  -Salas

  -Turnos

  -Facturación

  -Obras sociales

  -Resultados de estudios

  -Reportes estadísticos

El sistema fue desarrollado como Trabajo Final de la materia Programación II, siguiendo prácticas de programación orientada a objetos y manejo de archivos binarios.

--Arquitectura y diseño

El sistema se organiza con una estructura clara y escalable:

-Entidades

Cada módulo principal se modela con una clase (Paciente, Bioquímico, Turno, Factura, etc.) que contiene únicamente datos y métodos simples.

-Managers

Los Manager son plantillas (templates) orientadas a:

  -Gestionar archivos binarios .dat

  -Implementar ABML:

    -Alta

    -Baja (lógica mediante atributo _estado)

    -Modificación

    -Lectura

  -Realizar búsquedas y obtener IDs autoincrementales

  -Listar registros activos

Cada entidad tiene su propio manager derivado de Manager<T>.

-Servicios

Los Servicios encapsulan la lógica de negocio, incluyendo:

  -Validaciones

  -Interacción con el usuario

  -Coordinación entre múltiples entidades

  -Reglas adicionales (evitar turnos superpuestos, validar DNI único, etc.)

  -Esto hace que el sistema sea modular y fácil de mantener.


--Tecnologías utilizadas--

  -C++ 17

  -POO (Programación Orientada a Objetos)

  -Manejo de archivos binarios (.dat)

  -Code::Blocks + MinGW 14.2.0

--Cómo compilar y ejecutar--

1-Abrir el proyecto en CodeBlocks.

2-Asegurarse de que MinGW 14.2 esté configurado.

3-Compilar (Build).

4-Ejecutar desde el IDE.
