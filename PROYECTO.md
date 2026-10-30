# Proyecto Web - Nutricionista

## PROYECTO
Web profesional para nutricionista con dos partes:
- Web pública — presentación, servicios, cursos
- Panel de administración — gestión de pacientes y dietas

---

## STACK
- React, Node.js + Express, SQLite, JWT

---

## LÓGICA DE DIETAS
1. Se ingresan datos del paciente
2. Harris-Benedict calcula las calorías diarias
3. Se desglozan en proteína, carbo y grasa según objetivo
4. Se distribuyen en las comidas del día
5. Se asignan alimentos rotando para generar 15 días variados
6. La nutricionista revisa y ajusta
7. Vista previa → PDF → envío al paciente

---

## REGISTRO DEL PACIENTE
- Nombre completo
- Sexo
- Fecha de nacimiento
- Peso (kg)
- Estatura (cm)
- Nivel de actividad física
- Objetivo
- Número de comidas al día
- Documento de identidad
- Teléfono
- Correo electrónico
- Ciudad
- Restricciones alimentarias
- Alimentos que no consume

---

## BASE DE DATOS DE ALIMENTOS
- Alimentos cotidianos y fáciles de conseguir
- Clasificados por: calorías, macros, rico en, apropiado para qué comida, grupo de rotación, etiquetas
- Nosotros los precargamos, ella puede agregar más desde el panel

---

## PANEL ADMIN
- Login nutricionista (protegido con JWT)
- Registro de pacientes
- Generación automática de 15 días de dieta
- Editor por día/comida (cambiar, quitar, ajustar cantidades)
- Contador de macros en tiempo real
- Vista previa antes de generar PDF
- Gestión de alimentos

---

## DIETA
- Tiene fecha de inicio
- Se puede ajustar en cualquier momento
- Queda guardada con fecha de última modificación
- Historial de dietas por paciente

---

## PDF DE LA DIETA (ejemplo de cómo se vería)

```
DIETA DE: Carlos Pérez
Período: 01/11/2026 - 15/11/2026
─────────────────────────────────
DÍA 1 - Lunes

  Desayuno
  • Avena .............. 150g
  • Huevos ............. 3 unidades
  • Banano ............. 120g

  Media mañana
  • Yogur griego ....... 200g
  • Manzana ............ 1 unidad

  Almuerzo
  • Pechuga pollo ...... 200g
  • Arroz blanco ....... 200g
  • Aguacate ........... 100g

  Merienda
  • Atún ............... 100g
  • Pan integral ....... 80g

  Cena
  • Salmón ............. 150g
  • Brócoli ............ 150g
─────────────────────────────────
DÍA 2 - Martes
  ...
```
- Se envía al paciente por WhatsApp y correo electrónico
