# Ternary Diagrams

These files are related to the selection of substances and their qualitative behavior regarding phase split. 

The classes of substances used are showed here and also the proposed ternary diagrams for analysis.

## Substances

The biodiesel process uses the following classes of substances:

- Triacylglycerol (TAG)
  - Triolein OOO
- free fatty acid (FFA)
  - Oleic Acid O-Acid
- water
  - wtr
- alcohol (methanol)
  - MeOH
- ester (biodiesel)
  - Methyl-Oleate Me-O
- glycerol
  - Gly-OH

---

## Property methods available

these are the methods that were used for testing the Liquid-Liquid Equilibria. Right column is the Method ID

| property method | Number |
| :-------------: | :----: |
|      NRTL       |  100   |
|    UNIF-DMD     |  200   |
|    UNIF-LBY     |  300   |
|     UNIF-LL     |  400   |
|     UNIFAC      |  500   |
|     UNIQUAC     |  600   |





# Ternary diagrams

The ternary diagrams are used for phase split analysis. The following components are tested with different methods.

| Composition            | number |
| ---------------------- | ------ |
| TAG + FFA + water      | 001    |
| TAG + FFA + GLYCEROL   | 002    |
| FFA + water + glycerol | 003    |
| FFA + Methanol + water | 004    |
| FFA + Ester + water    | 005    |

 

## conditions



| Parameter        | values |
| ---------------- | ------ |
| temperature (oC) | 25     |
| pressure (bar)   | 1      |

## How to read the number

The generated images are saved in image directory. 

Images generated are saved in the directory images with the following code (left column). The other columns represent the meaning:

| img ID | method       | components              |
| ------ | ------------ | ----------------------- |
| 101    | 100 - NRTL   | 001 - TAG + FFA + water |
| 201    | 200 - UNIFAC | 001 - TAG + FFA + water |

