# PHYS305 Homework Set #5

Welcome to the repository for **Homework Set #5** in PHYS305.
This homework set is worth **10 points** and is designed to test your
understanding of topics that we've covered.
The submission cutoff time is at **Tuesday Apr 17th, 11:59pm** Arizona
time.
Please use [this link](https://classroom.github.com/a/______) to
accept it from GitHub Classroom.


## Structure and Grading

This homework set consists of **five assignments**, each contributing
equally to your overall grade.
The grading breakdown is as follows:

1. **Automated Evaluation (50%)**:
   * Each assignment will be graded using `pytest`, an automated
     testing framework.
   * The correctness of your solutions accounts for 1 point per
     assignment (5 points in total).
   * You can run `pytest` in GitHub Codespaces or your local
     development environment to verify your solutions before
     submission.

2. **Documentation and Coding Practices (50%)**:
   * The remaining 1 point per assignment (5 points total) will be
     based on documentation and coding practices.
   * Clear and concise **documentation** of your code, including
     meaningful comments.
   * Adherence to good **coding practices**, such as proper variable
     naming, modular design, and code readability.

By following the interface and prototypes provided in each assignment
template, you can ensure compatibility with the autograding system and
maximize your score.


## Assignments

To simplify debugging and to help you visualize your progress, a
Jupyter notebook is provided at `demo/vis.ipynb`.
This notebook demonstrates how the functions developed for each
assignment interact and shows sample visualizations. Use the notebook
alongside `pytest` to validate your code and to better understand the
behavior of your implementations.


### **Assignment 1**: Run Tutorial 3.2 from the GW ODW 2024 #7 (2 points)

* **Objective**:
  Add [Tutorial 3.2](https://github.com/gw-odw/odw-2024/blob/main/Tutorials/Day_3/Tuto_3.2_Parameter_estimation_for_compact_object_mergers.ipynb)
  from Gravitational Wave Open Data Workshop #7 to this repository,
  set up the environment so it can be run automatically to pass
  autotest.

* **Details**:
  You are required to:

  1. Download
     [Tutorial 3.2](https://github.com/gw-odw/odw-2024/blob/main/Tutorials/Day_3/Tuto_3.2_Parameter_estimation_for_compact_object_mergers.ipynb)
     and add it to this repository as `notebook/a1.ipynb`.

  2. Potentially modify `src/phys305_hw5/a1.ipynb` so it can be run
     successfully on VSCode.

  3. Potentially modify "pyproject.toml" to set up the python
     environment so the notebook can be run (tested) automatically.

  4. Commit all changes (including the notebook) to Git.


### **Assignment 2**: Test at Least One Built-in Bilby Sampler (2 points)

* **Objective**:
  [Bilby](https://lscsoft.docs.ligo.org/bilby) has [multiple built-in
  samplers](https://lscsoft.docs.ligo.org/bilby/samplers.html#).
  Test them and make at least one work for the ODW tutorial.

* **Details**:
  You are required to:

  1. Copy `src/phys305_hw5/a1.ipynb` to `src/phys305_hw5/a2.ipynb` and
     add it to this Git repo.

  2. Right below `# Run the analysis`, run
     `bilby.core.sampler.get_implemented_samplers()`
     to get a list of implemented samplers.

  3. Test at least one of them by changing the cell
     ```
     result_short = bilby.run_sampler(
         likelihood, prior, sampler='bilby_mcmc', outdir='short', label="GW150914",
	 ...
     )
     ```
     to use the name another sampler.
     Note that you may need to modify "pyproject.toml" to set up the
     python environment so the notebook can be run (tested)
     automatically.

  4. Commit all changes (including the notebook) to Git.


### **Assignment 3**: Setup Bibly Plugin to Implement Your Own Sampler

* **Objective**:
  Following the
  [Bibly sampler-template](https://github.com/bilby-dev/sampler-template)
  and turn the homework repo into a sampler repo.

* **Details**:
  You are required to:

  1. According to the
     [template's README](https://github.com/bilby-dev/sampler-template),
     you need to provide an "entry point" in `pyproject.toml`.
     Let's name the sampler `MySampler` so the pyproject section looks like:
     ```
     [project.entry-points."bilby.samplers"]
     mysampler = "phys305_hw5.a34:MySampler"
     ```

  2. Given the above entry point, copy the
     [template](https://github.com/bilby-dev/sampler-template/blob/main/src/demo_sampler_bilby/plugin.py)
     to `src/phys305_hw5/a34.py` and rename the class accordingly.

  3. Commit all changes (including the notebook) to Git.


## Additional Notes

* **Collaboration**:
  You are encouraged to discuss ideas with your peers, but your
  submission must reflect your own work.
* **Help and Resources**:
  If you encounter any difficulties, please refer to the course
  materials, consult your instructor, or seek help during office
  hours.
* **Deadlines**:
  Be mindful of the submission deadline, as late submissions will not
  be accepted.

Good luck, and have fun working on the assignments!
