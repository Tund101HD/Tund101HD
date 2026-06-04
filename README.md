# Hey there 👋

```asm
; ──────────────────────────────────────────────────────────
;  whoami.asm — Luca Perri
;  nasm -f elf64 whoami.asm && ld -o whoami whoami.o
; ──────────────────────────────────────────────────────────

section .data
    name    db  "Luca Perri", 0xA
    nlen    equ $ - name
    role    db  "Embedded Systems & Aerospace Engineering", 0xA
    rlen    equ $ - role
    uni     db  "DHBW Ravensburg - Campus Friedrichshafen", 0xA
    ulen    equ $ - uni
    motto   db  "Building tools that bridge bare metal and big ideas.", 0xA
    mlen    equ $ - motto

section .text
    global _start

_start:
    mov rax, 1              ; sys_write
    mov rdi, 1              ; fd = stdout
    mov rsi, name
    mov rdx, nlen
    syscall

    mov rax, 1
    mov rdi, 1
    mov rsi, role
    mov rdx, rlen
    syscall

    mov rax, 1
    mov rdi, 1
    mov rsi, uni
    mov rdx, ulen
    syscall

    mov rax, 1
    mov rdi, 1
    mov rsi, motto
    mov rdx, mlen
    syscall

    mov rax, 60             ; sys_exit
    xor rdi, rdi            ; exit code 0
    syscall
```

I'm a working student and dual-study engineer from southern Germany. I build developer tools, full-stack applications, and anything that makes circuits — digital or redstone — easier to reason about.

---

## Featured Projects

### [Advanced Assembly for CLion](https://github.com/Tund101HD/clion-assembly-plugin) &nbsp; [![JetBrains Marketplace](https://img.shields.io/badge/Marketplace-Advanced%20Assembly-blue?logo=jetbrains)](https://plugins.jetbrains.com/plugin/31969-advanced-assembly)

First-class **NASM** (x86/x64) and **MIPS** (MIPS32) support for JetBrains CLion — syntax highlighting, context-aware completion, 11 inspections, cross-file navigation, and a working **QEMU-backed debugger** with gutter breakpoints. Project generation, CMake integration, and transparent WSL support on Windows.

`Kotlin` · `JFlex / Grammar-Kit` · `IntelliJ Platform SDK` · `QEMU`

> [Feature tour & walkthroughs](https://lucidev.me/tools/clion-assembly-plugin) · [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/31969-advanced-assembly)

---

### CircuitForge &nbsp; *(work in progress)*

A browser-based redstone circuit editor: drag logic gates onto a canvas, wire them up, and export a **Minecraft schematic** (`.schem` / `.litematic`). The engine handles placement via topological sort + ASAP layering, routes wires with 3D A\*, inserts repeaters, validates signal strength, and detects crosstalk — 156 tests, OpenAPI spec, zero stubs.

**Engine** — `Kotlin/Ktor` · `knbt` · `Supabase` · `A* pathfinding` · `NBT serialization`
**Web** — `Next.js` · `React Flow` · `Supabase` · `Prisma` · `Tailwind`

---

### [Okay Jarvis, how do I...?](https://github.com/Tund101HD/Okay-Jarvis-how-do-I-)

A growing knowledge-sharing repo — concise guides and references on topics I've learned the hard way.

---

## Tech I work with

#### Systems & Low-Level
![C](https://img.shields.io/badge/C-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Assembly](https://img.shields.io/badge/Assembly-NASM%20%7C%20MIPS-6E4C13?style=for-the-badge)
![Kotlin](https://img.shields.io/badge/Kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)

#### Web & App
![TypeScript](https://img.shields.io/badge/TypeScript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)

#### Backend & Data
![Ktor](https://img.shields.io/badge/Ktor-087CFA?style=for-the-badge&logo=ktor&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)

#### Tooling & Platforms
![JetBrains](https://img.shields.io/badge/IntelliJ%20Platform%20SDK-000000?style=for-the-badge&logo=jetbrains&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=for-the-badge&logo=qemu&logoColor=white)

---

## Currently exploring

![Rust](https://img.shields.io/badge/Rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Postgres](https://img.shields.io/badge/Postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

Rust for systems work, PyTorch for ML on embedded, cloud infra for scaling CircuitForge, and Postgres to replace my current DB stack where it makes sense.

---

## Stats


<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Tund101HD&theme=tokyo-night&hide_border=true&area=true" width="95%" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Tund101HD/Tund101HD/output/github-snake-dark.svg" width="95%" />
</p>

---

## Connect

[![Portfolio](https://img.shields.io/badge/lucidev.me-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://lucidev.me/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lucag-perri)
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://instagram.com/lucag.perri)
[![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?style=for-the-badge&logo=discord&logoColor=white)](https://discord.com/users/966775587152756766)
[![X](https://img.shields.io/badge/Follow%20on%20X-%20?style=for-the-badge&color=%23000203)](https://x.com/LucaG_Perri)
