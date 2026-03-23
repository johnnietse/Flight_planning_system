# Flight Planning System

A C-based flight planning and management system developed for ELEC 278 (Data Structures and Algorithms). This project allows users to manage airports, waypoints, aircraft types, and create detailed flight plans including departure/arrival information and intermediate waypoints.

## Features

- **Airport Management**: Add and retrieve airports using their names and ICAO codes (e.g., JFK, KBOS).
- **Waypoint Management**: Define navigation waypoints for flight routes.
- **Aircraft Management**: Register different aircraft types (e.g., B737, A320, Q400).
- **Flight Planning**:
    - Create unique flight plans with designated IDs.
    - Assign aircraft to flight plans.
    - Set departure and arrival airports with timestamps.
    - Add multiple waypoints to a flight route.
- **Reporting**:
    - Print detailed summaries for specific flight plans.
    - List all departures or arrivals for a given airport.

## Project Structure

- `main.c`: Test driver that initializes sample data and demonstrates system functionality.
- `FlightPlan.h/c`: Core logic for managing flight plans and coordinating between other modules.
- `AirportInfo.h/c`: Data structures and functions for airport information storage.
- `WaypointInfo.h/c`: Data structures and functions for waypoint information storage.
- `AircraftInfo.h/c`: Data structures and functions for aircraft type information storage.
- `CMakeLists.txt`: Build configuration file for CMake.

## Getting Started

### Prerequisites

- A C compiler (e.g., GCC, Clang, or MSVC).
- [CMake](https://cmake.org/download/) (version 3.26 or higher).

### Build Instructions

1.  Open a terminal in the project root directory.
2.  Create a build directory and navigate into it:
    ```bash
    mkdir build
    cd build
    ```
3.  Generate the build files:
    ```bash
    cmake ..
    ```
4.  Compile the project:
    ```bash
    cmake --build .
    ```

## Usage

After building, you can run the executable:

- **Windows**: `assignment.exe`
- **Linux/macOS**: `./assignment`

The `main.c` file provides a working example. It populates the system with several airports (JFK, Logan, etc.), waypoints, and aircraft types, then creates and prints several sample flight plans.

## API Overview (`FlightPlan.h`)

| Function | Description |
| :--- | :--- |
| `createFlightPlan(name)` | Creates a new flight plan and returns its unique ID. |
| `getFlightPlan(name)` | Retrieves the ID of an existing flight plan by name. |
| `setAircraft(fplan_id, id, type)` | Assigns an aircraft ID and type to a flight plan. |
| `setDeparture(fplan_id, airport, time)` | Sets the departure airport and time. |
| `setArrival(fplan_id, airport, time)` | Sets the arrival airport and estimated arrival time. |
| `addWaypointToFP(fplan_id, name)` | Adds a waypoint to the flight plan's route. |
| `printFlightPlan(fplan_id)` | Prints a detailed report for the flight plan. |
| `printDepartures(airport)` | Prints all departures for a specific airport. |

## License

