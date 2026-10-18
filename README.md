# SIS FSM optimisation

Assignment for the Computer Architecture course at the University of Verona (2022–23). It is a car park access controller (entry and exit barriers, three sectors A–C) built as a digital circuit: a controller (FSM) and a datapath combined into an FSMD, described and simulated in SIS. Most of the work went into optimising the circuit.

## Structure

- `src/` – the optimised `.blif` files (top-level circuit: `FSMD.blif`)
- `Relazione.pdf` – full report (in Italian): specification, how the FSM works, design and optimisation choices

## How to run the simulation

Step-by-step instructions are in [`src/README.md`](src/README.md).
