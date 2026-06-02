# .github
Protein - Amyloid Fibrils
Protein - Amyloid Fibrils is a computational protein design workspace focused on exploring binder design workflows for amyloid fibril-associated protein targets.

The current project centers on adapting and running BindCraft, a de novo binder design pipeline that combines AlphaFold2-based design, ProteinMPNN sequence generation, and PyRosetta-based filtering. Our near-term goal is to establish a reproducible workflow for generating, filtering, and evaluating candidate binders against selected amyloid fibril target regions.

Current Focus
We are currently building the compute and workflow foundation needed to run BindCraft reliably on high-performance GPU resources.

This includes:

setting up command-line and VS Code-based access to remote compute environments
learning how to run Python and Bash scripts on shared servers
preparing SLURM-compatible job scripts for GPU-based binder design
testing BindCraft on tutorial/sample targets before moving to amyloid fibril targets
identifying target windows and hotspot regions for initial binder generation
collecting early candidate binders to understand the design, filtering, and validation process
Active Repository
BindCraftRepo
This repository contains the working BindCraft codebase used for our early setup and binder design experiments.

Current work in this repo includes:

confirming BindCraft can run on available compute resources
moving from local or low-memory GPU testing to stronger institutional compute
preparing scripts for server-side execution
testing initial binder generation workflows
planning first design runs against selected protein regions
Research Direction
The first phase is intentionally practical: before interpreting designed binders biologically, we need to confirm that the computational pipeline runs correctly and reproducibly.

Our early design plan is to:

Run BindCraft successfully on a remote GPU server.
Generate a small first set of candidate binders against selected target regions.
Use the first outputs to learn the validation and filtering workflow.
Refine target hotspot selection based on protein structure and relevant literature.
Run larger design iterations with improved target definitions and filtering criteria.
Initial target regions under consideration include windows around amino acid ranges 120-140 and 205-250. These early runs are exploratory and are meant to validate the pipeline before prioritizing stronger candidates.

Workflow Overview


Target protein structure
Select target region orhotspot
Configure BindCraft targetJSON
Submit GPU job on remoteserver
Generate candidatebinders
Filter computationaloutputs
Review top candidates
Plan validation or nextdesign iteration
Compute Notes
Early testing showed that small tutorial runs can begin on lower-memory GPUs, but meaningful BindCraft runs require stronger compute. The current setup effort is therefore focused on running jobs through institutional servers rather than relying on local hardware.

Key infrastructure goals:

server access through terminal and VS Code
reproducible Bash/SLURM scripts
organized input/output directories
clear records of settings files, target regions, and accepted designs
documentation that lets future lab members rerun the same workflow
Near-Term Roadmap
Confirm Python and Bash execution on the target server
Submit a minimal test job through the server scheduler
Run BindCraft tutorial/sample target end to end
Create amyloid fibril target configuration files
Run first exploratory binder generation jobs
Review early accepted binders and failure modes
Refine hotspot selection using structural and literature context
Document the working pipeline for future contributors
Project Values
This organization is meant to keep the work:

reproducible
readable for new contributors
honest about experimental stage and uncertainty
organized around clear design iterations
useful as a record of computational setup, not just final results
Contributors
This work is being developed as a research and training project under the Protein - Amyloid Fibrils organization.

Internship progress notes from the current setup phase informed this README, especially the transition from tutorial BindCraft runs to remote server execution and first amyloid-targeted design planning.

Disclaimer
This repository is for computational research and workflow development. Candidate binders generated through this process require further computational review and experimental validation before any biological interpretation or application.
