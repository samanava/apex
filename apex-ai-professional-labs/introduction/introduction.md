# Introduction

## What is APEX?

Oracle APEX is a low-code application platform for Oracle Database. APEX Application Development, Autonomous Data Warehouse (ADW), Autonomous Transaction Processing (ATP), and Autonomous JSON Database are fully managed services, pre-integrated and pre-configured with APEX, for rapidly building and deploying modern data-driven applications in Oracle Cloud. Business users, citizen developers, and application developers can create enterprise apps faster with less code, without learning complex web technologies, using only a browser.

A page is the basic building block of an application. A region is an area on a page that serves as a container for content. Use Page Designer to maintain and enhance pages within an Oracle APEX application.

In this workshop, you use Page Designer to create and configure pages and regions in the Talent Acquisition Portal (TAP) and Employee Self-Service Portal (ESS). You work with Static Content, Dynamic Content, and Cards regions; configure region sources and positions; add a region to the Global Page; and inspect page rendering with Debug mode.

You are building a Talent Management System (TMS) for a sample company called Acme Corp. The system covers the complete employee lifecycle:

```text
Job Opens -> Candidate Applies -> Interviews -> Offer Made
     -> Offer Accepted -> Onboarding -> Active Employee
         -> Leave Management -> Self-Service -> Analytics
```

The Talent Management System is split across three APEX applications:

- **Talent Acquisition Portal** - Used by recruiters and hiring managers to post jobs, track candidates, schedule interviews, and manage offers.
- **Employee Self-Service Portal (ESS)** - Used by employees and HR administrators for onboarding tasks, leave requests, payslips, employee profiles, and HR self-service.
- **HR Analytics App (HAA)** - Used by HR administrators and department heads for pipeline, time-to-hire, headcount, and leave analytics.

In this workshop, you update TAP to display the following candidate and hiring information:

- Candidate details
- Application history
- Open requisitions
- Candidate pipeline stage
- Applied date

ESS users will see a personalized home page with onboarding progress placeholder content.

### Workshop Flow

Complete the workshop in the following order:

1. **Get Started** - Access an Oracle APEX workspace.
2. **Lab 1: Create Candidate Profile Page Manually** - Create a blank page and add two Static Content regions.
3. **Lab 2: Add Regions to the Candidate Pipeline Page** - Add Dynamic Content and Cards regions.
4. **Lab 3: Configure the Global Page** - Add a shared hiring banner to Page 0.
5. **Lab 4: Add a Dynamic Content Region** - Display the active-candidate count on TAP Home.
6. **Lab 5: Enable Debugging and Review** - Enable App Trace and review page-rendering details.
7. **Lab 6: Employee Self Service (ESS) - Add Home Regions** - Add welcome and onboarding-progress regions to ESS Home.

Estimated Workshop Time: 35 minutes

## Objectives

In this workshop, you will learn how to:

- Navigate through and review the Page Designer panes.
- Create a blank page with the Create Page Wizard.
- Create regions from the Gallery and the Rendering Tree context menu.
- Configure region types, sources, positions, and attributes.
- Use a Dynamic Content region to display HTML returned by a PL/SQL function.
- Configure a Cards region based on a SQL Query.
- Add a region to the Global Page so it appears throughout the application.
- Compare APEX debug levels and review page-rendering details.
- Use the `&APP_USER.` substitution string in a Static Content region.

## Prerequisites

- An APEX workspace.

- The **Talent Acquisition Portal** and **Employee Self Service** applications.

- The `TMS_JOB_REQUISITIONS` and `TMS_CANDIDATES` tables.

- An API key for the AI provider of your choice. Supported providers include OCI Generative AI, OpenAI, Cohere, Google Gemini, Anthropic Claude, Mistral AI, Ollama, and Generic OpenAI API Compatible providers.

If you choose OCI Generative AI as your AI provider, the prerequisites are as follows:

- A paid Oracle Cloud Infrastructure (OCI) account, or a Free Oracle Cloud account with $300 in credits valid for 30 days to use on other services. Learn more at [oracle.com/cloud/free](https://www.oracle.com/cloud/free/).

    The OCI account must be created in, or subscribed to, a region that supports the OCI Generative AI service. OCI Generative AI is supported in the following regions:

    - Brazil East (Sao Paulo)
    - Germany Central (Frankfurt)
    - India South (Hyderabad)
    - Japan Central (Osaka)
    - Saudi Arabia Central (Riyadh)
    - UAE East (Dubai)
    - UK South (London)
    - US East (Ashburn)
    - US Midwest (Chicago)
    - US West (Phoenix)

    The OCI Generative AI service is available only in select regions. To see if your cloud region supports OCI Generative AI, visit the documentation.

- An OCI compartment. An Oracle Cloud account comes with two preconfigured compartments: the tenancy (root compartment) and `ManagedCompartmentForPaaS`, which is created by Oracle for Oracle Platform services.

- The logged-in user must have the necessary privileges to create and manage Autonomous Database instances in this compartment. You can configure these privileges using an OCI IAM policy. If you are using a Free Tier account, it is likely that you already have all the necessary privileges.

> **Note:** This workshop assumes you are using Oracle APEX 26.1. Some of the features might not be available in prior releases, and the instructions, flow, and screenshots might differ if you use an older version of Oracle APEX.

> **Important:** This workshop requires an active account with a supported Generative AI provider. Oracle APEX connects to the provider using your own credentials. Any API usage charges are billed directly by your provider. Please review your provider's pricing before proceeding.

## Downloads

If you are stuck or the apps are not working as expected, you can download and install the completed applications.

1. **[Download the Talent Acquisition Portal export](files/talent-acquisition-portal-app.sql)**.

2. **[Download the Employee Self-Service Portal export](files/employee-self-service-portal-app.sql)**.

## Learn More - Useful Links

- [Oracle APEX Product Overview](https://www.oracle.com/apex/)
- [Oracle APEX 26.1 Documentation](https://docs.oracle.com/en/database/oracle/apex/26.1/)
- [Managing Pages in an Application](https://docs.oracle.com/en/database/oracle/apex/26.1/htmdb/managing-pages-in-an-application.html)
- [About Page Designer](https://docs.oracle.com/en/database/oracle/apex/26.1/htmdb/about-page-designer.html)
- [About Regions](https://docs.oracle.com/en/database/oracle/apex/26.1/htmdb/about-regions.html)
- [Oracle APEX Tutorials](https://apex.oracle.com/en/learn/tutorials/)
- [Oracle APEX Community](https://apex.oracle.com/community/)
- [Oracle APEX Discussion Forum](https://forums.oracle.com/ords/apexds/domain/dev-community/category/application_express)

You may now **proceed to the next lab**.

## Acknowledgements

- **Author** - Sahaana Manavalan, Senior Product Manager
- **Last Updated By/Date** - Sahaana Manavalan, Senior Product Manager, July 2026
