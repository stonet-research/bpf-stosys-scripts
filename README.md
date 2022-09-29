# BPF-Stosys-scripts 

A collection of BPF scripts to break down performance aspects of various layers in storage systems software stack.

## Running

```bash
sudo bpftrace ./[script path]
```

To direct the BPF output containing the resulting maps, we can provide an output file in the bpftrace command.

```bash
sudo bpftrace ./[script path] -o data.dat
```
