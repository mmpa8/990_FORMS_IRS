# Trustees and Boards' Members Names for Education Institions. 
 
In this repository, we will scap names of Trustees and Boards' members for non-profit education instituions in the U.S. The data is directly gatehred from the forms 990s collected by the Internal Revenue Service (IRS).  

## 990 Form
[From IRS website on 990 form]

**__Form 990 is the IRS' primary tool for gathering information about tax-exempt organizations, educating organizations about tax law requirements and promoting compliance__**. Organizations also use the Form 990 to share information with the public about their programs. Additionally, most states rely on the Form 990 to perform charitable and other regulatory oversight and to satisfy state income tax filing requirements for organizations claiming exemption from state income tax.


Data from 990 forms, such as **Employer Identification Number (EIN), Object_ID (ID for the 990 form), and institutions general infomration** is hosted and extracted from Amazon S3. 

## AWS IRS 990 Filings Explorer:
[This IRS 990 Filings Explorer] allows us to search for electronically filed Form 990s hosted on Amazon S3. Amazon has made this essential resource available, but they have not provided an easy way to search the records. This very simple site lets you search for these records by the organization's name, and provides a link to the S3-hosted XML file.

The data used in this project is specifically extracted from the CSV 2021 file of 990, indexed by year. From this file, we will extract the OBJECT_ID to then run it through the XML-990-Reader.

This is how the data from the AWS Filing Explorer looks like (3 rows)

| RETURN_ID   | FILING_TYPE   | EIN   | TAX_PERIOD   | SUB_DATE   | TAXPAYER_NAME   | RETURN_TYPE   | DLN   | OBJECT_ID   | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
|17606342      | EFILE 452772761    | 201906   | 1/21/2021 10:02:51 AM   | CAMDENS CHARTER SCHOOL NETWORK INC   | 990 9.349307e+13   | 2.020107e+17





17606343       EFILE 237061115     201906 1/21/2021 10:02:51 AM JACKSON STATE UNIVERSITY DEVELOPMENT FOUNDATION INC         990 9.349307e+13 2.020107e+17
17606347       EFILE 344427516     201904 1/21/2021 10:02:52 AM                                   TIFFIN UNIVERSITY         990 9.349307e+13 2.020107e+17


RETURN_ID FILING_TYPE       EIN TAX_PERIOD              SUB_DATE                                       TAXPAYER_NAME RETURN_TYPE          DLN    OBJECT_ID


17606342       EFILE 452772761     201906 1/21/2021 10:02:51 AM                  CAMDENS CHARTER SCHOOL NETWORK INC         990 9.349307e+13 2.020107e+17
17606343       EFILE 237061115     201906 1/21/2021 10:02:51 AM JACKSON STATE UNIVERSITY DEVELOPMENT FOUNDATION INC         990 9.349307e+13 2.020107e+17
17606347       EFILE 344427516     201904 1/21/2021 10:02:52 AM                                   TIFFIN UNIVERSITY         990 9.349307e+13 2.020107e+17

#### What is the Object ID?

The object ID represents the unique identifier of the 990 form for each organization. 

[This IRS 990 Filings Explorer]:http://irs-990-explorer.chrisgherbert.com/#aws-index-files
[From IRS website on 990 form]:https://www.irs.gov/charities-non-profits/form-990-resources-and-tools
