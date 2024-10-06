## Welcome!

[![LinkedIn: matthieudreher](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/matthieu-dreher)

Hello! I'm Matthieu Dreher, a mainly C++/Python developer with a background in high-performance computing and currently looking for new challenges! Welcome to my personnal projects! Here you will find some personnal projects focused on molecular dynamics as well as some for fun projects. 
All these projects were or are currently being developped with the goal to learn new technologies/frameworks/languages. If you see something interesting which could use some improvements, please do not hesitate to submit a ticket.

## Molecular Dynamics Environment and Tools

My current goal is to provide an environment allowing users to:
- Define a simulation workflow for molecular dynamics
- Generate the corresponding inputs for a simlation backend (Lammps, Gromacs)
- Provide ways to execute a simulation on local or remote compute resources
- Allow live visualization, steering, and analysis of the simulation
  
This is a massive tasks which has to be divided into several projects. You'll find some of these projects below, as well as a TODO list for soonTM.

### Godrick

[Godrick](https://github.com/madreher/Godrick) is a middleware designed to couple parallel codes togethers to form a graph. Its goal is to provide communication pipeline between components and handle the flow of data via different transport methods such as MPI communicators, sockets, files, etc.
This middleware is the backbone to connect a simulation code like Lammps to a steering engine or visualization frontend. The API to describe the application graph is written in Python while the runtime itself is written in C++.

Software Stack: C++, Python, MPI, ZeroMQ, [Conduit](https://llnl-conduit.readthedocs.io/en/latest/index.html), Cmake, [Catch2](https://github.com/catchorg/Catch2)

### LammpsInputBuilder (LIB)

[LammpsInputBuilder](https://github.com/madreher/LammpsInputBuilder) is a Python library designed to offer a high level API to define customizable and reusable simulation workflows for Lammps. This workflows can also be expressed in JSON, which will allow a future RestAPI to generate Lammps inputs.

Software Stack: Python, [ASE](https://wiki.fysik.dtu.dk/ase/), Pylint, pytest

### Radahn 

[Radahn](https://github.com/madreher/radahn) is built on top of Godrick and LIB. It offers a way to configure and launch a Lammps simulation with live visualization, plotting, and steering from the confort of your web browser and is compatible with Linux, OSX, and Windows. 
**WARNING**: 
- The frontend was my first attempt at learning frontend web development on the fly, and is intended to be a throw away project to start learning. If you are a frontend dev and have some suggestions/direction/resources, I would love to hear it!
- The frontend section of the project will be moved to its own repo in the second version and Radahn will focus solely on providing the simulation backend.

Software Stack: C++, Javascript, HTML, CSS, Flask, SocketIO, Docker, CMake 

## For Fun (and Learning) Projects

There is more to life that molecules dancing in a vaccum. Here are some for fun projects!

### Miquella 

[Miquella](https://github.com/madreher/miquella) is a playground to toy parallelisation methods like multithreading, gpu programming, etc. And what better way to test different parallelisation methods than to make shiny images???

Software stack: C++, ImGUI, [BS::thread_pool](https://github.com/bshoshany/thread-pool), [FastAPI](https://fastapi.tiangolo.com/), [cpr](https://github.com/libcpr/cpr)
PS: This project is currently on standby and needs documentation.




<!--
**madreher/madreher** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
