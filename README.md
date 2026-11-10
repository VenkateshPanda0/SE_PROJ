# SE_PROJ
VENKATESH PANDA


PES1UGCS524

## Software Engineering Labs

Labs 1, 2 and 3 use the self-service coffee kiosk scenario from the handouts.

| Lab | Contents |
| --- | --- |
| [Lab 1](lab%201/) | Five functional and two nonfunctional requirements in Word, UML use-case diagram, and one-page use-case flow in Word and PDF. |
| [Lab 2](lab%202/) | Epics and backlog, illustrative burndown charts, reflection on the completed Jira simulation, and supplied story screenshots packaged in Jira Evidence.pdf. |
| [Lab 3](lab%203/) | Five-component architecture diagram with four interfaces and a one-page architecture justification in Word and PDF. |
| [Lab 4](lab%204/) | Previously completed before-and-after demonstration videos. |
| [Lab 5](lab%205/) | Assigned online-exam repository, corrected Python code, before-and-after static-analysis reports, issue table and reflection. |
| [Lab 6](lab%206/) | Assigned tennis-scoring repository, separate statement and branch coverage tests, and rendered terminal results. |

## Verified results

- Lab 5 achieved Pylint 10.00/10, zero Bandit findings and zero Flake8 diagnostics. Three commits separate formatting, security and maintainability fixes.
- Lab 6 statement coverage is 100% with 20 tests. Branch coverage is 100% with 34 tests, covering all 38 statements and all 30 measured branches. Two commits record the separate suites.
- Jira board 69 contains two epics and five stories. Sprint 71 completed 7 points and sprint 72 completed 8 points. Both sprints are closed.

[Jira workspace](https://yashasc1223.atlassian.net/jira/software/projects/COFFEE/boards/69/backlog)

## Evidence limitations

Lab 2 includes the five supplied story screenshots. The backlog, estimate-field, active-board and native burndown screenshots remain missing. Simulated Burndown.pdf is explicitly illustrative. Reflection.pdf describes the actual short simulation.

Lab 6 output PNGs render real test results. They are labeled rendered terminal output and do not fulfill the handout's literal terminal-screenshot requirement.

## Clone the assigned repositories

The Lab 5 and Lab 6 clones are included as Git submodules so their required commit history remains available.

```sh
git clone --recurse-submodules https://github.com/VenkateshPanda0/SE_PROJ.git
# For an existing clone
git submodule update --init --recursive
```

## Reproduce checks

Install the tools in a Python virtual environment.

```sh
python -m pip install pylint bandit flake8 coverage pytest
cd "lab 5/L5_34_online_exam"
python -m pylint online_exam.py
python -m bandit -r online_exam.py
python -m flake8 online_exam.py
python online_exam.py
```

From `lab 6/L6_L7_34_tennis_scoring/lab6`, run

```sh
python -m coverage run --include=tennis_scoring.py -m pytest CodeCoverageTest_PES1UGCS524_tennis_scoring.py
python -m coverage report -m
python -m coverage run --branch --include=tennis_scoring.py -m pytest BranchCoverageTest_PES1UGCS524_tennis_scoring.py
python -m coverage report -m
```
