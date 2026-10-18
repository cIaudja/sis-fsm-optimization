# SIS FSM optimisation

Assignment for the Computer Architecture course at the University of Verona (2022–23). It is a digital circuit made of a controller (FSM) and a datapath, combined into an FSMD, described and simulated in SIS. Most of the work went into optimising the circuit.

## Structure

- `src/` – the optimised `.blif` files (top-level circuit: `FSMD.blif`)
- `legacy/` – an earlier, non-optimised version, kept for comparison
- `Relazione.pdf` – full report (in Italian): specification, how the FSM works, design and optimisation choices

## Running the simulation

SIS runs inside a Docker container. Step-by-step instructions are in [`src/README.md`](src/README.md).
