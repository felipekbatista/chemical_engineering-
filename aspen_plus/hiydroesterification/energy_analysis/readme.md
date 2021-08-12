# Energy Analysis 

The energy analysis of the hydroesterification process is in the file AEA_1. 

## AEA 1

Open the file, on the left pane click APLUS_Import. Several scenarios of optimization are in the file, all advances of Scenario 1. The scenarios versions are new heat exchangers. 

Each Scenario has a design optimization.

## Files

The files located in image directory are layout prints of

- no integration (HEN_101)
- integration (HEN_102)

They have a simple layout of the streams, a streams with pinch line and the network analysis parameters for each one. 

## Scenarios

### Scenario 1

- BaseCase 
- BaseCases 1N-X (New Heat Exchanger)
- A_Design7 --> The optimized version

### Scenario 1.1

- BaseCase 
- BaseCases 1N-X (New Heat Exchanger)

### Scenario 1.2

- BaseCase
- BaseCase 1N-X
- BaseCase 1N-X-1N-Y

### Scenario 1.3

- BaseCase
- BaseCase 1N-X
- BaseCase 1N-X-1N-Y
- BaseCase 1N-X-1N-Y-1N-Z

### Scenario 1.4

- BaseCase
- BaseCase 1N-X
- BaseCase 1N-X-1N-Y
- BaseCase 1N-X1-1N-X2-1N-X3-1N-X4

### Scenario 1.5

- A_Design7

### Scenario 1.6

- BaseCase
- BaseCase 1N-X
- BaseCase 1N-X-1N-Y
- A_Design6
- **A_Design8**

The best results found was **Scenario 1.6 A_Design8**, with the following Descriptions

**Network Cost Indexes**

| Parameter           | Index     |
| ------------------- | --------- |
| Heating (cost/s)    | 0,01669   |
| Cooling (cost/s)    | -0,006569 |
| Operating (cost/s)  | 0,01012   |
| Capital (cost/s)    | 235.000   |
| Total Cost (cost/s) | 0,01208   |

**Network Performance**

| Parameter        | Value      |
| ---------------- | ---------- |
| Heating (kJ/h)   | 24.030.000 |
| Cooling (kJ/h)   | 2.012.000  |
| Number of Units  | 12         |
| Number of shells | 14         |
| Total Area (m2)  | 318,5      |













#
