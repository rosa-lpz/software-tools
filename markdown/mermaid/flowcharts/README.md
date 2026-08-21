
# Flowcharts
# Example - SQL

## Code
```bash
flowchart TB
    SQL["SQL<br/>Structured Query Language"]
SQL --> DDL["DDL<br/>Data Definition Language"]
SQL --> DML["DML<br/>Data Manipulation Language"]
SQL --> DQL["DQL<br/>Data Query Language"]
SQL --> DCL["DCL<br/>Data Control Language"]
SQL --> TCL["TCL<br/>Transaction Control Language"]

DDL --> DDL_C["CREATE<br/>ALTER<br/>DROP<br/>TRUNCATE<br/>RENAME"]

DML --> DML_C["INSERT<br/>UPDATE<br/>DELETE<br/>MERGE"]

DQL --> SELECT["SELECT"]

SELECT --> FROM["FROM"]
FROM --> WHERE["WHERE"]
WHERE --> LOGIC["AND / OR / NOT"]

SELECT --> GROUP["GROUP BY"]
GROUP --> HAVING["HAVING"]

SELECT --> ORDER["ORDER BY"]
SELECT --> DISTINCT["DISTINCT"]
SELECT --> JOIN["JOIN"]

DCL --> DCL_C["GRANT<br/>REVOKE"]

TCL --> TCL_C["COMMIT<br/>ROLLBACK<br/>SAVEPOINT"]

classDef sql fill:#1d4ed8,color:white,stroke:#1e3a8a,stroke-width:3px
classDef category fill:#7c3aed,color:white,stroke:#5b21b6,stroke-width:2px
classDef command fill:#f3f4f6,color:#111,stroke:#6b7280
classDef logic fill:#fef3c7,color:#92400e,stroke:#d97706,stroke-width:2px

class SQL sql
class DDL,DML,DQL,DCL,TCL category
class DDL_C,DML_C,SELECT,FROM,WHERE,GROUP,HAVING,ORDER,DISTINCT,JOIN,DCL_C,TCL_C command
class LOGIC logic

```

## Flowchart
```mermaid
flowchart TB
    SQL["SQL<br/>Structured Query Language"]
SQL --> DDL["DDL<br/>Data Definition Language"]
SQL --> DML["DML<br/>Data Manipulation Language"]
SQL --> DQL["DQL<br/>Data Query Language"]
SQL --> DCL["DCL<br/>Data Control Language"]
SQL --> TCL["TCL<br/>Transaction Control Language"]

DDL --> DDL_C["CREATE<br/>ALTER<br/>DROP<br/>TRUNCATE<br/>RENAME"]

DML --> DML_C["INSERT<br/>UPDATE<br/>DELETE<br/>MERGE"]

DQL --> SELECT["SELECT"]

SELECT --> FROM["FROM"]
FROM --> WHERE["WHERE"]
WHERE --> LOGIC["AND / OR / NOT"]

SELECT --> GROUP["GROUP BY"]
GROUP --> HAVING["HAVING"]

SELECT --> ORDER["ORDER BY"]
SELECT --> DISTINCT["DISTINCT"]
SELECT --> JOIN["JOIN"]

DCL --> DCL_C["GRANT<br/>REVOKE"]

TCL --> TCL_C["COMMIT<br/>ROLLBACK<br/>SAVEPOINT"]

classDef sql fill:#1d4ed8,color:white,stroke:#1e3a8a,stroke-width:3px
classDef category fill:#7c3aed,color:white,stroke:#5b21b6,stroke-width:2px
classDef command fill:#f3f4f6,color:#111,stroke:#6b7280
classDef logic fill:#fef3c7,color:#92400e,stroke:#d97706,stroke-width:2px

class SQL sql
class DDL,DML,DQL,DCL,TCL category
class DDL_C,DML_C,SELECT,FROM,WHERE,GROUP,HAVING,ORDER,DISTINCT,JOIN,DCL_C,TCL_C command
class LOGIC logic

```


# Example - SQL 2

```mermaid
flowchart LR
    SQL["SQL<br/>Structured Query Language"]
SQL --> DDL["DDL<br/>Data Definition"]
SQL --> DML["DML<br/>Data Manipulation"]
SQL --> DQL["DQL<br/>Data Query"]
SQL --> DCL["DCL<br/>Data Control"]
SQL --> TCL["TCL<br/>Transaction Control"]

DDL --> DDL_C["CREATE<br/>ALTER<br/>DROP<br/>TRUNCATE<br/>RENAME"]

DML --> DML_C["INSERT<br/>UPDATE<br/>DELETE<br/>MERGE"]

DQL --> SELECT["SELECT"]

SELECT --> FROM["FROM"]
SELECT --> WHERE["WHERE"]
WHERE --> LOGIC["AND<br/>OR<br/>NOT"]

SELECT --> GROUP["GROUP BY"]
SELECT --> HAVING["HAVING"]
SELECT --> ORDER["ORDER BY"]
SELECT --> DISTINCT["DISTINCT"]
SELECT --> JOIN["JOIN"]

DCL --> DCL_C["GRANT<br/>REVOKE"]

TCL --> TCL_C["COMMIT<br/>ROLLBACK<br/>SAVEPOINT"]

classDef sql fill:#2563eb,color:#fff,stroke:#1e40af,stroke-width:3px
classDef category fill:#7c3aed,color:#fff,stroke:#5b21b6,stroke-width:2px
classDef command fill:#f3f4f6,color:#111,stroke:#6b7280
classDef logic fill:#fef3c7,color:#92400e,stroke:#d97706,stroke-width:2px

class SQL sql
class DDL,DML,DQL,DCL,TCL category
class DDL_C,DML_C,SELECT,FROM,WHERE,GROUP,HAVING,ORDER,DISTINCT,JOIN,DCL_C,TCL_C command
class LOGIC logic

```

# Example - Database

```mermaid
graph TD
    %% Layer 1: Bronze (Raw)
    subgraph Bronze_Layer [Source Data]
        RAW_STK[(Raw_Stock_Levels)]
        RAW_TRX[(Raw_Transactions)]
    end

    %% Layer 2: Silver (Cleaning)
    subgraph Silver_Layer [Data Cleaning]
        CLN_STK[Clean: Handle NULLs & Unit Conversions]
        CLN_TRX[Clean: Format Dates & Remove Duplicates]
    end

    %% Layer 3: Gold (Business Logic)
    subgraph Gold_Layer [Analytics Ready]
        JOIN_DATA{SQL JOIN}
        CALC_METRICS[Calculate: Inventory Turnover Ratio]
    end

    %% Final Output
    FINAL_VIEW{{V_Inventory_Health_Dashboard}}

    %% Relationships
    RAW_STK --> CLN_STK
    RAW_TRX --> CLN_TRX
    CLN_STK --> JOIN_DATA
    CLN_TRX --> JOIN_DATA
    JOIN_DATA --> CALC_METRICS
    CALC_METRICS --> FINAL_VIEW
```
