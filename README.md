# Data Quality
 - Use the CHECK CONSTRAINT inside the ETL, because will be processed in a set-based statement rather than ROW BY ROW
 - An Overview Data quality is the capability of data to satisfy the stated business, system, and technical requirements of an
   enterprise. Data quality is an insight into or an evaluation of data’s fitness
 - DDL Trigger for Database: MonitorSchema changes by Role 
 - Use stored procedures to insert and update the audit tables. Use the execute sql control flow taks to execute the SP, and pass
   in parameters from system and local package variables 
- **Some commonly used data quality dimensions are:**

    - Completeness 
    - Accuracy 
    - Timeliness 
    - Conformity 
    - Consistency.


---
**(Microsoft)**
 - Data Quality Client Application
 - DQS Knowledge Bases and Domains
 - Data Quality Projects
 - Data Cleansing
 - Data Matching
 - Reference Data Services in DQS
 - Data Profiling and Notifications in DQS
 - DQS Administration
 - DQS Security

---
**Data Profiling and Data Cleansing – The initial steps for your data quality management process(SAP)**
Data Quality Management initiative, including the following six implementable steps:

 - **Discover**: your enterprises data assets to get a clear understanding where your data is stored within the organization and how it is moved and consumed as well as look deeper into the systems and tables to get also first insight of the content of your d ata containers.
 - **Define**: your data standards, data policies, data qualty requirements to set the goal or target where you what to go with your data qualt management initiative. Also use this definition phase to define a common business term glossary to ensure that everyone within the company is talking about the same thing avoiding unnecessary and painfull missunderstanding
 - **Assess**: the existing sthe currently level of data quality based on the data standards and validation rules that you have setdefined, approved by your data stewar or business experts and bound to the data sources. Get away from rule of thumb or stomach feeling about the quality level of your data. Put figures and numbers to the to the data quality questions so you have some measures that allow you to prioritize also your upcoming cleansing strategy.
 - **Analyze**: the root cause of your identified bad data as well as identify the impact of the bad data to further downstream systems like from the data warehouse staging area to your individual reports. The data quality issue root cause analysis is an important piece to understand where e.g. in your operational system bad data is stored, that is then moved to your data warehouse data warehouse b the ETL processes.
 - **Improve**: your data quality by defining the right data cleansing strategy. After you are aware of the root causes of your  bad data quality, decide on where, when and how to take action. Set up the data quality firewall for your systems and applications to avoid that any new data entering your systems is not compliant with your requirements. Be it transactional , real-time entry of data by employees or customer self services or batch loading processes of external data or sources. Also define your cleansing strategy for the existing data by internal batch processes.
 - **Monitor**: your data quality constantly. Apply your data validation rules to your data sources on a regular schedule to get a historical trend analysis and see how your data quality scores change over time. Prove the benefit (and cost) of data cleansing or improvement activites by showing the increase of data quality on the scorecards. React early and proactively on slight decreases of your given data quality scores, even before your employees or even worser your suppliers or customerare unhappy and dissatisfied.
 









## Categorization of Data Data:

#### Master data:

 - Master Data Master data are high-value, key business information that describes the core entities of organizations and that supports
   the transactions and plays a crucial role in the basic operation of a business. It is the core of every business transaction, application, analysis, report, and decision. 

 - Master data can be recognized by nouns such as patient, customer, or product, to give a few examples. Master data can be grouped by places 
   (locations, geography, sites, areas, addresses, zones, and so on), parties (persons, organizations, vendors, prospects, customers, suppliers, patients, students, employees, and so on),
   and things (products, parts, assets, items, raw materials, finished goods, vehicles, and so on).

 - Master data are characteristically non-transactional data that are used to define the primary business entities and used by multiple business processes, systems, and applications in the organization. 
   
 - Master data are created once, used multiple times by different business processes, and either do not change at all or change infrequently.
 
 - Master data are generally assembled into master records, and associated reference data may form a part of the master record 

 - Master data, which represent key business entities

 - Master data are defined as the basic characteristics of instances of business entities such as 
  
       | Customers | Products | Parts | Employees | Accounts | Sites | Inventories | Materials | Suppliers | 

#### Reference data:

 - Reference data are sets of permissible values and corresponding textual descriptions that are referenced and shared by a number of systems, 
   applications, data repositories, business processes, and reports, as well as other data like transactional and master data records.

 - As the name suggests, reference data are designed with the express purpose of being referenced by other data, like master data and transactional data, 
   to provide a standard terminology and structure across different systems, applications, and data stores throughout an organization. 
 
