# Hambrick et al., in prep.
To explore the effects of temperature on the _M. aeruginosa_ host and Ma-LMM01 viral interaction two models were developed including a lytic population model and a resistant subpopulation model (Hambrick et al., in prep). All code for both of these models along with the corresponding data can be found in this repository.

**Lytic Population Model**
----------------------------
The lytic population model was used to approximate the host-phage interaction with an underlying assumption that all hosts are susceptible to the phage.

A susceptible algal host population is defined as:

$$\frac{dA_S}{dt} = μA_S-φ_S A_S V + lamb*I*(1-Pr_S) $$

where $μ$ is the algal host growth rate (day-1), $A_S$ is the susceptible algal host (cells mL-1), $φ_S$ is the viral infection rate of the susceptible algal host (mL virus-1 day-1), and $V$ is the abundance of free phage (virus mL-1). 

$$\frac{dI_S}{dt}=φ_S A_S V- λ_S I_S$$

$$\frac{dV}{dt}=β_S λ_S I_S  - φ_S A_S V$$


**Resistant Subpopulation Model**
----------------------------------
The resistant subpopulation model assumed the presence of a small initial subpopulation of resistant hosts to a given phage within a culture dominated by susceptible hosts. 

$$\frac{dA_S}{dt} = μA_S-φ_S A_S V$$

$$\frac{dA_R}{dt}= μA_R- φ_R A_R V$$

$$\frac{dI_S}{dt}=φ_S A_S V- λ_S I_S$$

$$\frac{dI_R}{dt}=φ_R A_R V- λ_R I_R$$

$$\frac{dV}{dt}=β_S λ_S I_S+ β_R λ_R I_R-(φ_S A_S+φ_R A_R)V$$

**Installation**
--------------------------------------------------------------------
NIES298infection can be installed by cloning the repo and installing:

cd /dir/you/want

git clone https://github.com/kennedihambrick/NIES298infection.git

cd NIES298infection/

pip install .
