# IGCN Server Suite 9.5.1.20

This repository contains the source code for **IGCN Server Suite** version 9.5.1.20. It is a collection of Windows C++ applications used to host a private MU Online server.

## Projects

The solution `GameServer_x9.5.sln` includes the following components:

- **ConnectServer** – Accepts connections from the game client and provides a list of available game servers.
- **DataServer** – Manages the SQL database, item data, and server configuration.
- **GameServer** – Implements gameplay logic, character actions, and networking between clients.
- **IGC_DLL_S9E2** – Client-side DLL used for additional hooks and anti-hack features.

Each project builds a separate executable or DLL. Precompiled resource scripts and icons are also included.

## Dependencies

- **Windows**: the code uses WinAPI APIs, ODBC, and other Windows libraries.
- **Visual Studio**: project files were created with Visual Studio 2015 (solution format 12.00). The projects require platform toolsets `v140_xp` (for the client DLL) or `v143` (for the servers). Visual Studio 2022 with the Windows 10 SDK and the optional v140 toolset can build all targets.
- **pugixml**: a lightweight XML parser included in the source tree for reading configuration files.
- **ODBC**: DataServer links against `odbc32.lib` and `odbccp32.lib` for database connectivity (typically MS SQL Server).

## Building

1. Install Visual Studio 2022 (or later) with the Windows 10 SDK and the optional "v140" toolset for XP compatibility.
2. Open `GameServer_x9.5.sln` in Visual Studio.
3. Select the desired configuration (Debug or Release) and platform (Win32 or x64).
4. Build the solution to produce the server executables and client DLL.

## Notes

This repository is provided without build scripts, documentation, or a license. Refer to the source code for further details about configuration files and runtime requirements.
