# supabase-powerbi-guide

Hh everyone 

Here How to Connect Supabase to Power BI via ODBC
1. Get Your Supabase Connection Details
    Go to your Supabase project dashboard.
    Navigate to Settings > Database > Connection Pooling.
    Copy the following details from the Transaction pooler section:
    Host:..........
    Port: ....
    Database: postgres
    User: ........
    Password: (your Supabase password)
2. Download and Install the PostgreSQL ODBC Driver
    Go to: https://www.postgresql.org/ftp/odbc/releases/
    Download the latest psqlodbc_x64.msi .
    Run the installer and complete the installation.
3. Set Up an ODBC Data Source (DSN)
    Open ODBC Data Source Administrator (search for "ODBC" in Windows Start).
    Go to the System DSN or User DSN tab and click Add.
    Select PostgreSQL Unicode and click Finish.
    Fill in the details:
    Data Source: (Any name, e.g., Supabase)
    Server: (your Supabase pooler host)
    Port: ....
    Database: postgres
    Username: .........
    Password: (your Supabase password)
    SSL Mode: require
    (Optional) Uncheck "Verify Server Certificate" if you have SSL issues.
    Click Test to ensure the connection works, then OK to save.
4. Connect Power BI to the ODBC DSN
    Open Power BI Desktop.
    Go to Home > Get Data > ODBC.
    Select the DSN you just created (e.g., Supabase).
    Click OK.
    Select the tables you want to import and click Load.
