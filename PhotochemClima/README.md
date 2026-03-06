
# cod-accra: Photochem.clima

This folder reproduces all `Photochem.clima` calculations for the cod-accra model inter-comparison. To run this code, first use the `conda` package manager to create a new environment:

```sh
conda create -n codaccra -c conda-forge python=3.13 photochem=0.8.3 matplotlib
conda activate codaccra
```

Next, run the main function:

```sh
python main.py
```

After a ~1 minute of runtime, the results will appear in the `results/` folder as .txt files.

## Summary of tests

| Test   | Description                   | Opacities | Bolometric flux | Star       | Relative humidity | Surface albedo | Surface emissivity |
| ------ | ----------------------------- | --------- | --------------- | ---------- | ----------------- | -------------- | ------------------ |
| I-1a   | Modern Earth (inverse)        | Native    | 1360 W/m^2      | Sun        | N/A               | 0.32           | 0.9                |
| I-1b   | Modern Earth (inverse)        | Common    | 1360 W/m^2      | Sun        | N/A               | 0.32           | 0.9                |
| II-1   | Modern Earth (RCE)            | Native    | 1360 W/m^2      | Sun        | 1.0               | 0.32           | 0.9                |
| III-7a | TRAPPIST-1 g (`P_CO2=5 bar`)  | Native    | 343 W/m^2       | TRAPPIST-1 | 1.0               | 0.2            | 1.0                |
| III-7b | TRAPPIST-1 g (`P_CO2=10 bar`) | Native    | 343 W/m^2       | TRAPPIST-1 | 1.0               | 0.2            | 1.0                |
