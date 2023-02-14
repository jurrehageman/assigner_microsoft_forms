# Assigner (Microsoft Forms Version)

Get the best assignment out of student preferences for a project.
Uses the Munkres algorithm:
https://docs.scipy.org/doc/scipy-0.18.1/reference/generated/scipy.optimize.linear_sum_assignment.html

## Getting Started

These instructions will show some examples to run the scripts

### Prerequisites

Scipy and numpy need to be installed on your system


### Installing

Use pip to install scipy and numpy.
- Numpy:

```
pip install numpy
```

- Scipy

```
pip install scipy
```

## Running the assignment.py module

This module will generate the actual assignment

Example:
```
python3 assigner.py dummy_data.xlsx assignment.xlsx experiments.txt
```

Example files are included

### Arguments:
usage: assigner.py [-h] infile outfile experiment_names

Required arguments:
- infile: path to the Excel file containing the preferences
- outfile: path to the Excel file with the assignment
- experiment_names: a txt file with number of positions and the name of the experiments


## Example Workflow

- First create a Microsoft Forms as shown [here](https://forms.office.com/Pages/ResponsePage.aspx?id=FJCzo9x6-kihFDfCQ029aUl4zQoSS2FNpqWJwSaQQQpUNjFaOTlES05IUU9CRkdMOEcxNjI4MlJEWS4u)

- Share your form to submit data. Download the data as Excel file:

- Create a text file with the following layout: positions per experiment;experiment name (see example)


- Run the script:
```
python3 assigner.py ../test_data/dummy_data.xlsx ../test_data/assignment.xlsx ../test_data/experiments.txt
```

- An Excel file is generated that can be opened in Excel. The terminal output will show some statistics.


## Built With

* [Scipy linear sum assignment module](https://docs.scipy.org/doc/scipy-0.18.1/reference/generated/scipy.optimize.linear_sum_assignment.html)


## Authors

* **Jurre Hageman** 

## License

This project is licensed under the GNU General Public License (GPL)

## Acknowledgments

Dave Langers helped on the algorithm