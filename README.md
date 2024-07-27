# COMP311 Cucumber Group9

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/sensational-vegetables/comp311-cucumber-group9)

Select **Open in GitHub Codespaces** and then **Create codespace**. **GitHub** will prepare the development environment with all installed dependencies.

To make sure everything works together correctly, run Cucumber from Terminal.

```sh
mvn test
```

```
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running testrunner.TestRunner

Scenario Outline: Today is or is not Friday # src/test/resources/hellocucumber/is_it_friday_yet.feature:11
  Given today is "Friday"                   # hellocucumber.SearchSteps.today_is(java.lang.String)
  When I ask whether it's Friday yet        # hellocucumber.SearchSteps.i_ask_whether_it_s_Friday_yet()
  Then I should be told "TGIF"              # hellocucumber.SearchSteps.i_should_be_told(java.lang.String)

Scenario Outline: Today is or is not Friday # src/test/resources/hellocucumber/is_it_friday_yet.feature:12
  Given today is "Sunday"                   # hellocucumber.SearchSteps.today_is(java.lang.String)
  When I ask whether it's Friday yet        # hellocucumber.SearchSteps.i_ask_whether_it_s_Friday_yet()
  Then I should be told "Nope"              # hellocucumber.SearchSteps.i_should_be_told(java.lang.String)

Scenario Outline: Today is or is not Friday # src/test/resources/hellocucumber/is_it_friday_yet.feature:13
  Given today is "anything else!"           # hellocucumber.SearchSteps.today_is(java.lang.String)
  When I ask whether it's Friday yet        # hellocucumber.SearchSteps.i_ask_whether_it_s_Friday_yet()
  Then I should be told "Nope"              # hellocucumber.SearchSteps.i_should_be_told(java.lang.String)
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.551 s - in testrunner.TestRunner
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 3, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  18.086 s
[INFO] Finished at: 2024-07-27T12:08:04Z
[INFO] ------------------------------------------------------------------------
```

Please see this tutorial for the in-class demonstration: https://cucumber.io/docs/guides/10-minute-tutorial/?lang=java
