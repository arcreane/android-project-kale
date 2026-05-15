[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/b_O8BvCE)

# Kinedex

Kinedex is a high-utility Android application designed to eliminate friction in fitness education. Instead of scrubbing through long videos to figure out how an exercise is performed, users can search for any movement to immediately access looping animations, targeted muscle data, and technical benefit details.

## Core Features

* **Motion Dictionary:** High-speed, searchable index of exercise animations.
* **Visual Form Guides:** Focused, looping visuals to ensure perfect execution.
* **Integrated Rest Timer:** A background-aware timer to manage workout recovery periods.
* **Responsive Layouts:** Full-screen immersive mode for landscape orientation.

---

## Technical Compliance

### 1. Multiple Activities and Intents

The application utilizes separate Activities for the Search Interface and Exercise Details.

* **Explicit Intents:** Used for navigation between the directory and detail views.
* **Implicit Intents:** Features a "Share" action to fulfill external application communication requirements.

### 2. Orientation Changes

The Detail Activity is optimized for orientation awareness. Users can rotate to landscape mode to transition the looping animation into a fullscreen view, ensuring a versatile UI.

### 3. Fragments and Data Exchange

Workout data (sets, reps, and descriptions) is managed via a dedicated **Fragment** hosted within the Details Activity. Data is exchanged dynamically to ensure context-specific content loading.

### 4. Menus and Real Actions

An **Options Menu** is integrated to handle functional actions, including category filtering and quick access to the Rest Timer, ensuring all UI actions are wired to underlying logic.

### 5. Advanced View Component

The search core utilizes a **RecyclerView** with a **Custom Adapter**. This ensures memory-efficient scrolling and dynamic data binding for the exercise library.

### 6. Themes and Styles

A strict design system is defined in `res/values`. The application uses no hard-coded colors, relying entirely on consistent XML styles and themes to maintain a professional aesthetic.

### 7. Hardware Features

To provide physical feedback, the application utilizes the phone's **Vibrator**. This hardware feature is triggered via the Rest Timer to signal the end of a break.

### 8. Services and Background Processing

The Rest Timer is implemented as a **Foreground Service**. This ensures the countdown remains active and persistent in the background while the user is away from the app.

---

## Tech Stack

* **Language:** Java
* **Platform:** Android SDK
* **Design:** XML Styles / Paged Media
* **Repository:** Created by GitHub Classroom
