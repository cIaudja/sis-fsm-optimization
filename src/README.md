# Optimised circuit (`src/`)

This folder contains the optimised `.blif` files. The top-level circuit is `FSMD.blif`.

## Simulating with SIS

The commands below assume a local Docker image called `sis` (the one provided for the course).

1. Start Docker, then run the container from this folder:

   ```bash
   docker run -it -v $PWD/.:/esercizio-sis -v $PWD/.bsis_history:/root/.bsis_history sis
   ```

   This mounts the current folder at `/esercizio-sis` and keeps the SIS command history between sessions.

2. Inside the container, go to the mounted folder and start SIS:

   ```bash
   cd /esercizio-sis
   sis
   ```

3. Load the circuit (and, if you want, print its equations):

   ```
   rl FSMD.blif
   write_eqn
   ```

4. Simulate it by giving one binary value per input, for example:

   ```
   sim 1 0 0 1 1 0
   ```
