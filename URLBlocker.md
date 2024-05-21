```mermaid
flowchart TD
    Start --> Initialize("Load congfiguration file")
    Initialize --> Parse-command-line-options("Command Line Options")
    Parse-command-line-options --> GetConfigFile("Config file")
    GetConfigFile --> Download-blocklist("Check feedback"}
    Download-blocklist --> Download-fail("Feedback")
    Download-blocklist --> Correct-file("File loading")
    Correct-file --> Parse-merge("Parse and merge files")
    Parse-merge --> Regex("Extract domains")
    Regex --> CombineList("Append to list")
    Combinelist --> ModifiedHostFile("File Modified")
```
