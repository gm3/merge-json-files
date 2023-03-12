# merge-json-files

```Get-ChildItem -Filter *.json | ForEach-Object {Get-Content $_ | ConvertFrom-Json} | ConvertTo-Json -Depth 100 | Out-File -Encoding UTF8 -FilePath combined.json -Force
```
