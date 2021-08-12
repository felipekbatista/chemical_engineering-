# Solvay process - logs

This file has the logs of the executed steps and changes. 

Made for tracking what I have done and obtained results



## Model and Components

The thermodynamic model used for this situation was ELECNRTL due to the presence of electrolites.

- H2O
- NaCl
- CO2
- NH3
- NaHCO3
- NH4Cl
- NaOH
- HCl
- Na2CO3

For handling with solids, a solid PSD mesh was created and stream class CONV was updated with MIXED and CIPSD

### Chemistry

**equilibrium reactions**

> described in Properties/Chemistry/C-1

- HCL  <-->  CL-  +  H+

- NH3  +  H2O  <-->  OH-  +  NH4+

- HCO3-  <-->  CO3--  +  H+

- H2O  +  CO2  <-->  HCO3-  +  H+

- H2O  <-->  OH-  +  H+

- NH4CL(S)  <-->  CL-  +  NH4+

- NAHCO3-S  <-->  HCO3-  +  NA+

- NAOH(S)  <-->  OH-  +  NA+

- NA2CO3-S  <-->  CO3--  +  2 NA+

- NACL(S)  <-->  CL-  +  NA+

- NAHCO3  -->  HCO3-  +  NA+

- NH4CL  -->  CL-  +  NH4+

- NAOH  -->  OH-  +  NA+

- NACL  -->  CL-  +  NA+

  

> removal of all sodium carbonates hydrates (precipitates) for chemistry simplification
>
> solid PSD was created and the stream class CONV was updated with CIPSD and MIXED 





**101**

Water and NaCl-S dissolution  test
no dissolution occured. 

Water and NaCl (CONV) dissolution  test
NaCl was already dissolved and in contact with water nothing happened, though there was an increas of 2oC in temperature 

Water and NaCl(s)-conv dissolution test 
dissolution occured and temperature gone down 3 oC, as expected with the dissolution of NaCl.

As I have observed here, for dissolution to occur, it needs to be used as a solid from CONV stream, not a CIPSD stream

**102**

Water and CO2 solubility test
The dissolution showed an increase in temperature and a sligthly production of HCO3 - (magnitude of 10^(-5))



Water and NH3 solubility test
The dissolution presented an increase in temperature and a slight production of NH4+ ( magnitude of 10^-4)

**103**

Water and CO2 and HCL solubility test 
The HCl does not dissociates in water due to the lack of dissociation equation

Used a H+ and CL- ions directly in the stream
Got problem with the stream flash due to the fact that HCL is not present in the vapor phase
There was no reaction happenning 

Added the dissociation of HCl in properties/chemistry/C-1

Problem with dissociation  enthalpy, missing params 
Temperature dropped to -63oC
No reaction happened

Used NaOH in the stream replacing HCL



**104**

Added the HCL equilibrium for the simulation. 
Due to the lack of available data from databank, I've copied  the equilibrium parameters from the NaOH(s) dissociation values. 

All the parameters seems to have been specified and nothing is missing (at least no alarm was triggered)

**105**

Runned the sim in the mixer M-103 with CO2 and NAOH.
Produced a high wuantity of HCO3 and also precipitated the NaHCO3
Im happy for dis!  =D



**106**

This step is to collect info in the equilibrium of ammonium ion with water and HCL or NaOH Uusing Mixer M-102
Used 0.5 kmol of NaOH and the output was 2.6e(-7) kmol/h of NH4+ and the temperature was 99oC
Used an exchanger toreduce the temperature to 25oC and the quantity of NH4+ did change in one order of magnitude
Temperature reduction is good for production of NH4+  



**107**
Used 0.5 kmol of HCL and the output was  0.1274 kmol/h of NH4+, adiabatic.
When reduced the temperature, the NH4+ concentration was raised to 0.5kmol/h  



**108 - process start**

Create the  brine mixer M-104

Used 10 kmol of NaCl and 100 kmol of water

run worked flawless'



**109**

Add absorption colum T-101

check the colum for comments



**110**
reaction column T-102
check column comments  

the column did not converge even though I tried somethings on it, so I decided to check the reactions with streams in the mixers, starting with M-105
deleted the column T-102 



**111 **

This run is to  produce NH4+ ions, HCO3- via streams mixer only.

these mixers produced NH4+ and Na+ ions. 
M-105 check the mixer for comments.
M-106 check the mixer for comments.
M-107 check the mixer for comments.

M-106 has enthalpy inbalance. 
is producing  NaOH(s). 

M-107 produced the NH4+ and dissolving the NaOH that was previously produced.
it does not shoots any inbalance warning, though the temperature has risen to 11oC.



*observations*

> HCl dissolution causes problems regarding energy balance. It reduces water temperature 
>
> 



These mixers produce CO2 dissolved in water. 

Used NaOH(s) to raise HCO3- content.

M-108 check the mixer for comments.
M-109 check the mixer for comments.



HCO3-  and NaHCO3-(s) were prodouced in stream HCO3-1.

Needed to separate NaHCO3(s) from HCO3-1, so used the SEP-1.



M-110 mix ammoniacal brine and HCO3 to produce NaHCO3

The outlet stream did not resulted in NaHCO3(s) production, but, the following stream, 10, after a cooldown to 25 oC did show NaHCO3(s) production. This shows that temperature control is an important factor to sodium bicarbonate production. 



| kmol NaHCO3 / h | kmol total /  h |
| :-------------: | :-------------: |
|      0.73       |       234       |



**112**

Absorption column is not converging in mass balance.

The absorption column is at some extent working, providing absorbed ammonia to outlet bottom products, though it is in mass inbalance.

The HCL presented problems with enthalpy when mixed with water and my guess is that it also responsible for the absorption column problem

filesave: sodium_bicarbonate-105



**113**

Since HCL presented problem with enthalpy and T-101 had mass balance problems (also HCL was leaving in TOP), I decided to check the HCL component. Since this is an electrolyte model, HCL has a dissociation equation. I did check it and it was an equilibrium equiation, not a dissociation, so I deleted the equilibrium and replaced it for a dissociation equation. 

- T-101 is in mass balance and NH4+ ions are present in stoichiometricall relation with NH4+
- HCL streams are now non-volatile, so it throws a problem about it



**114**

Add T-102, the solvay tower with 20 stages

produced NaHCO3-s   =D 

file 

- _107











