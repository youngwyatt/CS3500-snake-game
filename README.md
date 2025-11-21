Online Multiplayer Snake Game

C# • .NET • Blazor WebAssembly • TCP Networking

A real-time multiplayer Snake game with a custom networking layer, Blazor GUI, and optional SQL leaderboard. Built for CS3500 Software Practice II.

⸻

Features: </br>
	•	Real-time online multiplayer gameplay </br>
	•	Custom TCP networking protocol (async / await)</br>
	•	Blazor WebAssembly front-end</br>
	•	Dynamic rendering of snakes, food, and world</br>
	•	JSON-based message passing</br>
	•	Client–server architecture</br>
	•	Optional SQL-backed leaderboard</br>
	•	Chat client & server using shared networking stack</br>

Project Structure: </br>
```text
Snake.sln
│
├── Networking/                 # Core networking logic
│   ├── Server.cs
│   ├── NetworkConnection.cs
│   └── Networking.csproj
│
├── GUI/                        # Blazor WebAssembly GUI
│   ├── GUI/
│   │   ├── Pages/SnakeGUI.razor
│   │   ├── Controllers/NetworkController.cs
│   │   ├── Models/
│   │   │   ├── Snake.cs
│   │   │   ├── World.cs
│   │   │   ├── Wall.cs
│   │   │   └── Power.cs
│   │   └── GUI.csproj
│   └── GUI.Client/
│
├── ChatClient/                 # Multiplayer chat system
├── ChatServer/
│
└── WebServer/                  # Supporting web server
```
How the Game Works</br>

1. Input:</br>
Player presses an arrow key → client sends command to server.</br>

2. Server Loop:</br>
Processes all client inputs → updates world state → resolves collisions.</br>

3. Broadcast:</br>
Server sends updated world to all clients each frame.</br>

4. Rendering:</br>
Blazor GUI redraws the game world in real time.</br>

⸻

Networking Highlights</br>
	•	Asynchronous TCP I/O using Task</br>
	•	Concurrent message loops for read/write</br>
	•	JSON world-state packets</br>
	•	Thread-safe message queues</br>
	•	Heartbeats + disconnect handling</br>
	•	Designed to support many simultaneous clients</br>

⸻

SQL Leaderboard </br>
	•	Stores player names and high scores</br>
	•	Inserts scores automatically at match end</br>
	•	Uses parameterized queries</br>
	•	Displays leaderboard in GUI</br>

⸻

Data Models</br>
	•	World — board size, food, snakes, walls</br>
	•	Snake — segments, direction, living/defeated state</br>
	•	Wall — static obstacles</br>
	•	Power — food / items</br>
	•	Point2D — basic geometry</br>

⸻

Skills Demonstrated</br>
	•	Distributed systems with client–server architecture</br>
	•	C# object-oriented design</br>
	•	Multi-project .NET solution</br>
	•	Asynchronous networking</br>
	•	Blazor WebAssembly front-end development</br>
	•	State synchronization in real-time systems</br>
	•	JSON serialization/deserialization</br>
	•	SQL integration</br>
	•	Concurrent threads and safe message passing</br>
