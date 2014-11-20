# SQL Server 2012 Name Convention


## Table names

| SQL Server Object Name    | Notation   | Length | Plural | Prefix | Suffix | Abbreviation | Char Mask               |
| ------------------------- | ---------- | ------ | ------ | ------ | ------ | ------------ | ------------------------|
| Database                  | UPPERCASE  |    100 | None   | None   | None   | Yes          | [A-z]                   |
| Database Trigger          | PascalCase |    128 | None   | DTR_   | None   | Yes          | [DATABASENAME_ACTION]   |
| Schema Name               | lowercase  |    100 | None   | None   | None   | Yes          | [A-z][0-9]              |
| Table Name                | PascalCase |    100 | None   | None   | None   | Yes          | [A-z][0-9]              |
| Table Default Values      | PascalCase |    128 | None   | DF_    | None   | Yes          | [TableName]             |
| Table Primary Key         | PascalCase |    128 | None   | PK_    | None   | Yes          | [TableName_ColumnName1] |
| Table Alternative Key     | PascalCase |    128 | None   | AK_    | None   | Yes          | [TableName_ColumnName1] |
| Table Foreign Key         | PascalCase |    128 | None   | FK_    | None   | Yes          | [TableName_ColumnName1] |
| Table Clustered Index     | PascalCase |    128 | None   | IXC_   | None   | Yes          | [TableName_ColumnName1] |
| Table Non Clustered Index | PascalCase |    128 | None   | IX_    | None   | Yes          | [TableName_ColumnName1] |
| Table Trigger             | PascalCase |    128 | None   | TR_    | None   | Yes          | [TableName_Action]      |
| View                      | PascalCase |    128 | None   | VI_    | None   | Yes          | [TableName_Purpose]     |
| Stored Procedure          | PascalCase |    128 | None   | usp_   | None   | Yes          | [Action]                |
| User-Defined Functions    | PascalCase |    128 | None   | udf_   | None   | Yes          | [Action]                |


## Offical Reference
 - [Database object TECHNET] (Limitations)
 - [User-Defined Functions MSDN]
 
 [Database object TECHNET]:http://technet.microsoft.com/en-us/library/ms172451%28v=sql.110%29.aspx
 [User-Defined Functions MSDN]:http://msdn.microsoft.com/en-us/library/ms191007.aspx
