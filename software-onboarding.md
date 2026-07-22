# ThunderStrike FTC #33535 — Software Engineer Onboarding

A ground-zero path to a productive contributor on the team's robot control software — from no programming at all to opening your first reviewed pull request. Every resource below is free and current.

| | |
|---|---|
| **Start point** | little / no coding |
| **Target** | ship a reviewed PR |
| **Pace** | ~6 weeks part-time |
| **Cost** | $0 — all free |
| **Stack** | Java 8 · Android · FTC SDK |

> **How to use this.** Work the phases in order — each assumes the one before it. The Git track runs in parallel: start it in Week 2 and use it for everything after. You are not expected to master a topic before moving on; you are expected to be able to *follow along* in the codebase. Pair with your assigned mentor early and often. On-robot testing is done by the Product Owner — your loop is write, build, get reviewed.

**Track legend:** **Core** = the main sequence · **Parallel** = runs alongside the core.

---

## The Path

### Phase 0 — Setup & Orientation
*Day 1 · ~2–3h · Core*

Get accounts, tools, and the repository on your machine — and read where you've landed. Do not write code yet; just get everything opening cleanly.

- **Create a GitHub account & get invited to the team** — *setup · 15m.* Your identity for every change you make.
- **Install the toolchain: JDK, Android Studio, Git** — *setup · 1–2h.* Follow the [FTC "Installing Android Studio" guide](https://ftc-docs.firstinspires.org/en/latest/programming_resources/tutorial_specific/android_studio/installing_android_studio/Installing-Android-Studio.html) (it pairs Studio with the right JDK), or the [official Android Studio install guide](https://developer.android.com/studio/install). Then clone the repo, open it in Android Studio, and let Gradle finish syncing once.
- **Read the team README and Engineering Process** — *read · 45m.* `README.md` and `doc/engineering-process.md`. Orientation only; don't try to absorb it all.

### Phase 1 — Programming Foundations
*Week 1 · ~8–12h · Core*

Learn what a program *is* — variables, conditionals, loops, functions — in a low-noise language before Java's syntax piles on. These ideas transfer directly.

- **[Intro to Python Fundamentals](https://www.khanacademy.org/computing/intro-to-python-fundamentals)** — *interactive · self-paced · Khan Academy.* Runs in the browser, zero setup, assumes no experience. Python teaches the concepts cleanly; you'll switch to Java next.

### Phase 2 — Java & Object-Oriented Programming
*Weeks 2–3 · ~20–25h · Core*

The whole codebase is Java. Learn the language, then the object-oriented model (classes, objects, inheritance, interfaces, polymorphism) — this is the single most important phase.

- **[Learn Java Programming (v17)](https://youtu.be/A74TOX803D0)** — *video · 4h · freeCodeCamp.* One sitting, no signup: variables through arrays, ending in OOP. Watch first.
- **[Learn Java](https://www.codecademy.com/learn/learn-java)** — *interactive · ~17h · Codecademy (free course).* Hands-on; the OOP unit has you write your own classes, which is where it sticks. Ignore the Pro upsell.
- **[Learn Java for FTC](https://github.com/alan412/LearnJavaForFTC)** *(free PDF)* — *book · self-paced · Alan G. Smith.* The bridge: Java taught through motors, servos, sensors, gamepads, and OpModes. Read as you enter Phase 5.

### Phase 3 — Git & GitHub
*From Week 2 · ~3–4h · Parallel*

Version control and the pull-request workflow — how every change on this team is made, reviewed, and merged. Start alongside Java; you'll use it for the rest of your time here.

- **[Introduction to GitHub](https://github.com/skills/introduction-to-github)** — *interactive · <1h · GitHub Skills (official).* Learn repos, branches, commits, and opening a PR by doing it in a real repo. Best starting point.
- **[Review Pull Requests](https://github.com/skills/review-pull-requests)** — *interactive · <30m · GitHub Skills (official).* Requesting a review, suggesting changes, approving — the collaboration half of PRs.
- **[Resolve Merge Conflicts](https://github.com/skills/resolve-merge-conflicts)** — *interactive · <30m · GitHub Skills (official).* What causes conflicts and how to fix them without fear.
- **Read the team Git Protocol** — *read · 30m.* `.claude/skills/git-protocol`. Our branch naming, commit, and PR rules. Follow it exactly.

### Phase 4 — Android Studio, Deploying & Debugging
*Weeks 3–4 · ~8–10h · Core*

The robot code is a Java Android app. Learn the editor, build and install the APK onto the Control Hub, connect over ADB, read the logs when something breaks, and watch live data on the dashboard.

- **[Creating and Running an OpMode](https://ftc-docs.firstinspires.org/en/latest/programming_resources/tutorial_specific/android_studio/creating_op_modes/Creating-and-Running-an-Op-Mode-(Android-Studio).html)** — *docs · ~30m · FTC (official) · Java.* Studio is already installed and synced from Phase 0; here you open the robot project, then create, build, and install your first OpMode APK to the Robot Controller.
- **[Using Android Studio](https://gm0.org/en/latest/docs/software/getting-started/using-android-studio.html)** — *guide · ~20m · gm0 · Java.* The IDE layout, the Gradle build, deploying to the Control Hub over USB or wireless, and a first look at ADB and logcat.
- **[Build and run your app](https://developer.android.com/studio/run)** — *docs · reference · Android (official).* Language-neutral reference for what the Run button does and where the built APK lands.
- **[Gradle — Getting Started](https://docs.gradle.org/current/userguide/getting_started.html)** — *docs · ~1h · Gradle (official).* What Gradle is, plus tasks, dependencies, and the `./gradlew` wrapper. This is the tool behind `assembleDebug`; our build files are Groovy `.gradle` (`build.dependencies.gradle` and `TeamCode/build.gradle`).
- **[Managing a Control Hub](https://ftc-docs.firstinspires.org/en/latest/programming_resources/shared/managing_control_hub/Managing-a-Control-Hub.html)** *(wireless ADB)* — *docs · ~15m · FTC (official).* The authoritative steps to reach the Control Hub over Wi-Fi so you can deploy and pull logs without a cable.
- **[Android Debug Bridge (adb)](https://developer.android.com/tools/adb)** — *reference · ~30m · Android (official).* The command reference: `adb connect`, `adb devices`, and `adb pull` to copy DataLogger CSV files off the hub.
- **[Common Issues](https://gm0.org/en/latest/docs/software/getting-started/common-issues.html)** + **[Logcat](https://developer.android.com/tools/logcat)** — *guide + reference · gm0 · Android (official).* Read a crash log and stack trace by example, then the definitive logcat reference for filtering the crash buffer.
- **[FTC Dashboard — Getting Started](https://acmerobotics.github.io/ftc-dashboard/gettingstarted.html)** + **[Features](https://acmerobotics.github.io/ftc-dashboard/features.html)** — *docs · ~30m · ACME Robotics.* Connect in a browser, then plot values over time, draw the field overlay, and tune `@Config` parameters live.
- **[Panels — Telemetry](https://ftcontrol.bylazar.com/docs/panels/telemetry/)** — *docs · ~20m · Bylazar.* Our advanced dashboard: field view, telemetry, and live graphing. Read after FTC Dashboard.

> **On our robot.** We build with `./gradlew assembleDebug` and deploy the APK to the REV Control Hub. Pull logs with `adb`; watch live data on FTC Dashboard (port 8080) and Panels (port 8001). You'll learn our exact flow with your mentor once you can build cleanly.

### Phase 5 — The FTC Robotics Stack
*Weeks 4–5 · ~10–15h · Core*

Now the domain: how FTC robot code is structured (OpModes, hardware mapping, gamepads) and the two libraries this robot relies on for autonomous movement.

- **[Game Manual 0 — Software](https://gm0.org/en/latest/)** — *tutorials · ~1–2h · gm0 (community).* The most-recommended free FTC learning resource. Start with the "Getting Started" software pages.
- **[Official FTC Documentation](https://ftc-docs.firstinspires.org/en/latest/)** — *docs · reference · FIRST (official).* Authoritative install + first-OpMode guide, always current for the active season.
- **[Getting Started Programming your FTC Robot in Java](https://www.youtube.com/watch?v=fbSiZSnPf-U)** — *video · intro · YouTube.* A watch-along first OpMode if you prefer video before docs.
- **Our hardware & safety rules** — *read · 30m · README § Wiring.* The wiring table that maps each motor and sensor name to a real port. Two rules: the names in code must match the Robot Configuration File exactly — renaming one breaks the robot — and you never run OpModes on the physical robot yourself; the Product Owner does that.
- **[Get Started with Pedro Pathing](https://www.youtube.com/watch?v=6v7QgzRhOwA)** + **[docs](https://pedropathing.com/)** — *video + docs · Pedro Pathing.* Our autonomous path-following library. The Nov 2025 setup video matches our version.
- **[NextFTC Guide](https://nextftc.dev/guide/about)** — *docs · ~1–2h · NextFTC (official).* Our command-based library. Documentation-first (no video series yet); code-along in Java.

> **Our versions.** FTC SDK `11.0.0` · Pedro Pathing `2.0.5` · NextFTC `1.1.0`. When docs and our code disagree, our pinned version wins — read the source for the version we use.

### Phase 6 — Our Codebase & First PR
*Weeks 5–6 · ongoing · Core*

Turn general knowledge into *this* robot. Learn how our software is organized, our rules, and then ship a small change end to end.

- **Architecture: the control loop & coordinate systems** — *read · 2h · README § Software Architecture.* The 50 Hz five-phase state-machine loop, the subsystems, and FTC (mm/degrees) vs Pedro (inches/radians) coordinates.
- **Coding Conventions** — *read · 30m · README § Coding Conventions.* No-allocation hot paths, no magic numbers, short single-purpose methods, comprehensive comments.
- **Real-time constraints (advanced)** — *read · advanced · README § Performance.* Why we avoid creating objects and doing extra hub reads inside the ~50 Hz loop: object creation causes stutter-inducing garbage-collection pauses, and each hub read is a slow round-trip. Save this for after your first PR.
- **The PBI lifecycle & Definition of Done** — *read · 30m · `doc/engineering-process.md`.* How work flows: code changes happen only in the Implementation stage; a PR isn't done until the PO accepts it.
- **Running the unit tests** — *hands-on · 30m.* `./gradlew :TeamCode:testDebugUnitTest`. See `TeamCode/src/test/README.md` for the harness.
- **Capstone — your first PBI** — *guided · 1 week · with a mentor.* Pick up a small starter task, branch, implement, get it reviewed, open a PR. This is the finish line.

---

## Control Software Concepts

The ideas the codebase is built on. Dip into these while working through Phases 5–6 — they explain *why* the subsystems look the way they do. Video where a good one exists; two are best learned from short articles, and that's flagged.

- **[The control loop: sense → decide → act](https://gm0.org/en/latest/docs/software/getting-started/linear-opmode-vs-opmode.html)** + **[why it runs at a fixed rate](https://gameprogrammingpatterns.com/game-loop.html)** — *articles · ~20m · gm0 · Game Programming Patterns.* Read inputs, decide, then act, repeated ~50 times a second. No strong beginner video exists here, so it's text. This is the shape of every loop in the code.
- **[State machines](https://www.youtube.com/watch?v=sNFMdLEVxFo)** + **[Mealy vs Moore](https://www.youtube.com/watch?v=ublVFRXOdZo)** — *video · ~20m · YouTube · Neso Academy.* States and transitions, then the Moore-vs-Mealy distinction. Our robot software is a Moore machine: outputs depend only on state.
- **[Command-based programming](https://www.youtube.com/watch?v=VoxeXqy1bdQ)** + **[WPILib explainer](https://docs.wpilib.org/en/stable/docs/software/commandbased/what-is-command-based.html)** — *video + docs · FRC 0 to Autonomous · WPILib.* Behavior organized into commands and subsystems that get scheduled, running in sequence or in parallel. The model behind our NextFTC library.
- **[Closed-loop control: PID](https://www.youtube.com/watch?v=UR0hOmjaHp0)** — *video · ~10m · Brian Douglas.* Correcting error toward a target, with almost no math. How the shooter holds a set flywheel speed.
- **[Feedforward (and PIDF)](https://gm0.org/en/latest/docs/software/concepts/control-loops.html)** + **[flywheel example](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/introduction/tuning-flywheel.html)** — *docs · ~15m · gm0 · WPILib.* Predicting the output you need instead of only reacting to error: the "F" in the shooter's PIDF. gm0 covers PID and feedforward together, no calculus. No clean beginner video exists here.
- **[Odometry & localization](https://www.youtube.com/watch?v=ixsxDn_ddLE)** + **[gm0 concept page](https://gm0.org/en/latest/docs/software/concepts/odometry.html)** — *video · ~10m · The Clueless (FTC) · gm0.* How the robot tracks its position and heading from wheel encoders and the IMU. Our Pinpoint does this with sensor fusion.
- **[Mecanum kinematics](https://www.youtube.com/watch?v=noqBUEgyQ8A)** + **[gm0 holonomic drives](https://gm0.org/en/latest/docs/common-mechanisms/drivetrains/holonomic.html)** — *video · ~9m · Lesics · gm0.* How four angled-roller wheels combine into forward, strafe, and turn. This is our drivetrain.

---

## What Else Is Missing — Proposals

These aren't in the generic courses above but a team contributor needs them. Fold them into the phases or run them as short mentor-led sessions.

1. **FTC field geometry & frames** — The field coordinate system, our mm/degree convention, and where the season's field elements sit. Read the README coordinate section with the field diagrams open.
2. **Mentorship & review etiquette** — Assign a mentor on Day 1, pair on the first PBI, and set expectations for giving and receiving code review kindly and specifically.
3. **Access checklist** — One list to grant everything: GitHub org invite, ClickUp board, team chat, and robot-lab access. Nothing blocks a new hire faster than missing access.

---

*Timeline is a guide for part-time study, not a deadline — adjust to the person. All external courses were free and resolving when this program was assembled; re-check links each intake, especially any Udemy alternative, whose free status can change.*
