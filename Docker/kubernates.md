# Installation Kubernates

Download the latest 1.30 patch release: kubectl 1.30.0.

Or if you have curl installed, use this command:

> curl.exe -LO "https://dl.k8s.io/release/v1.30.0/bin/windows/amd64/kubectl.exe"

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/2e0ad7bf-6efe-46de-a19a-432f595061d7)

> curl.exe -LO "https://dl.k8s.io/v1.30.0/bin/windows/amd64/kubectl.exe.sha256"

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/1fcd7e7a-209c-4b7c-8a19-bf69cbcbbda0)

> CertUtil -hashfile kubectl.exe SHA256
> type kubectl.exe.sha256

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/b1b50055-d069-486d-a108-3dc85921370d)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/82f12f6b-0b3b-4a1c-a864-a0ff2ce8bd7a)

Test to ensure the version of kubectl is the same as downloaded:

> kubectl version --client

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/beb300cf-190d-4730-b72f-d09dbfbf77b3)

Installing Minicube 

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/757de741-9169-45c3-8e84-1df2630c5b96)

starting at its file location 
> minicube.exe start

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/684b8c5c-495a-4672-94bc-1d0e3331dd88)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/e2060e3c-682f-4884-8442-7522f815b8b2)
