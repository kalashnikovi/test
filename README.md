# test
Test Repo

master branch
2020-11-25 new line
commit test



### 2021-10-07

1. Stop Tomcat.
2. Database changes:

    **IMPORTANT:**
        Run **ONLY** if the SSO-app is working on a dedicated database.

  - Run SQL-script ${SSO_SERVICE_PROJECT}/sql/currency-country.sql
    + Tables **country** and **currency** will be renamed to **country_old** and **currency_old**.
    + Will be created new tables  **country** and **currency** with data.
3. Deploy application to Tomcat.
4. Run Tomcat