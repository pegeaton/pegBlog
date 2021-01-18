# Part3: A more complex example -- Work in Progress

In this section we dive into the details of a more complex GitHub Actions workflow, written to support Modern Apps Ninja member registration, handling secrets and environment variables.


The assigm
1. Contributor completes assignment file
2. Contributor submits a pull request for assignment file to the Modern Apps Ninja course repository
3. GitHub Action verify-assignment is triggered to run
3.1 If assignment results are correct the pull request is closed
3.2 If the assignment results are incorrect the error is posted to the pull request for modification.


