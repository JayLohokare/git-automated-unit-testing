# git-automated-unit-testing
Simple Flask server implementation for unit testing git based PHP projects

The API takes git URLs does the following:
1. Takes GIT repo URL as input
2. Clones the repo on server
3. Runs PHPUNIT on the projects
4. Returns the test results as response


The current implementation is not ideal as the API could time out while it runs the tests.
Ideally, the API should lazily trigger a cron job to run the tests, and not wait for execution of the tests. 
