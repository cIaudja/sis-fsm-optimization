# Non-optimised version (`legacy/`)

This folder contains the first, non-optimised version of the circuit:

- `FSMDnonottimizzata.blif` – full circuit (FSM + datapath)
- `FSMnonottimizzata.blif` – controller (FSM)
- `datapathnonottimizzato.blif` – datapath

It is kept only for reference, to compare it with the optimised version in [`src/`](../src).

## Note on running it

These files load their sub-circuits by their original names (`.search FSM.blif`, `.search datapath.blif`, `.search mux4.blif`…), which are not in this folder, so `rl FSMDnonottimizzata.blif` does not work from here as it is. To run the optimised circuit, follow [`src/README.md`](../src/README.md).
