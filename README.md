Realms of Elementa

Week 2 Features & Updates

Here is a summary of the new mechanics, updates, and architectural improvements introduced in Week 2:

Custom Theme Music: Integrated dynamic, realm-specific background music composed by my brother (including tracks like Aqua_Main_Theme.mp3 and Ignis_Main_Theme.mp3) that play when visiting corresponding regions.

World Map Navigation & Fast Travel: Added full navigation across the four elemental realms (Aer, Aqua, Terra, and Ignis) with a fast-travel region selection menu.

NPC Interactions & Merchant Shop: Integrated dialogue parsing from JSON files alongside a functional Merchant Shop interface hosted by Gwen, allowing players to purchase health elixirs and mana potions using accumulated gold.

2D Camera Movement: Implemented bounded 2D camera tracking that follows the player with smooth zooming and boundary constraints tailored to each region hub.

Building Entrances & Collision Hitboxes: Added interactive building hitboxes, distinct roof and door visuals, interior floor maps, and strict wall collision detection.

Encapsulated Inventory & In-Combat Items: Upgraded the inventory system to a strictly encapsulated Inventory class supporting initializer lists, safe item stacking/removal, and quick-use healing consumables directly within combat.

Dynamic Enemy AI: Introduced autonomous movement logic for enemies, including state-based behaviors (Idle, Chase, Leash/Return to Spawn) and automatic combat triggering upon contact.

Controls & How to Play

Player Movement & World Interactions

W / A / S / D or Arrow Keys: Move the player.

F: Interact with NPCs, enter buildings, select destinations on the world map, or trigger fast travel.

Q: Toggle the fast-travel map window.

E: Pick up items from the ground within the region hub.

F5: Quick save current game progress.

Inventory & Shop Navigation

I: Open or close the inventory screen.

W / S or Up / Down Arrow Keys: Navigate through items in the inventory or shop menu.

E or ENTER: Use selected item in the inventory, or buy selected item in the shop.

ESC or I: Close the merchant shop.

Combat System

Proximity Touch: Move into an active enemy to initiate combat.

1 - 9: Execute selected attack or spell based on the available skills list.

H: Use a Health Elixir from your inventory to heal during your turn.

R: Attempt to run away from the combat encounter.

ENTER: Confirm combat victory or wake up after defeat.

Compilation & Installation Guide

You can either run the precompiled binary from the official release or compile the project from the source code.

Option 1: Running the Precompiled Binary (GitHub Release v2)

Go to the Releases section of the GitHub repository.

Download the RealmsOfElementa-v2.zip release package.

Extract the contents of the archive to a local folder.

Ensure the assets/ folder remains in the exact same directory as the executable file.

Launch GameEngine.exe to run the game.

Option 2: Compiling from Source Code

Prerequisites

C++17 compatible compiler (MSVC, GCC, or Clang).

Raylib library (version 4.0 or newer).

Dear ImGui library with rlImGui integration bindings.

Build Instructions

Clone the repository:

git clone https://github.com/your-username/realms-of-elementa.git
cd realms-of-elementa


Configure your compiler or build tool (CMake, Visual Studio solution, or Makefile) to link against Raylib and system dependencies (opengl32, gdi32, winmm on Windows).

Ensure the project structure includes external/imgui and external/rlImGui headers during compilation.

Build the executable.

Copy the assets/ directory into your output build directory alongside the compiled executable.

Execute the compiled binary to play.
