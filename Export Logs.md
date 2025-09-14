Export Sysmon + Security logs into a single text file:

# Sysmon logs
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 20 |
  ForEach-Object { "{0} | {1} | {2}" -f $_.TimeCreated, $_.Id, $_.Message } |
  Out-File D:\SysmonLogs\clean_logs.txt -Encoding utf8

# Security logs
Get-WinEvent -LogName "Security" -MaxEvents 20 |
  ForEach-Object { "{0} | {1} | {2}" -f $_.TimeCreated, $_.Id, $_.Message } |
  Out-File D:\SysmonLogs\clean_logs.txt -Append -Encoding utf8
