Define your SOC-style prompt:

$prompt = @"
You are a SOC analyst. Analyze the following Windows Sysmon and Security logs.
Tasks:
1. Summarize suspicious activity
2. Map to MITRE ATT&CK techniques
3. Extract IOCs
4. Rate severity
"@


Combine logs + prompt:

$inputData = $prompt + "`n--- Logs Start ---`n" + (Get-Content D:\SysmonLogs\clean_logs.txt -Raw) + "`n--- Logs End ---"


Run through Ollama:

$inputData | ollama run mistral | Out-File D:\SysmonLogs\ollama_output.txt -Encoding utf8
notepad D:\SysmonLogs\ollama_output.txt
