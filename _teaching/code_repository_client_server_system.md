---
title: "Code Repository Client/Server System"
collection: teaching
type: "C++, WPF, WCF, C#, C++/CLI, GUI"
permalink: /project/code_repository_client_server_system
date: 2018-1-1
---

<span style="color: #666666; font-size: 0.8em;">A C++ based code repo system.</span>

[Link to GitHub](https://github.com/ZzzGin/code_repo)

- Check in/out files, version management, file browser supported
- Developed a NoSQL database with C++
- A file and directory operations module in C++
- WPF for UI design
- WCF for communication between C/S
- Object oriented design (OOD), all modules have test sets and necessary comments.
  - GUI (C# WPF Application)
    - Demonstrates C# user interface sending messages through native C++ communication channel to a remote server.
    - Connects to channel through Translater
  - Translater (C++\CLI dll)
    - Defines managed message class
    - Translates managed messages and strings to native messages and strings and vice versa.
    - Connects to channel via the CommLibWrapper.
    - Managed code (C++\CLI) is isolated from native code (C++) using IComm interface and CommLibWrapper factory
  - MessagePassingComm (C++)
    - Sends messages through socket-based one-way channels
    - Sends files as a series of chunks with message headers
    - Each endpoint has both a sender and receiver, wrapped in a Comm object
  - Sockets (C++)
    - Socket library the supports both IP4 and IP6 protocols
    - Provides three classes Socket, SocketConnector, and SocketListener
  - Message (C++)
    - Defines messages as collections of attributes
  - ServerPrototype (C++)
    - Processes incoming messages based on ServerProc callable objects, keyed to a message's command attribute
  - FileSystem (C++)
    - Provides static functions for managing files, paths, and directories