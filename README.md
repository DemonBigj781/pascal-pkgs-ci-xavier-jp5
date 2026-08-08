# Pascal Packages CI - Xavier JP5

This repository is the older-GPU packaging laboratory for the Xavier stack. It carries compatibility shims, wheel-building patterns, and CI experiments for CUDA architectures that modern package releases often omit.

## Relationship to Triton

`pascal-pkgs-ci` is the aggressive compatibility side of the experiment: it targets older GPU packaging constraints. The neighboring Triton fork stays as close to its source baseline as practical. Flash Attention Legacy is the attention implementation connected to both lines of investigation.

## Role in the Xavier stack

- Tests packaging approaches for Volta/Pascal-era compatibility.
- Hosts controlled shims used to satisfy legacy CUDA dependency expectations.
- Produces evidence and build inputs, not automatic proof of runtime correctness.
- Must not replace a correct source fix with a broad fake-package workaround.

## Build discipline

All native compilation must use exactly one compiler worker.

## Upstream

Forked from `sasha0552/pascal-pkgs-ci`. This fork is organized specifically around the Xavier JetPack 5 toolchain.
