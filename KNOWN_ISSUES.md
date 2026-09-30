# Beta limitations

- Windows x64 only. Microsoft WebView2 Runtime is required.
- Unsigned application and installer; Windows may show a publisher warning.
- Installation, upgrade, uninstall and offline use on a separate clean Windows
  machine have not been verified. Please report your Windows version and result.
- The import limit is 1 GiB per file. Large CSV/Excel inputs may exhaust memory.
- Use copies of source data and keep project backups during the beta.
- Updates are manual. Close the app before running a newer installer.
- Existing projects using the CSV Skip policy retain it. Select strict handling
  if you want malformed records to stop an import rather than be discarded.
- Downloads will only work once the GitHub prerelease is published.
