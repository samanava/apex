# Introduction

## What is APEX?

Oracle APEX is a low-code application platform for Oracle Database. APEX Application Development, Autonomous Data Warehouse (ADW), Autonomous Transaction Processing (ATP), and Autonomous JSON Database are fully managed services, pre-integrated and pre-configured with APEX, for rapidly building and deploying modern data-driven applications in Oracle Cloud. Business users, citizen developers, and application developers can create enterprise apps faster with less code, without learning complex web technologies, using only a browser.

Oracle APEX continues to evolve for modern application development. Oracle APEX 26.1 includes AI-assisted development capabilities, APEXlang for expressing application intent as structured metadata, Universal Theme enhancements, workflow improvements, security updates, and richer declarative components. These features build on the same core model you use in this workshop: pages, regions, items, shared components, and data-driven behavior.

In this workshop, you explore and review the Page Designer in APEX. Then, you create and configure pages and regions in the Talent Acquisition Portal. You also make a short update in the Employee Self-Service Portal (ESS) so both applications begin to feel more structured and useful.

You are building a Talent Management System (TMS) for a sample company called Acme Corp. The system covers the complete employee lifecycle:

```text
Job Opens -> Candidate Applies -> Interviews -> Offer Made
     -> Offer Accepted -> Onboarding -> Active Employee
         -> Leave Management -> Self-Service -> Analytics
```

This lifecycle is split across three APEX applications:

- **Talent Acquisition Portal** - Used by recruiters and hiring managers to post jobs, track candidates, schedule interviews, and manage offers.
- **Employee Self-Service Portal (ESS)** - Used by employees and HR administrators for onboarding tasks, leave requests, payslips, employee profiles, and HR self-service.
- **HR Analytics App (HAA)** - Used by HR administrators and department heads for pipeline, time-to-hire, headcount, and leave analytics.

Once the pages and regions are created, Talent Acquisition Portal users will be able to view the following candidate and hiring details in the application:

- Candidate details
- Application history
- Open requisitions
- Candidate pipeline stage
- Applied date

ESS users will see a personalized home page with onboarding progress placeholder content.

Estimated time: 35 minutes

## Objectives

In this workshop, you will learn how to:

- Navigate through and review the Page Designer panes.
- Create a blank page to display business information.
- Add regions for static and dynamic content.
- Configure a Cards region to display query results in a visual layout.
- Add a Global Page region that appears across an application.
- Add page regions to a second application.
- Enable and review debug output to inspect page rendering and SQL execution.

## Prerequisites

- An APEX workspace.

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
- [Oracle APEX Tutorials](https://apex.oracle.com/en/learn/tutorials/)
- [Oracle APEX Community](https://apex.oracle.com/community/)
- [Oracle APEX Discussion Forum](https://forums.oracle.com/ords/apexds/domain/dev-community/category/application_express)

You may now **proceed to the next lab**.

## Acknowledgements

- **Author** - Sahaana Manavalan, Senior Product Manager
- **Author** - Roopesh Thokala, Principal Product Manager
