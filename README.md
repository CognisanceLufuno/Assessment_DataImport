# Assessment_DataImport
1.	File Data Extraction – Import data from csv files provided using SSIS
a.	The package imports data from csv files provided into respective tables.
b.	Truncates the data tables every time before load.
c.	Archives the files after data loads.
d.	Keeps track of the files being processed in the backend (Store the audit information – file processed, date and time, record counts, etc.).

SQL:
1.	IRBA AQI Reporting
a.	SQL script that counts the subsidiary companies flagged as PIE for each UltimateHoldingCompany. Returns UltimateHoldingCompany with at most 2 subsidiary companies flagged as PIE.
b.	SQL script that returns UltimateHoldingCompany that is a PIE, if any subsidiary company under the UltimateHoldingCompany is a PIE or have a PIS score greater 2000 then flag the UltimateHoldingCompany as PIE.
c.	SQL script that returns total hours charged by each signing partner.
d.	SQL script that links all the data in all the tables into a single result-set.
i.	Groups hours per UltimateHoldingCompany and signing partner. 
ii.	Group billed amount per UltimateHoldingCompany and invoice.
iii. Adds a calculated column to the result-set to show TotalBilledAmount at the UltimateHoldingCompany level. 
iv.	The script dynamically returns data between the beginning of the previous calendar year and end of the previous calendar (Posting date should be used for this). 
v.	Returns only singing partner data.
vi.	Orders data by UltimateHoldingCompany, client, posting date.
