```mermaid
flowchart TD
    Start --> Initialize("Load configuration file")
    Initialize --> Parse-command-line-options("Command Line Options")
    Parse-command-line-options --> GetConfigFile("Config file")
    GetConfigFile --> Download-blocklist("Check feedback")
    Download-blocklist --> Download-fail("Download Fail")
    Download-blocklist --> Correct-file("File loading")
    Download-fail --> GetConfigFile
    Correct-file --> Parse-merge("Parse and merge files")
    Parse-merge --> Regex("Extract domains")
    Regex --> CombineList("Append to list")
    CombineList --> ModifiedHostFile("File Modified")
    ModifiedHostFile --> ("Execute") 
```
