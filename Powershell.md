# Powershell name convention


## Powershell object name
| Object    | Verb-Noun | Notation              | Length | Plural| Prefix | Suffix | Example             |
|-----------|-----------|-----------------------|--------|-------|--------|--------|---------------------|
| Cmdlet    | Yes       | PascalCase (for Noun) | 50     | No    | Yes    | No     | Import-PREFIXModule |
| Function  | Yes       | PascalCase (for Noun) | 50     | No    | Yes    | No     | Get-PREFIXDbRecord  |
| Parameter | No        | PascalCase            | 30     | No    | No     | No     | MyParameter         |


## Useful Links
 - [MSDN Development Guidelines]
 - [MSDN Approved Verbs]

[MSDN Development Guidelines]:https://msdn.microsoft.com/en-us/library/dd878270%28v=vs.85%29.aspx
[MSDN Approved Verbs]:https://msdn.microsoft.com/en-us/library/ms714428%28v=vs.85%29.aspx
