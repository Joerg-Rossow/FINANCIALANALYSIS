# Merge and group tables from MS Excel

One of the most used formulas in MS Excel to merge (enrich) data from different sources is vlookup. However the amount of cells with vlookup formulas is limited due to both the peformance of hardware and MS Excel. When data gets bigger, waiting times rise and there are freeze times and software crashes on an average work place equipment. As a reaction the amount of data is usually limited which causes multiple preparation times and additional steps.

To analyise more data (and get holistic and cross-divisional results and findings) but still use workplace equipment and remain independent from other IT resources, vlookups can be done via python. Once prepared, the data can be handled in Excel/PowerQuery/Powerpivot). Remark: High volume data analysis should be handled in adequate hardware and there has to be some automation. Doing this regularly in MS Excel is not appropriate in terms of modern business management.

**Problem**: The data file from the general ledger of an accounting system has 129.000 entries. There are several years, months and versions and this export just names the cost account but the cost account name and its position within the chart of accounts is needed in connection with the booking data. Due to the nature of accounting, there are more than one booking on a cost account within a year, month, version and cost center. The data has be grouped on the level of cost accounts.

**Approach**:

1. Import data from MS Excel to a pandas dataframe
2. Merge (enrich) data (as 'vlookup' in MS Excel, as 'join' in SQL)
3. Group data
4. Export data from dataframe to a .csv file