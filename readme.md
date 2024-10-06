NEURON mod files for the Ih current from the paper:
R. Bal and D. Oertel
Hyperpolarization-activated, mixed-cation current (Ih)
in octopus cells of the mammalian Cochlear Nucleus,
*J. Neurophysiol.* 84, 806-817 (2000)

- The current has been modeled as two independent HH-like gates 
with the same activation curve but different time constants (fast and slow).
The two gates are added to give the current as :
 ``` i_hcno = gbar_hcno*(v-eh)*(h1*frac+h2*(1-frac)) ```
 
- Running the kinetics.hoc simulation file will show 
the activation steady-state, the time constants, a simple simulation
using a somatic current injection of -1.3nA, and a family of curves
generated modeling the same protocol used in the experiments 
for Fig.6A of the paper. For Fig.6A the peak conductance has been adjusted
to give approximately the same currents shown in the paper.

- The time constants reported in the paper are shown
as markers of different colors. 
Time constants in the range not covered by the paper are an arbitrary
extension.
 
- By changing the frac and color parameters 
one can model the relative percentage of fast and slow gates.
 
## Under unix systems:
to compile the mod files use the command 
``` nrnivmodl ```
and run the simulation hoc file with the command 
``` nrngui kinetics.hoc ```

## Under Windows using NEURON 5.1:
to compile the mod files use the "mknrndll" command.
A double click on the simulation file
kinetics.hoc 
will open the simulation window.

\
Questions on how to use this model should be directed to
michele.migliore@pa.ibf.cnr.it

Changelog:
----------
2024-10: converted readme to markdown
