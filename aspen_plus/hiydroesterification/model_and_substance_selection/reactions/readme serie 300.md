# Series 300

reaction studies

## Reactions

### Hydrolysis

Using a Gibbs reactor, the objective is to hydrolyse all the TAG with water to form FFA via an equilibrium.

**301**

Reactor feed is an equimolar (10 kmol/h of each) mixture of TAG and Water. The reached equilibria indicates a complete conversion of Water into FFA. All TAG was not converted due to the stoichiometry.

````
TAG + 3 H2O --> 3 FFA + GlyOH
````



**302**

Sensitivity analysis of the gibbs reactor for search of the best molar output.

​	Parameters that will be analyzes

- Feed Molar Ratio (water/TAG)			

- Temperature

- Pressure

  Analyzed parameter

- TAG output

#### Sensitivity 1

| parameter                      | value (kmol/h) |
| ------------------------------ | -------------- |
| Molar feed ratio (TAG / water) | 0.5 - 20       |
| Water feed (constant)          | 30             |

This sensitivity shows that the conversion fully happens and is equals to the molar ammount of available water. 

The minimum required water feed is the molar feed ratio.

file 

````
image S1_OOO_FFA
````

#### Sensitivity 2

| parameter                      | value       |
| ------------------------------ | ----------- |
| Temperature                    | 50 - 250 ºC |
| molar feed ratio (TAG / water) | 1 / 3       |

This sensitivity shows at first glance that the conversion decreases with temperature raise, but a closer look at the Y-axis scale and it is possible to see that the change happens at the 3rd decimal place, so, for this situation, temperature is a non influent parameter

#### Sensitivity 3

| parameter                      | Value       |
| ------------------------------ | ----------- |
| Pressure                       | 1 - 10  bar |
| molar feed ratio (TAG / water) | 1 / 3       |
| Temperature                    | 200 ºC      |

this sensitivity shows that pressure does not influenciate in the conversion.



#### Image

check Image folders for the sensitivity analysis regarding the equilibrium reactor

```` 
S1_OOO_FFA
S2_TEMP_FFA
S3_PRESSURE_FFA
````



**303 **

In this simulation, I found a paper[^1] in which a kinectic reaction (Arrhenius) is described together with optimum reaction parameters. 

The kinetics are in the table bellow

| Variable               | value                           |
| ---------------------- | ------------------------------- |
| pre-exponential factor | 156.9 (direct) / 2,42 (reverse) |
| activation energy      | -40,421,9 (kj/kmol)             |

This simulation is made to find suitable parameters for the operation:

- molar feed ratio (TAG / Water)
- reactor length (diameter = 0.1 m)
- temperature 



**sensitivity 4**

what is the best molar water TAG feed ratio?

For finding the most suited answer to that question, a sensitivity analysis is done. 

constant parameters

| parameter        | value    |
| ---------------- | -------- |
| Temperature      | 280 oC   |
| TAG              | 1 kmol/h |
| Pressure         | 56 bar   |
| Reactor Length   | 50 m     |
| reactor diameter | 0.1 m    |

| vary       | Define      | tabulate                |
| ---------- | ----------- | ----------------------- |
| water flow | O-Acid flow | (OACID - 3*OOO) / OACID |
|            | OOO flow    |                         |

The sensitivity analysis generated the plot 

````python
S4_WATER_OOO_CONV
````

the graph shows that for 0.95 conversion of the TAG, a water moleflow of 6.5 kmol/h is needed @ 280 oC (for T = 250 oC, the moleflow is 8.5 kmol/h).



**sensitivity 5**

This sensitivity analyzes the influence of temperature in the reaction conversion. For sake of comparison, the molarfeed ratio is 3 : 1 for water, a stoichiometric one

| parameter        | value    |
| ---------------- | -------- |
| Water            | 3 kmol/h |
| TAG              | 1 kmol/h |
| Pressure         | 56 bar   |
| Reactor Length   | 50 m     |
| reactor diameter | 0.1 m    |

| vary                | Define      | tabulate                |
| ------------------- | ----------- | ----------------------- |
| reactor temperature | O-Acid flow | (OACID - 3*OOO) / OACID |
|                     | OOO flow    |                         |

The sensitivity analysis generated the plot 

````
S5_TEMPERATURE_OOO_CONV
````

This plot indicates two things

- bellow 200 the conversion rate increases very low
- above 200 the conversion rate increases sharply
- at 260 oC the conversion rate is 0.5
- 0.95 conversion is above  360 oC

**sensitivity 6 **

This sensitivity analyzes the influence of temperature in the reaction conversion. For sake of comparison, the molarfeed ratio is 6 : 1 for water, a stoichiometric one

| parameter        | value    |
| ---------------- | -------- |
| Water            | 6 kmol/h |
| TAG              | 1 kmol/h |
| Pressure         | 56 bar   |
| Reactor Length   | 50 m     |
| reactor diameter | 0.1 m    |

| vary                | Define      | tabulate                |
| ------------------- | ----------- | ----------------------- |
| reactor temperature | O-Acid flow | (OACID - 3*OOO) / OACID |
|                     | OOO flow    |                         |

The sensitivity analysis generated the plot 

````
S6_TEMPERATURE_OOO_CONV
````

This plot indicates two things

- bellow 120  the conversion rate increases very low
- above 120 the conversion rate increases sharply
- near 185oC the conversion rate is 0.5
- 0.95 conversion is above  290 oC



**sensitivity 7 **

This sensitivity analyzes the influence of temperature in the reaction conversion. For sake of comparison, the molarfeed ratio is 7 : 1 for water, a stoichiometric one

| parameter        | value    |
| ---------------- | -------- |
| Water            | 7 kmol/h |
| TAG              | 1 kmol/h |
| Pressure         | 56 bar   |
| Reactor Length   | 50 m     |
| reactor diameter | 0.1 m    |

| vary                | Define      | tabulate                |
| ------------------- | ----------- | ----------------------- |
| reactor temperature | O-Acid flow | (OACID - 3*OOO) / OACID |
|                     | OOO flow    |                         |

The sensitivity analysis generated the plot 

````
S7_TEMPERATURE_OOO_CONV
````

This plot indicates two things

- 170 oC the conversion rate is 0.5
- 0.95 conversion is above  270 oC



#### Conclusion

The sensitivities show that the molarfeed ratio (an thus concentration) is a very relevant parameter for reaching significant conversions, together with temperature (above 200 oC). and the reactor operated at constant temperature.

The 0.95 conversion was chosen for this evaluation and it is shown that raising the ratio reduces the temperature in which 0.95 conversion is reached, though an equilibrium is reached near a 0.98 conversion for temperature ranges near 300  oC.



## Esterification





# References

[^1]: Biodiesel production by hydroesterification: simulation studies. By DAG Aranda and GD Machado, 2016.

