# Changing the class assignment thresholds

<img src="logo.png" alt="Logo" width="300" height="300">

First of all, thanks for your interest in using our programs.

Most classifiers from the Python packages can predict the classes of instances as either binary values, like yes or no, or as probabilities, for example, using values from 0 to 1. The standard is: if the value is smaller or equal to 0.5, it belongs to one class, and if it is greater than that, it belongs to the other class.

We can change that

For example, every morning I check the weather forecast. If it says 30% chance of raining, I do not bring an umbrella. But if it says 70 or 80%, then I bring an umbrella.

We can do the same with classifiers. Instead of assigning instances to one or the another based on the 0.5 value, we can change it to pretty much any other value. For example, 0.7. This way, instances that get prediction values below 0.7 will go to one class, and only those above 0.7, go to the other.

# The code in this repository
 
This simple script will:
- open a CSV file from the command line
- perform 10-fold stratified cross-validation
- train a Random Forest classifier
- predict the class of the test instances using probability scores

After that, it will calculate the balanced accuracy and the F1 score based on different class assignment thresholds (cutoff values).

And will plot everything to show the variation.

## How to run it

1. Clone the repo
   ```sh
   git clone https://github.com/Nezu-life/change_class_threshold.git
   cd change_class_threshold
   ```
2. Run it with either the provided CSV file, or your own data.
   ```sh
   python3 change_classification_threshold.py <input_file.csv>
   ```

## Dependencies

- Pandas (2.1.1)
- Sklearn (1.3.1)
- Matplotlib (3.8.0)
- Numpy (1.23.5)

## Ready to go?

Comments, suggestions, forks and improvements are very much welcome.

Made with ❤️  by Tiago Lopes, PhD - the founder of Nezu Life Sciences.

## Reference for the example blood donation dataset

Yeh, I-Cheng, Yang, King-Jang, and Ting, Tao-Ming, "Knowledge discovery on RFM model  using Bernoulli sequence, "Expert Systems with Applications, 2008 (doi:10.1016/j.eswa.2008.07.018).

<p align="right">(<a href="#readme-top">back to top</a>)</p>
