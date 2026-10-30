<h1 align="center">JarvisOS</h1>

<h3 align="center">An AI-powered engineering workstation, built by an engineer who doesn't code</h3>

<p align="center"><code>chemical engineering</code> · <code>CAD / CFD / process simulation</code> · <code>local-first AI</code> · <code>data sovereignty</code></p>

---

> **This is a showcase.** JarvisOS itself is private. This page explains what it is, why I'm building it, and what I've
> learned about what AI makes possible for engineers today.

## The question behind it

I'm a chemical engineer, not a software developer. A year ago I asked myself:

> **How far can an engineer with no coding background go, if he treats today's AI models as a development team and
> keeps his engineering judgement in charge?**

JarvisOS is my answer in progress: a full engineering workstation — process simulation, parametric CAD, meshing, CFD,
FEM, project knowledge and an AI assistant that lives inside the work — designed, specified, reviewed and tested by me,
with the code written by AI agents working under rules, tests and review gates that I set.

## Why I started

**1. Independence from expensive licences.** University licences end. COMSOL, ANSYS, Aspen and friends are excellent
and priced for large companies. I wanted to keep doing serious R&D without depending on them — using open engines
(OpenFOAM, Gmsh, CalculiX, DWSIM, build123d/OpenCASCADE) where they are good enough, and leaving the door open to
commercial tools where they are genuinely better.

**2. Data sovereignty.** Unpublished research, designs and IP shouldn't leave the machine just because an AI is useful.
JarvisOS runs local models on my own GPU by default and treats every use of a cloud model as an explicit, logged
decision — with sensitivity checks on what is sent, and subscription-based access instead of pay-per-call APIs.

**3. An experiment in empowerment.** Can AI give an engineer the leverage that used to require a software team? Not
"AI writes an app", but AI as the hands — and the engineer as architect, reviewer and owner of every decision.

## What it does today

- **Design workspace** — a plant flowsheet with a steady-state solver and solver console, component trees, versions
  and case studies, all on one shared project state.
- **Parametric CAD** — geometry generated from typed specifications and sandboxed scripts, exported to STEP/STL/GLB
  and inspected in a 3D viewer.
- **CFD** — OpenFOAM pipe-flow cases (laminar and RANS) from geometry to mesh to results, with run comparison and
  reduced models published back into the process simulation.
- **Model workshop** — every engineering model shows its Python source side-by-side with its equations, rendered like
  a LaTeX paper and linked line by line.
- **Bubu, the assistant that points** — a small mascot that opens a chat bubble anywhere in the app. It reads the
  page, explains how to do things, and *draws arrows* to the buttons you need. You can point at things for it, dictate,
  or share your screen. It never clicks or changes anything on its own.
- **Governed AI** — local models for everyday work, frontier models through subscriptions for hard problems, every
  call routed, budgeted and recorded.

<!-- Screenshots: add 3–4 images here, e.g. Bubu pointing at a control, the Design page, CFD results, the LaTeX workshop. -->

## How it's built

I don't write the code. I write **specifications**: what a feature must do, how it will be tested, what it must never
do. A team of AI agents — different models from different companies, each with a defined role — implements,
reviews and verifies, through:

- 250+ written specifications and a single source of truth for what's done and what's next;
- thousands of automated tests and continuous integration on every change;
- an autonomous supervisor that carries the roadmap forward, switches between AI providers when one runs out of
  quota, and stops to ask me whenever the effect of an action is uncertain.

The interesting part isn't any single tool — it's making good existing tools cooperate inside a traceable engineering
workflow instead of living in separate programs, spreadsheets and AI chats.

## Where it's going

A COMSOL-like workbench: direct 3D modelling in the viewport with a parametric history, full 3D CFD results views,
FEM on the same geometry, and an assistant that can turn "make a 50 mm tube two metres long and run the pressure
drop" into a reviewed sequence of steps.

## About me

Chemical engineering, Politecnico di Milano. Working on an R&D project in microalgae cultivation, which is what JarvisOS
was first built to serve.

If you're curious about building engineering software with AI — or about any of the above — get in touch.

<!-- Contact: LinkedIn profile URL -->
