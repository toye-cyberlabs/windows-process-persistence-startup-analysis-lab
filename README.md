# windows-process-persistence-startup-analysis-lab
Windows Process Persistence &amp; Startup Analysis Lab
Overview

This lab focused on identifying persistence mechanisms on a Windows system using built-in administrative tools. The objective was to understand how attackers maintain access and how defenders detect unauthorized startup entries.

Tools Used:

	•	tasklist
  <img width="1366" height="768" alt="P18_4" src="https://github.com/user-attachments/assets/50b888bb-3c7f-4c19-8491-c11cfba71d51" />

	•	wmic startup get caption,command
  <img width="1366" height="768" alt="P18_!" src="https://github.com/user-attachments/assets/54713025-7bd5-494e-961e-21ac9309bced" />

	•	reg query HKCU\Software\Microsoft\Windows\CurrentVersion\Run
  <img width="1365" height="768" alt="P18_3" src="https://github.com/user-attachments/assets/1af8d601-440b-4749-9043-bcaf353bdf4e" />

	•	sc query state= all
  <img width="1366" height="768" alt="P18_2" src="https://github.com/user-attachments/assets/c72af366-19bd-4dad-a00f-7661c459f5b1" />


Key Findings:

	•	10 startup programs identified.
	•	GoogleDriveF5 configured in registry Run key.
	•	70+ Windows services enumerated.
	•	Java Update Scheduler (jusched.exe) running.

Security Insight

Persistence is a critical phase in post-exploitation. Attackers use startup mechanisms to survive reboots and maintain access. Monitoring registry Run keys, services, and startup entries is essential for detecting compromise.

Defensive Recommendation:

	•	Implement EDR monitoring.
	•	Audit startup entries regularly.
	•	Restrict administrative privileges.
	•	Monitor service creation events.

Skills Demonstrated:

	•	Windows process enumeration
	•	Registry inspection
	•	Service analysis
	•	Persistence detection
	•	Security triage methodology
  
