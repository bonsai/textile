# bonsai/textile

Textile design as machine-readable data.

## Purpose

`textile` is the shared intermediate representation (IR) for textile manufacturing. It separates **design intent** from machine-specific output.

```text
image / drawing
      ↓
textile IR
      ├── amimono → knit machine formats
      └── shishu  → embroidery / patch machine formats
```

## Scope

- image-to-textile design conversion
- geometry, color, material and production metadata
- machine-independent textile IR
- adapters/exporters for `bonsai/amimono` and `bonsai/shishu`
- reproducible manufacturing data

## Repository structure

```text
schema/       shared JSON Schemas
examples/     small reference designs
spec/         semantic definitions
converters/   image/vector → textile IR
adapters/     domain adapters
exporters/    machine-specific output
```

## Design principle

Do not make PNG/SVG or a machine format the source of truth. Preserve the semantic design first; generate machine instructions afterward.

## Status

Skeleton / initial ontology.

## Related

- `bonsai/amimono` — knitting design and machine output
- `bonsai/shishu` — embroidery, patches and sewing-machine output
