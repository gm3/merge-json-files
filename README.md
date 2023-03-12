# merge-json-files

This command uses the ConvertTo-Json cmdlet with the -Depth parameter set to 100 to ensure that nested objects are fully expanded in the output. The -Encoding parameter is set to UTF8 to ensure that the output file is properly encoded, and the -Force parameter is added to overwrite any existing file with the same name.

The resulting JSON file will have proper formatting, including indentation and line breaks for readability.


```
Get-ChildItem -Filter *.json | ForEach-Object {Get-Content $_ | ConvertFrom-Json} | ConvertTo-Json -Depth 100 | Out-File -Encoding UTF8 -FilePath combined.json -Force
```
