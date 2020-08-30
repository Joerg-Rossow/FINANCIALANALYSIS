# Generate a proper calendar file for Excel Powerpivot

To setup a Powerpivot data model in Microsoft Excel it is best practice to add a calendar file as a dimensional table for filtering financial data by the dimension time (e.g. year, month, day). A proper calendar file can easily be prepared within Excel but it is also possible to setup the file in python as part of other preparations e.g. for an analytics project.

The start and end date is set within the script. The file is beeing generated as a python list, exported to a pandas data frame and saved in csv file format. It can be imported into Excel and into the Poverpivot model.