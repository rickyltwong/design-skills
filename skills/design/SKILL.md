---
name: design
description: Ask which design skill fits a UI or motion request, typed as `/design <request>`. A router over the skills in this repo; it hands the request to the one skill that owns it.
disable-model-invocation: true
---

# Design

Route the request to one skill below, then hand off. The chosen skill's SKILL.md owns the work; do not restate its rules here or answer from memory.

1. Match the request to the first row that fits, in this order: platform (Expo, Swift), then problem (jank, mobile web, worst-case data, toasts), then the verb (build, review, audit, find, name, compare).
2. Two rows fit equally -> ask one question that separates them.
3. A model-invocable skill -> invoke it with the user's request, unchanged.
4. A skill marked † runs only when the user types it -> reply with the exact command, for example `/prototype a pricing card with three tiers`, and one line on why it fits. Do not run it yourself.
5. Nothing fits -> say so and name the two closest skills.

| Request | Skill |
|---|---|
| Animate anything in React Native or Expo: gestures, sheets, screen transitions, press feedback, haptics | `animate-expo` |
| Write, review or migrate Swift; a concurrency error, hang, data race or retain cycle | `write-swift` |
| A web animation is janky or drops frames; which property to animate; CSS vs JS on performance; `will-change` | `animation-performance` |
| A web app feels wrong on a phone: sticky hover, 100vh, input zoom, safe areas, PWA, touch carousels | `mobile-native` |
| Stress-test a component or screen with worst-case data | `break-ui` |
| Sonner: setup, toast calls, styling, toasts that don't appear or appear twice | `ask-sonner` |
| Build a new web animation or transition, add motion, make a component feel alive | `animate` |
| Gesture-driven UI, springs, momentum, interruptible transitions, materials and depth, Apple-style feel | `apple-design` |
| Review the motion in a diff or a component | `review-animations` † |
| Audit every animation in a codebase and plan the fixes | `improve-animations` |
| Find places that should animate but don't | `find-animation-opportunities` |
| "What's it called when…": name a motion effect | `animation-vocabulary` |
| Pick a library for a frontend task: charts, OTP, command menu, drag and drop, virtualization | `pick-ui-library` † |
| Several different versions of a UI piece to flip between | `prototype` † |
| General UI polish, component design or design critique that no row above covers | `emil-design-eng` |

A request that spans two skills, for example "build this sheet, then make sure it holds 60fps": run the first skill, then name the second as the next step.
