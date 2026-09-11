# EGD TutorBoard

**Status:** In development — advanced working prototype

EGD TutorBoard is a specialised digital drawing-board application for Engineering Graphics and Design (EGD) tutors and learners.

It was created because generic whiteboards and geometry tools did not provide the combination of accurate page sizes, millimetre-based measurements, realistic drawing instruments and multi-page workflow needed for practical EGD tutoring.

## The problem

Online EGD tutoring is difficult when the software behaves like a normal whiteboard instead of a technical drawing board. Tutors and learners need tools that support proper drawing technique, accurate measurements and realistic interaction with EGD instruments.

## The solution

EGD TutorBoard is being built to provide a purpose-built EGD workspace with real page sizes, editable drawing objects and digital versions of traditional drawing instruments.

The app is designed to support both teaching and practical drawing while still requiring the learner to use correct EGD technique.

## Current working features

- Multi-page drawing workspace
- A3/A4-style page workflow and page setup locking
- Per-page tool and drawing state
- Editable textboxes with movement and resizing
- Draw tool with EGD line types and line properties
- Millimetre-based editable drawing objects
- Full board ruler with top and bottom working edges
- Board ruler movement, locking, opacity and position control
- Drawing snap behaviour against the board ruler
- 30°/60° triangle with movement, rotation, flipping, locking and stencil behaviour
- 45° triangle with movement, rotation, flipping, locking and stencil behaviour
- Drawing along triangle edges
- 360° protractor with movement, rotation, locking and visual angle reading
- Physical-style compass with movement, locking and adjustable opening
- Compass arc drawing stored as editable millimetre-based objects
- Dimension Line tool with measurement, selection and snapping
- Whole Object Eraser
- Fine Eraser for drawn lines and compass arcs
- Global Ctrl+Z undo framework for supported actions
- Collapsible left toolbar and right Properties panel
- Automatic workspace enlargement when side panels are collapsed

## A deliberate design decision

EGD TutorBoard is not intended to become an automatic geometry calculator.

Rulers and triangles are used as physical-style drawing guides and do not expose typed angle controls. The protractor remains the tool used to determine or check angles.

This keeps the software useful for learning while preserving the drawing technique the learner is expected to practise.

## Technical highlight

Drawing data is stored as editable objects rather than flattened images.

For example, the Fine Eraser does not simply paint white over a line or compass arc. It edits the underlying geometry and leaves the remaining pieces as editable drawing objects.

This approach supports future measurement, editing, selection, undo and export features.

## Technology

- React
- Vite
- TypeScript
- CSS
- SVG-based drawing and instrument rendering

## Current development stage

The core drawing-instrument system is already functional, but the project is still under active development.

### Planned / not yet complete

- Symbol Tool foundation
- Civil, architectural and electrical symbol libraries
- North arrow and projection symbols
- Lasso Delete
- PDF import and scale-to-page workflow
- Project save/open workflow
- PDF/image export
- Tutorial and revision content
- Final Microsoft Store packaging and release

## Screenshots

Screenshots of the current working prototype will be added soon.

Planned screenshots will show:

- Main workspace with multiple EGD instruments
- Board ruler and triangle stencil behaviour
- 360° protractor
- Compass with a drawn arc
- Dimension Line tool and snapping
- Multi-page drawing layout
- Expanded workspace with the side panels collapsed

## Project goal

The goal is to build a practical EGD-focused drawing environment that feels closer to using a real drawing board than a generic digital whiteboard, while making online tutoring and digital demonstrations easier.

---

**Project status:** Active development
