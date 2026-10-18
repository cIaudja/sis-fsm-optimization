# Optimised circuit (`src/`)

This folder contains the optimised `.blif` files. The top-level circuit is `FSMD.blif`; the other files are its components (FSM, datapath, registers, adders, multiplexers, comparators…).

## How to run the simulation

SIS runs inside Docker, using the `sis` image provided for the course.

### 1. Start Docker

Open Docker Desktop and wait until it says it is running.

### 2. Go to this folder

Open Terminal and move into the `src` folder of the project:

```bash
cd path/to/sis-fsm-optimization/src
```

### 3. Start the SIS container

```bash
docker run -it -v $PWD/.:/esercizio-sis -v $PWD/.bsis_history:/root/.bsis_history sis
```

This mounts the current folder inside the container at `/esercizio-sis` and saves the SIS command history, so you can reuse old commands with the ↑ key next time.

### 4. Open the mounted folder and start SIS

Inside the container:

```bash
cd /esercizio-sis
sis
```

The prompt changes to `sis>`.

### 5. Load the circuit

```
rl FSMD.blif
```

Optionally, print the circuit's equations:

```
write_eqn
```

### 6. Simulate

The circuit has 5 inputs, in this order: `IN OUT A B C`. Give one binary value (0 or 1) for each of them:

```
sim 1 0 1 0 0
```

SIS prints the value of the outputs (`SETTORE_NON_VALIDO SBARRA_IN SBARRA_OUT SECTOR_A SECTOR_B SECTOR_C`). Run `sim` again to simulate the next clock cycle; the circuit keeps its state between calls.

### 7. Quit

```
quit
```

then `exit` to leave the container.

## Simulating a single component

The same steps work for any other file in this folder, e.g. `rl FSM.blif` or `rl datapath.blif`. Check the `.inputs` line at the top of the file to see how many values `sim` needs.
