# SQL Server 2012 Name Convention


## SQL Server Object Name
| Object                    | Notation   | Length | Plural | Prefix | Suffix | Abbreviation | Char Mask  | Example                          |
| ------------------------- | ---------- | ------ | ------ | ------ | ------ | ------------ | ---------- | -------------------------------- |
| Database                  | UPPERCASE  |     30 | No     | No     | No     | Yes          | [A-z]      | MYDATABASE                       |
| Database Trigger          | PascalCase |    128 | No     | DTR_   | No     | Yes          | [A-z]      | DTR_CheckLogin                   |
| Schema                    | lowercase  |     30 | No     | No     | No     | Yes          | [A-z][0-9] | myschema                         |
| Tempory Table Nam         | PascalCase |    118 | No     | No     | No     | Yes          | [A-z][0-9] | #MyTable                         |
| Table                     | PascalCase |     30 | No     | No     | No     | Yes          | [A-z][0-9] | MyTable                          |
| Table Default Values      | PascalCase |    128 | No     | DF_    | No     | Yes          | [A-z][0-9] | DF_MyTable_MyField               |
| Table Primary Key         | PascalCase |    128 | No     | PK_    | No     | Yes          | [A-z][0-9] | PK_MyTableID                     |
| Table Alternative Key     | PascalCase |    128 | No     | AK_    | No     | Yes          | [A-z][0-9] | AK_MyTable_MyField_AnotherFeild  |
| Table Foreign Key         | PascalCase |    128 | No     | FK_    | No     | Yes          | [A-z][0-9] | FK_MyTable_ForeignTableID        |
| Table Clustered Index     | PascalCase |    128 | No     | IXC_   | No     | Yes          | [A-z][0-9] | IXC_MyTable_MyField_AnotherFeild |
| Table Non Clustered Index | PascalCase |    128 | No     | IX_    | No     | Yes          | [A-z][0-9] | IX_MyTable_MyField_AnotherFeild  |
| Table Trigger             | PascalCase |    128 | No     | TR_    | No     | Yes          | [A-z][0-9] | TR_MyTable_UpdateCheck           |
| View                      | PascalCase |    128 | No     | VI_    | No     | No           | [A-z][0-9] | VI_LogicalName                   |
| Stored Procedure          | PascalCase |    128 | No     | usp_   | No     | No           | [A-z][0-9] | usp_LogicalName                  |
| User-Defined Functions    | PascalCase |    128 | No     | udf_   | No     | No           | [A-z][0-9] | udf_LogicalName                  |
| Synonim                   | CamelCase  |    128 | No     | sy_    | No     | No           | [A-z][0-9] | sy_logicalName                   |

                                                                           
## Offical Reference
 - [Database object TECHNET] (Limitations)
 - [User-Defined Functions MSDN]
 - [Synonim TECHNET]
 
[Database object TECHNET]:http://technet.microsoft.com/en-us/library/ms172451%28v=sql.110%29.aspx
[User-Defined Functions MSDN]:http://msdn.microsoft.com/en-us/library/ms191007.aspx
[Synonim TECHNET]:http://technet.microsoft.com/en-us/library/ms187552(v=sql.110).aspx
