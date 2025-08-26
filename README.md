# Hambrick et al., in prep.
To explore the effects of temperature on the _M. aeruginosa_ host and Ma-LMM01 viral interaction two models were developed including a lytic population model and a resistant subpopulation model (Hambrick et al., in prep). All code for both of these models along with the corresponding data can be found in this repository.

**Lytic Population Model**
----------------------------
The lytic population model was used to approximate the host-phage interaction with an underlying assumption that all hosts are susceptible to the phage.

A susceptible host population mass balance is defined as the difference between host growth, infection, and recovery:

$$\frac{dA_S}{dt} = μA_S-φ_S A_S V + λ_S I_S (1-P_{R,S})$$

where μ is the algal host growth rate (day-1), A_S is the susceptible algal host (cells mL-1), 〖 φ〗_S is the viral infection rate of the susceptible algal host (mL virus-1 day-1), and V is the abundance of free phage (virus mL-1). Lysis of an infected susceptible host population IS (cells mL-1) proceeds with lysis rate λ_S (day-1) and the proportion of lysis events that fail leading to recovery is represented by 〖(1- P〗_(R,S)). . 

A mass balance of infected host cells is defined as:

$$\frac{dI_S}{dt}=φ_S A_S V- λ_S I_S$$

where λ_S  is the infected susceptible host lysis rate ($$day^-1$$) and IS is the infected susceptible algal host (cells mL-1). 

Lastly, a population of free virus can be described as:

$$\frac{dV}{dt}=β_S λ_S I_S P_{R,S} - φ_S A_S V$$

where〖 β〗_Sis the burst size of phage from the infected susceptible host (virus cell-1). 

**Resistant Subpopulation Model**
----------------------------------
The resistant subpopulation model assumed the presence of a small initial subpopulation of resistant hosts to a given phage within a culture dominated by susceptible hosts. 

A resistant host population mass balance can be defined as the difference between host growth, infection, and recovery:  

$$\frac{dA_S}{dt} = μA_S-φ_S A_S V + λ_S I_S (1-P_{R,S})$$

$$\frac{dA_R}{dt}= μA_R- φ_R A_R V + λ_R I_R (1-P_{R,R})$$

where A_R is the resistant algal host (cells mL-1) and φ_R is the viral infection rate of the resistant algal host (mL virus-1 day-1). Lysis of an infected resistant algal host (cells mL-1) proceeds with lysis rate λ_R (day-1) and the proportion of lysis events leading to host recovery is (1-P_(R,R)).

A mass balance population of infected host cells derived from the resistant host population is defined as:

$$\frac{dI_S}{dt}=φ_S A_S V- λ_S I_S$$

$$\frac{dI_R}{dt}=φ_R A_R V- λ_R I_R$$

where λ_R is the infected resistant host lysis rate (day-1) and IR is the infected resistant algal host (cells mL-1). 

Finally, a mass balance of free virus can be described as:

$$\frac{dV}{dt}=β_S λ_S I_S P_{R,S}+ β_R λ_R I_R P_{R,R}-(φ_S A_S+φ_R A_R)V$$

where〖 β〗_(R )is the phage burst size from the infected resistant host (virus cell-1). 

**Installation**
--------------------------------------------------------------------
NIES298infection can be installed by cloning the repo and installing:

cd /dir/you/want

git clone https://github.com/kennedihambrick/NIES298infection.git

cd NIES298infection/

pip install .
