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

- First create a Microsoft Forms as shown below:

![alt text](https://github.com/jurrehageman/assigner-forms/blob/master/images/form.png "Microsoft Form setup")

- Share your form to submit data. Download the data as Excel file:

- Create a text file with the following layout: positions per experiment;experiment name

![alt text](https://github.com/jurrehageman/assigner-forms/blob/master/images/experiments_names.png "Experiment names")

- Run the script:

python3 assigner.py ../test_data/dummy_data.xlsx ../test_data/assignment.xlsx ../test_data/experiments.txt

- Running the script using the example data will generate the following output:

![alt text](https://github.com/jurrehageman/assigner-forms/blob/master/images/terminal_output.png "Terminal Output")

- An Excel file is generated that can be opened in Excel:

![alt text](https://github.com/jurrehageman/assigner-forms/blob/master/images/excel_screenshot.png "Excel file opened in Excel")

## Built With

* [Scipy linear sum assignment module](https://docs.scipy.org/doc/scipy-0.18.1/reference/generated/scipy.optimize.linear_sum_assignment.html)


## Authors

* **Jurre Hageman** 

## License

This project is licensed under the GNU General Public License (GPL)

## Acknowledgments

Dave Langers helped on the algorithm