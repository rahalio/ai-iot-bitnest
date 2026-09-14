# BitNest — User stories

**Product:** [PRODUCT.md](./PRODUCT.md)


### Embedded ML engineer

- As an ML engineer, I want to pack a zoo model to 8-bit with local regions and see top-1 and top-5 deltas, so I can decide if the build is shippable.
- As an ML engineer, I want to try 2-bit with local regions and compare accuracy to global quantization, so I can justify the extra packaging complexity.
- As an ML engineer, I want LUT substitution toggles per layer with latency reports, so I know which layers benefit on the target SoC.

### Firmware engineer

- As a firmware engineer, I want a single package artifact with runtime bindings for the target board, so integration is not a research project.
- As a firmware engineer, I want OTA rollback when latency SLAs breach after a bit-width change, so field devices recover without a factory visit.

### Hardware architect

- As a hardware architect, I want transistor and memory estimates for 4/2/1-bit builds, so I can avoid commissioning an FPGA when software packing is enough.

### QA / release manager

- As a release manager, I want promotion blocked when eval delta exceeds the SKU budget, so low-bit builds cannot silently ship.
- As a QA lead, I want a frozen eval set bound to each package, so vendors cannot move the goalposts after the fact.

### Privacy officer

- As a privacy officer, I want calibration images deleted after scales are sealed, so customer sites are not retained as training corpora.
- As a privacy officer, I want on-device-only mode attested in the package manifest, so cloud offload cannot be re-enabled by a silent flag.
