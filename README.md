# Smart Mall Evacuation & Surveillance Prototype

## Overview
This project is an interactive, web-based prototype designed to simulate an intelligent emergency evacuation and surveillance routing system for a large indoor facility (modeled after Lulu Mall). 

It demonstrates how physical sensors, dynamic pathfinding algorithms, and automated security cameras can integrate to guide users to safety during a zoned lockdown or hazard event.

## Key Features
* **Dynamic Grid Mapping:** The facility is represented as a digital occupancy grid divided into four distinct zones (A, B, C, and D).
* **Two-Pass Pathfinding Algorithm:** Uses Breadth-First Search (BFS) to calculate the absolute shortest route to the nearest emergency exit. 
    * *Pass 1:* Attempts to find a completely safe route avoiding all hazards.
    * *Pass 2:* If the user is trapped, calculates an "Emergency Extraction" route through the shortest possible hazard path.
* **Automated Camera Targeting:** Fixed security cameras automatically activate and draw a tracking line of sight to the center of any zone placed under lockdown.
* **Real-Time Telemetry Dashboard:** A live status feed updates instantly based on user location, camera status, and active threats.
* **Interactive Simulation:** Users can walk through the facility in real-time using keyboard controls and dynamically trigger hazards using a mouse.

## How to Run
This is a standalone, client-side web application. No server, database, or installation is required.
1. Download or save the code as an `.html` file (e.g., `evacuation-system.html`).
2. Double-click the file to open it in any modern web browser (Chrome, Edge, Firefox, Safari).

## Controls & Usage
* **Movement:** Use `W, A, S, D` or the `Arrow Keys` to move the blue user cursor around the map.
* **Zone Lockdown:** Check the boxes in the "Incident Command" panel and click **Trigger Zone Lockdown** to simulate a massive hazard in a specific sector.
* **Manual Hazards:** Set the tactical action dropdown to "Place Manual Blockage" and click anywhere on the walkable grid to spawn a custom hazard.
* **Teleport User:** Set the tactical action dropdown to "Teleport User" and click anywhere on the grid to instantly move the user cursor to test different trapping scenarios.

## Legend
* **Dark Grey Blocks:** Solid walls / Store spaces (Impassable)
* **Green Blocks:** Emergency Exits
* **Blue Pulsing Dot:** User Location
* **Blue Line + Arrows:** Standard Safe Evacuation Route
* **Red / Yellow Pulsing Dot:** User in Danger Zone
* **Orange Line + Arrows:** Emergency Extraction Route (Trapped User)
* **Red Squares:** Active Hazards / Blocked Paths

## Technical Stack
* **HTML5 Canvas:** For high-performance rendering of the map, entities, and path lines.
* **Vanilla JavaScript (ES6):** For the pathfinding logic and game loop.
* **CSS3:** For the dashboard UI and styling.
