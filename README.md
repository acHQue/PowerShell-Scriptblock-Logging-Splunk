# PowerShell-Scriptblock-Logging-Splunk

https://sites.google.com/view/powershell-scriptblock-splunk/home

Bellow is the regex - i can see gtihub removong sysntax though, like the * from squence number.


|            Field           |                                         REGEX                                        |
|:--------------------------:|:------------------------------------------------------------------------------------:|
| ActivityID                 | ^(?:[^'\n]*'){9}(?P<ActivityID>[^']+)                                                |
| Channel-PowerShell         | (?:Channel>)(?<Channel>.*)(?:<\/Channel)                                             |
| Command_Name-PowerShell    | (?:Command Name =)(?<Command_Name>.*)(?:Command Type)                                |
| Command_Path-PowerShell    | (?:Command Path =)(?<Command_Path>.*)(?:Sequence Number)                             |
| Command_Type-PowerShell    | (?:Command Type =)(?<Command_Type>.*)(?:Script Name)                                 |
| Computer-PowerShell        | (?:Computer>)(?<Computer>.*)(?:<\/Computer)                                         |
| Connected_User-PowerShell  | (?<=Connected User   =)(?<Connected_User>.*)(?=Shell ID =)                          |
| Engine_Version             | (?:Engine Version =)(?<Engine_Version>.*)(?:Runspace ID)                             |
| EventID                    | ^(?:[^>\n]*>){4}(?P<EventID>\d+)                                                    |
| EventRecordID              | (?i)<EventRecordID>(?P<EventRecordID>[^<]+)                                         |
| ExecutionProcessID         | ^(?:[^'\n]*'){11}(?P<ExecutionProcessID>[^']+)                                       |
| Guid-powershell            | (?i)   Guid='(?P<Guid>[^']+)                                                        |
| Host-Version-PowerShell    | (?:Host Version =)(?<Version>.*)(?:Host ID)                                          |
| Host_Application           | (?:Host Application   =)(?<Host_Application>.*)(?:Engine)                           |
| Host_ID                    | (?:Host ID =)(?<Host_ID>.*)(?:Host Application)                                      |
| Level                      | ^(?:[^>\n]*>){8}(?P<Level>\d+)                                                       |
| Opcode-PowerShell          | (?:Opcode>)(?<Opcode>.*)(?:<\/Opcode)                                                |
| Payload-PowerShell         | (?:Payload'>)(?<Payload>.*)(?:<\/Data)(?:.*)(?:Data)                             |
| Pipeline_ID-Powershell     | (?:Pipeline ID   =)(?<Pipeline_ID>.*)(?:Command Name)                               |
| ProviderName               | (?i) Name='(?P<ProviderName>[^']+)                                                   |
| Runspace_ID                | (?:Runspace ID   =)(?<Runspace_ID>.*)(?:Pipeline)                                   |
| Script_Name-PowerShell     | (?:Script Name   =)(?<Script_Name>.*)(?:Command Path)                               |
| Sequence_Number-PowerShell | (?:Sequence Number   =)(?<Sequence_Number>.*)(?=User =)(?:.*)(?=Connected User =)  |
| Shell_ID-PowerShell        | (?:Shell ID =)(?<Shell_ID>.*)(?=\/Data)(?:.*)(?=Data)(?:.*)(?=Name)(?:.*)(?=<Data)  |
| Systemtime_PowerShell      | (?i)SystemTime='(?P<SystemTime>[^']+)                                               |
| Task_PowerShell            | (?i)<Task>(?P<Task>[^<]+)                                                           |
| Thread_ID-PowerShell       | ^(?:[^=\n]*=){7}'(?P<ThreadID>\d+)                                                  |
| User-PowerShell            | (?:User =)(?<User>.*)(?=Connected User =)                                           |
| UserID-PowerShell          | (?:UserID=')(?<UserID>.*)(?:'\/)                                                    |
| User_Data-PowerShell       | (?:UserData'>)(?<User_Data>.*)(?:<\/Data)(?:.*)(?:Payload)                          |
| Version-PowerShell         | ^(?:[^>\n]*>){6}(?P<Version>\d+)                                                    |
