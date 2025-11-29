# Analyzing the Time to Solve Issues in the Zephyr GitHub Repository: A Case Study

The following is a report on mining open source project data from GitHub using the Zephyr project as a case study.  Zephyr is a widely
used open source real-time operating system (RTOS) for embedded devices. Pull request data will be used to answer the question: "What is the median time to solve bug issues?"

Zephyr Open-Source GitHub Repository: https://github.com/zephyrproject-rtos/zephyr

## Methodology
Data was mined over the two year range between November 18th, 2023 and November 18th, 2025, and to analyze
whether an issue was a bug or not, I used the GitHub labels. It was essential to read and investigate the developer notes within the repository, to determine how the developers were using their
created labels that were attached to each pull request. Because the use of labels by developer’s across this code workspace was both prevalent and well documented, they served as essential
insight into determining which pull requests were related to bugs.

## Analyses and Results
Over a total of 43,651 pull requests, I analyzed 41,355 of which were closed or solved pull requests and 2,077 of which were identified as closed, bug-related issues. 
The closed-at and created-at metadata for each closed bug-related pull request were used to calculate a "time to solve" value, which was calculated by converting each of these into a datetime
python object and then calculating the difference. Each of these time to solve values for each PR then resulted in a median time to solve across the entire closed, bug PR dataset, which was 3 days 23 hours, 19 minutes, and 36 seconds - or after rounding up - 4 days.

_In the past two years, it took developer’s about 4 days to solve bugs in the Zephyr repository._
