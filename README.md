# DNS Filter for Hong Kong Fraudulent Bank Websites

## Initiative
Recently my parents asked me that they received an SMS, which mentioned that their account was banned. Although they consulted me and didn't click on any links in the SMS, I wonder if I can create an DNS filter to block any suspicious bank websites.

## Source
I identify that there is a webpage named ["Beware of Fraudsters!" in Hong Kong Monetary Authority (HKMA)](https://www.hkma.gov.hk/eng/smart-consumers/beware-of-fraudsters/). It listed the URLs of the suspicious bank websites identified. However, the list is not machine readable.

## Filters
The HKMA website does categorize the incident into different types. (However, the categorization seems not systematic.)

I try to only categorize the filters into the following two types.

### DNS Filter for Hong Kong Fraudulent Bank Websites
This filter will include all domains that are identified as fraudulent bank websites in HKMA. However, the domains hosting the suspicious app package will not be included.

### DNS Filter for Domains Hosting Hong Kong Fraudulent Bank Apps
I identify that the suspicious apps may be hosted in some well-known apk hosting websites. Someone may not want to block them, and as a result, I seperate the filter from the above one.

## Usage
I only tested the filters in AdGuard Home. Please report to me if they are functioning normally in other products.

To add the filter, please select "Filters > DNS blocklists" in your AdGuard Home. Click "Add blocklist", and then click "Add a custom list". Finally, input the URL of your desired filter.

- DNS Filter for Hong Kong Fraudulent Bank Websites (https://raw.githubusercontent.com/alan852/DNS-Filter-for-HK-Fraudulent-Bank-Websites/main/filters/adguard_home_filter.txt)

- DNS Filter for Domains Hosting Hong Kong Fraudulent Bank Apps (https://raw.githubusercontent.com/alan852/DNS-Filter-for-HK-Fraudulent-Bank-Websites/main/filters/adguard_home_filter_extra.txt)

## Future Planning
Currently, the filters are manually created. I plan to create some scripts to automate the whole process.
