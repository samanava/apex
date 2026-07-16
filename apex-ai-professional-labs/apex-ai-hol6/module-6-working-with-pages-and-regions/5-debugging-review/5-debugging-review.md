# Lab 5: Enable Debugging and Review

## Introduction

In this lab, you use APEX debug output to inspect TAP Home page rendering, timing, and SQL activity.

Estimated time: 5 minutes

### Objectives

In this lab, you will learn how to:

- Enable APEX debugging.
- Open the debug output.
- Review Home page rendering steps, elapsed times, and SQL activity.
- Disable debugging after the review.


## Task 1: Enable Debugging

In this task, you will enable APEX debugging from the running TAP Home page. Debug mode records page rendering details that help you inspect region execution and SQL behavior.

1. From the running TAP **Home** page, select **Debug** in the **Developer Toolbar**.

    ![Debug selected in the Developer Toolbar](images/01-enable-debug-toolbar.png " ")

2. Select **Enable Debug**.

    Select **App Trace**.

    ![Enable Debug menu opened from the Developer Toolbar](images/03-select-app-trace-debug.png " ")

3. Confirm that the debug toolbar appears.

    ![App Trace selected from the Enable Debug menu](images/enabled.png " ")

## Task 2: Review and Disable Debugging

In this task, you will review the debug output and identify any slow page-rendering steps. After the review, you will turn debugging off so regular page runs do not collect debug details.

1. Select **Debug**.

    Select **View Debug**.

    ![View Debug selected from the Debug menu](images/04-open-view-debug-menu.png " ")

2. Review page and region rendering steps, SQL queries, and elapsed times.

    ![Debug message list displayed](images/05-debug-message-list.png " ")

3. Select the debug identifier.

    Review the detailed timing and execution messages.

    ![Debug identifier selected](images/06-select-debug-identifier.png " ")

    ![Debug detail view showing timing and execution messages](images/07-debug-details-timing.png " ")

4. Identify regions or queries with long elapsed times.

5. To disable debugging, select **Debug > Current Debug Level > Off** in the **Developer Toolbar**.

    ![Debug turned off from the Developer Toolbar](images/08-turn-off-debug.png " ")

## Summary

In this lab, you enabled APEX debugging from the running TAP Home page and reviewed the generated debug output.

You opened the debug message list, selected a debug identifier, and inspected timing and execution messages for the page request.

Debug output helps you understand how a page renders, which regions and SQL statements run, and where performance issues may appear.

At the end of this lab, you are on the running TAP **Home** page with debugging disabled. In the next lab, you will switch to the Employee Self Service (ESS) application and open **Home** in Page Designer.

You may now proceed to the next lab.

## Acknowledgements

- **Author** - Sahaana Manavalan, Senior Product Manager
- **Author** - Roopesh Thokala, Principal Product Manager
