# Model and substance selection

These files are related to the selection of the thermodynamic model and substances.

## Substances 

- Oleic Acid (O-Acid)

  chosen to represent all the FFA

- Triolein  (OOO)

  chosen to represent all the TAG

- water (WTR)

- glycerol (GLYOH)

- Methanol (MEOH)

- Methyl Oleate (ME-O)

## Property methods available

| property method | Number |
| :-------------: | :----: |
|      NRTL       |  100   |
|    UNIF-DMD     |  200   |
|    UNIF-LBY     |  300   |
|     UNIF-LL     |  400   |
|     UNIFAC      |  500   |
|     UNIQUAC     |  600   |



## Terdiagram

**301** 

In Aspen: Properties/Analysis, the terdiagram-LL analysis are: 

| 001  | TAG + FFA + water      |
| ---- | ---------------------- |
| 002  | TAG + FFA + glycerol   |
| 003  | FFA + water + glycerol |
| 004  | FFA + methanol + water |
| 005  | FFA + ester + water    |



| Property method  | parameters |
| ---------------- | ---------- |
| temperature (oC) | 25         |
| pressure (bar)   | 1          |



Images generated are saved in the directory images with the following code (left column). The other columns represent the meaning:

| 101  | 100 - NRTL   | 001 - TAG + FFA + water |
| ---- | ------------ | ----------------------- |
| 201  | 200 - UNIFAC | 001 - TAG + FFA + water |