- Codes are industry standard reference data sets used for classification of business establishments

 - Reference data can be created either within an organization or by external bodies. 

 - Usually, reference data do not change excessively in terms of definition apart from infrequent amendments to reflect changes in the modes
   of operation of the business
 
 - The creation of a new master data element may necessitate the creation of new reference data. 

_(for example, Standard Industrial Classification (SIC) codes are four-digit numerical codes assigned by the US government to business establishments to identify 
  the primary business of the establishment; NAICS_

 
  
    |Country codes            |State abbreviations    |Area codes       |Post codes    |ZIP codes       |
    |Diagnosis codes ICD-10   |Currency codes         |Corporate codes  |Status codes  |Product codes   |
    |Product hierarchy        |Flags                  |Calendar         |HTTP STATUS   |Industry codes  | 



  

#### Transactional data:

 - Transactional data describe business events, and comprise the largest volume of data in the enterprise. 
 - Transaction data describe relevant internal or external events in an organization

       |Orders     | invoices        | Payments       | Patient encounters | Insurance claims | 
       |Deliveries | Storage records | Travel records | Complaints         |Shipments         |

#### Historical data:

 - Historical Data Transactional data have a time dimension and become historical once the transaction is complete.
 - Historical data contain significant facts, as of a certain point in time, that should not be altered except to correct an error 
 - Historical data are useful for trend analysis and forecasting purposes to predict future results

       | Financial forecasting | Growth | Earnings |

#### Meta data: 

 - Metadata are data that define other data, for example, master data, transactional data, and reference data
 - Metadata are structured information labels that describe or characterize other data and make it easier to retrieve, interpret, manage, and use data. 

 - The purpose of metadata is to add value to the data they describe, and it is important for the effective usage of data. 
 - One of the common uses of metadata today is in e-commerce to target potential customers of products based on an analysis of their current preferences or behaviors.



   **Technical metadata:**
 - Technical metadata are data used to describe technical aspects and organization of the data stored in data repositories such 
 - as databases and file systems in an organization, and are used by technical teams to access and process the data. 
 - Examples of technical metadata include physical characteristics of the layers of data, such as:
 
       | Key information (PK FK)     | Column or field names | Allowed values | Indexes  | Field length | Constraints |
       | Relationship between tables | Validation rules      | Table names    | Lineage  | Data type    | 
 
 - **Business metadata:**  
 - Business metadata describe the functionality—nontechnical aspects of data and how data are used by the business—that adds 
   context and value to the data. 
 - Business metadata are not necessarily connected to the physical storage of data or requirements regarding data access. 
 - Groups responsible and accountable for the quality of data in a specific data field—the data owners and data stewards.
      
       | Field definitions         | Application screen names          | Privacy level      | Security level | 
       | Business rules            | Key performance indicators (KPIs) | Data quality rules | Business terms |
       | Report names and headings |
  
 - **Process metadata:**
 - **Audit trail metadata** are used for tracking security breaches and compliance issues, and forensic and litigation purposes. 
         
        | Timestamp | Description of the action ( Creation, Deletion, Modification, Printing) | 


 - Process metadata are used to describe the results of various IT operations that create and deliver the data:
  
       |(ETL) process | Data from tasks in the run-time environment | create, update, restore |otherwise access data |
       | Start time | End time | CPU seconds used | Disk reads | Source table read | Disk writes | Target table written |
       | Rows read from the target |Rows processed | Rows written to the target—are logged on execution | Case of errors | 
       | this sort of data helps in troubleshooting and getting to the bottom of the problem. Some|

---

| Free of defects | Desired features |
| ---             |        ---       |
| Correct         | Contextual       |
| Comppleted      | Pertinent        |
| Valid           | Comprehensive    |
| Reliable        | Easy to read     |
| Consistent      | Unambiguous      |
| Unique          | Easy to understand |
| Current         | Right level of detail |

---

### Causes of Bad Quality Data: 
 - Manual data entry 
 - Aging of data/data decay 
 - Inadequate validation in the data capture process 
 - Inefficient business process management and design Multiple uses of data and lack of shared understanding of data 
 - Lack of common data standards, data dictionary, and metadata 
 - Business data ownership and governance issues 
 - Loss of expertise
