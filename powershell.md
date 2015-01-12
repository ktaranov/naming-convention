# Powershell name convention


| Object    | Verb-Noun | Notation              | Length | Plural| Prefix | Suffix | Example             |
|-----------|-----------|-----------------------|--------|-------|--------|--------|---------------------|
| Cmdlet    | Yes       | PascalCase (for Noun) | 50     | No    | Yes    | No     | Import-PREFIXModule |
| Function  | Yes       | PascalCase (for Noun) | 50     | No    | Yes    | No     | Get-PREFIXDbRecord  |
| Parameter | No        | PascalCase            | 30     | No    | No     | No     | MyParameter         |
