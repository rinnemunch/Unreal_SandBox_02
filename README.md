# 🧩 Unreal Engine Blueprint Showcase

A curated collection of **Unreal Engine 5.5.4** mini-projects — each one a focused, standalone system built to demonstrate clean, production-level Blueprint design.
Every project targets a core gameplay or visual mechanic that can scale into full systems for professional Unreal development.

---

## 🎞️ Project Gallery

![Project Showcase](Media/5.gif)

Explore the projects below 👇
Each entry includes a **Blueprint workflow**, **GIF preview**, and **feature breakdown** — perfect for learning, prototyping, or integrating directly into your own UE projects.

# 💬 Project 1 – On-Screen HUD Tips

This project demonstrates how to create **automatic on-screen HUD tips** in **Unreal Engine 5.5.4** using Blueprints.
It’s a lightweight, polished system that displays short text prompts when players enter trigger zones — perfect for tutorials, hints, or in-world storytelling.

---

## 🖼️ Preview

![HUD Tips Preview](Media/HUDTips.gif)

---

## 🧱 Features

- **WBP_HUDTip** widget with transparent multi-line text box
- **Fade animation** for smooth appearance and disappearance
- **FadeCE custom event** to control UI transitions
- **BP_TriggerZone** actor with overlap detection and player reference
- **Automatic widget creation and removal** during gameplay
- Modular setup — easy to expand for **quest markers**, **tutorials**, or **interactive world prompts**

# 🤖 Project 2 – Following AI Companion

This project demonstrates how to create a **custom AI companion** in **Unreal Engine 5.5.4** using Blueprints.
It blends **AI behavior** and **character design** to build a companion that not only follows the player but also moves and looks uniquely yours — adding personality, rhythm, and presence to the game world.

---

## 🖼️ Preview

![AI Companion Preview](Media/AI.gif)

---

## 🧱 Features

- **BP_Companion** character duplicated from the player for independent AI control
- **ABP_Companion** animation blueprint with modified skeletal proportions
- **Transform (Modify) Bone** setup to give the companion a unique appearance
- **Pawn Sensing** and **AI Move To** nodes for automatic player tracking
- **Navigation Mesh Bounds Volume** for smooth AI movement within the level
- Modular structure — extendable for **pets**, **followers**, or **story-driven NPCs**

---

# 🥊 Project 3 – Melee Attack Animation Integration

This project shows how to **retarget and trigger melee attack animations** for Unreal Engine 5.5.4’s default Third-Person Character using the **IK Retargeter** and **Blueprint input logic**.

It’s the foundation for a full melee combat system — clean, responsive, and ready to expand into combos, hit detection, and impact feedback.

---

## 🖼️ Preview

![Melee Attack Preview](Media/Melee.gif)

---

## 🧱 Features

- **RamsterZ Free Anims Volume 1** imported and prepped for retargeting
- **IK Retargeter** setup for converting external animation to SKM_Manny
- **Root Motion** enabled for realistic movement synchronization
- **Attack_Montage** created for Blueprint-triggered playback
- **Left Mouse Input** logic added to play montage with `isAttacking` lock
- Expandable base — ready for **combo chains**, **hit reactions**, and **timing windows**

---

# 🎬 Project 4 – Cinematic Camera Fade-In on Begin Play

This project demonstrates how to create a **cinematic camera fade-in effect** in **Unreal Engine 5.5.4** using Blueprints.
It delivers a smooth visual transition from black to your scene at game start — a small, professional touch that sets the tone and boosts immersion instantly.

---

## 🖼️ Preview

![Camera Fade Preview](Media/CameraFade.gif)

---

## 🧱 Features

- **BP_ThirdPersonCharacter** fade logic triggered on **Begin Play**
- Uses **Get Player Camera Manager** and **Start Camera Fade** nodes
- **From Alpha 1.0 → To Alpha 0.0** for full black-to-scene transition
- Adjustable **Fade Duration** for pacing control (e.g., 5 seconds for cinematic feel)
- Customizable **Fade Color** for tone or narrative mood

---

# 💥 Project 5 – Precise Melee Hits: Knockouts & Hit Detection

This project expands the **melee combat system** with **precise, reactive hit detection** and **ragdoll knockouts**, all built in **Unreal Engine 5.5.4** using Blueprints only.
It builds directly on the _Wandering AI_ and _Melee Combat_ setups — turning every swing into a physical, cinematic impact that connects cleanly with NPCs.

---

## 🖼️ Preview

![Melee Knockout Preview](Media/MeleeKnockout.gif)

---

## 🧱 Features

- **ANS_Hit** custom notify state defining the active hit window in the attack montage
- **Real-time hit detection** using `Sphere Trace for Objects` linked to animation notifies
- **BP_ThirdPersonCharacter** `HitDetection` function handling trace and NPC detection
- **BP_NPC** ragdoll response triggered instantly on successful hit
- **Add Impulse** physics push for knockout realism and visual impact
- Seamless integration with existing **AI wandering** and **melee attack** systems

---

## ⚙️ Technical Breakdown

- **Notify State Timing:** Active window covers attack swing (e.g., frame 10–53)
- **Trace Filtering:** Detects only `Pawn` object types for performance and precision
- **Hit Response:** Casts to `BP_NPC` and triggers `ActivateRagdoll()`
- **Physics Simulation:** Mesh simulation + directional impulse for knockout motion
- **Radius Control:** Adjustable trace radius (default: `50`) for close-range accuracy

---

## 🚀 Result

When you attack a wandering NPC, your melee swing now delivers a **real, timed impact**.
Each successful hit instantly drops the target into ragdoll with a subtle forward impulse — producing clean, satisfying knockouts that look and feel physically grounded.

---

# 🌀 Project 6 – Double Jump Flip System

This project shows how to create a **stylish mid-air flip animation** that triggers automatically on your **second jump** in **Unreal Engine 5.5.4**.
It combines jump logic and animation control to deliver a clean, acrobatic backflip that feels fluid, responsive, and cinematic — ideal for parkour or action-focused characters.

---

## 🖼️ Preview

![Double Jump Flip Preview](Media/DoubleJumpFlip.gif)

---

## 🧱 Features

- **BP_ThirdPersonCharacter** modified for double jump support
- **Switch on Int** logic to trigger unique animation on the second jump
- **HalfBackflip_Montage** animation plays only mid-air
- **Rate Scale** and **End Time** tuned for smooth cinematic timing
- Fully Blueprint-based — no C++ required
- Modular design ready for **aerial combos**, **parkour systems**, or **character flair moves**

---

## ⚙️ Technical Breakdown

- **Jump Max Count:** Set to `2` for double jump capability
- **Get Jump Current Count:** Feeds into **Switch on Int** for jump stage tracking
- **Second Jump Branch:** Executes `Play Anim Montage` for the flip
- **Montage Settings:** Rate Scale `0.7`, End Time `0.39` for tighter motion control

---

## 🚀 Result

On the **first jump**, your character performs a normal leap.
On the **second jump**, they perform a clean **backflip** mid-air — no extra input needed.
The system feels precise, cinematic, and adds effortless style to your character movement.
