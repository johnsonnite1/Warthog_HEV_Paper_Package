WARTHOG HEV MANUSCRIPT AND REPRODUCIBILITY PACKAGE
Prepared for Johnson Abiola

MAIN DOCUMENT
Warthog_HEV_Manuscript.docx is the editable Word manuscript. It contains
an abstract, introduction, recent related work, physical model, full hybrid
controller equations, analytical properties, tuning method, experimental
protocol, results/discussion, limitations, conclusion and references.
The comparison is PI, H-infinity, standalone MFAC and Warthog only.
The 12 references are dated 2021--2026, including two verified publications
by Johnson Abiola. The achieved H-infinity gamma is reported honestly.

CONTENTS
13 figure assets: the HEV system diagram; actual Simulink plant image;
closed-loop diagram; flowchart; tuning; test inputs; tracking/torque plots;
metric comparisons; adaptation; physical signals; actual vendor PI image;
and a current wrapper schematic. Seven manuscript tables are included.
The DOCX includes editable native Word equations and an online pseudocode.
Figures are also supplied separately as PNG/PDF where generated; the two
original Simulink images retain their original raster form.

DATASET
The manuscript reports only complete matched 150-second cases for the four
research controllers: payload/grade and noisy/lagged seeds 8041 and 8042.
There are 12 CSV traces. Noise means/std are descriptive for TWO seeds.
No nominal-condition or all-scenario performance claim is made. The
original model's continuous controller is outside the defined sampled
research-controller comparison. Original planning/provenance is retained
separately so the manuscript subset can be audited.

BEFORE SUBMISSION
1. Confirm final author list, affiliations, corresponding email, funding,
   competing interests and the chosen journal's assistance-disclosure policy.
   These were not invented in the manuscript.
2. Use the selected journal's official template. This document is a general
   single-column manuscript, not an assertion of journal-template compliance.
3. Refresh the FINAL wrapper/supervisor Simulink exports if the journal needs
   those exact native screenshots. The genuine plant and vendor PI exports
   supplied here are distinguished from source-derived schematics. Historical
   wrapper images have not been misrepresented as current final exports.

The helper code/export_final_simulink_diagrams.m exports three actual model
views WITHOUT running or tuning a simulation. Copy it into the existing
MATLAB experiment root and run:

 export_final_simulink_diagrams(fullfile(pwd,'runs','ONE_RUN_20261102_172501_986'));

The helper requires the original saved run/model files on your machine.
Its syntax was checked; it has not been executed in the preparation
workspace because MATLAB is unavailable here. Replace Figure A2 or add an
implementation figure after inspecting those native exports.

REPRODUCIBILITY
The MATLAB kernel and wrapper are source snapshots from the executed run;
the original experiment package and MathWorks plant are still required for
new physical simulations. The saved MAT checkpoint requires MATLAB and
its original control-system objects. JSON provides plain numeric values.
Python figure regeneration uses numpy, pandas, scipy and matplotlib:

 python code/rebuild_figures.py
 python code/rebuild_HEV_system_figure.py

Word regeneration additionally needs python-docx and lxml:

 python code/rebuild_manuscript.py

The equations.docx file inside code is an editable equation-source template
used by the document builder. It is not a second manuscript. The Markdown
is a text/source companion; use the DOCX as the formatted manuscript.
The provenance folder preserves the initial protocol and status; its
all-comparator performance target was NOT met and is not claimed here.
Publication, global nonlinear stability and hardware performance are not
inferred from the manuscript presentation.
