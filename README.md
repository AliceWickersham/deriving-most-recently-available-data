# Method for deriving a variable which contains data from the most recently available timepoint when repeated measurements of that variable have been taken

This Stata code illustrates a method for iterating backwards through multiple measurement timepoints to derive a variable containing data from the most recently available (i.e., non-missing) timepoint.

It draws on the example of ethnicity data in the National Pupil Database ([NPD](https://www.gov.uk/government/collections/national-pupil-database)). In the NPD, ethnicity is available from annual Autumn, Spring, and Summer school censuses. In a study I recently conducted, I needed to identify each individual's ethnicity, as derived from the most recently available timepoint to their Key Stage 4 assessment year. So, if an individual's Key Stage 4 assessment year was 2009/10, then in the first instance, we would want to use their ethnicity as recorded in the 2009/10 academic year's Summer census. But if they were missing ethnicity data in that census, then ethnicity should be taken from the 2009/10 Spring census, followed by the 2009/10 Autumn census, 2008/09 Summer census, 2008/09 Spring census....and so on, until all available timepoints have been checked for available ethnicity data.

This method has two key benefits:

- It minimises that the extent of missing data in the final variable.
- It ensures that the most up-to-date ethnicity data is captured for each individual. 

The code was developed by  [Alice Wickersham](https://www.kcl.ac.uk/people/alice-wickersham), supported by ADR UK (Administrative Data Research UK), an Economic and Social Research Council (ESRC) investment (part of UK Research and Innovation). Grant number: ES/W002531/1


**It is important to note that this repository does not contain any data. The data cannot be made publicly available, but can be accessed with permissions from the Department for Education.** 

## Table of Contents

- [License](#license)
- [Availability of Materials and Data](#availability-of-materials-and-data)

## License

This code has been released under [GNU General Public License (v3)](https://www.gnu.org/licenses/gpl-3.0.en.html) license to promote open source app development and sharing of innovation within the research community. Simply, use freely but make your code accessible to others.

## Availability of Materials and Data

The data cannot be made publicly available, but can be accessed with permissions from the Department for Education. The code developer ([Alice Wickersham](mailto:alice.wickersham@kcl.ac.uk)) can provide more information about the process.
