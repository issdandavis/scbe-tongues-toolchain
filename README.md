# SCBE Sacred Tongues Toolchain

> Assembler + virtual machine for the Sacred Tongue programming language.

Compile `.sts` source files to a bytecode format, then execute them on the stvm.
Part of the SCBE-AETHERMOORE ecosystem — extracted from the monolith into its own
repo so the toolchain has an independent release cadence.

## Directory layout

- `stasm/` — the Sacred Tongue assembler (`.sts` → `.bin` / JSON)
- `stvm/` — the Sacred Tongue virtual machine (executes compiled bytecode)

## Quick start

```bash
# Assemble a source file
python -m stasm.assembler examples/hello_world.sts /tmp/hello.bin

# Run it
python -m stvm.vm /tmp/hello.bin
```

## Relationship to other SCBE repos

- **[SCBE-AETHERMOORE](https://github.com/issdandavis/SCBE-AETHERMOORE)** — the full governance framework
- **[six-tongues-geoseal](https://github.com/issdandavis/six-tongues-geoseal)** — bijective tokenizer + sealed envelope CLI
- **[scbe-agents](https://github.com/issdandavis/scbe-agents)** — HYDRA swarm runtime that executes Sacred Tongue programs

## License

MIT
