# Fuzzing 

“Fuzzing” technique to test the security and vulnerabilities of crypto libraries in Android applications.
The tools used for fuzzing in this lecture include
1.	OSS-Fuzz: Continuous Fuzzing Service for Open Source Software
2.	ClusterFuzz: Scalable Fuzzing Infrastructure
3.	FuzzBench: Fuzzer benchmarking as a service


which are automated processes used by Google for open-source projects.
Fuzzing involves testing the behaviour and vulnerabilities of functions by manipulating inputs, such as strings or images.
These are all common fuzzing tools, but we will be discussing the CDF (crypto differential fuzzing) tool.
CDF (crypto differential fuzzing)
CDF is a tool to automatically test the correctness and security of cryptographic software. CDF can detect implementation errors, compliance failures, side-channel leaks, and so on. CDF implements a combination of unit tests with "differential fuzzing", an approach that compares the behaviour of different implementations of the same primitives when fed edge cases and values maximizing the code coverage.
Unlike general-purpose fuzzers and testing software, CDF is:
•	Smart: CDF knows what kind of algorithm it's testing and adapts to the tested functions.
•	Fast: CDF tests only what needs to be tested and parallelizes its tests as much as possible.
•	Polyvalent: CDF isn't specific to any language or API, but supports arbitrary executable programs or scripts.
•	Portable: CDF will run on any Unix or Windows platform, since it is written in Go without any platform-specific dependencies.
 
Installation
The purpose of CDF is to provide more efficient testing tool to developers and security researchers, being more effective than test vectors and cheaper than manual audit of formal verification.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/883e5370-44e7-4f39-aa87-4c90dc3a0a71)


Then enter the command in the terminal:
git clone https://github.com/kudelskisecurity/cdf.git
![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/45365d49-0d07-429f-8e01-f2d81a631320)


First build the cdf binary.
![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/d414ff57-a458-4ad6-ad6c-816d385e1c9a)

Command: make examples-all will build all the examples.
 
While make examples-go will only build the Go examples.
![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/b2ec47c3-a16d-4d02-9e6e-d1d362ff5574)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/2fde25e9-ee0f-4f33-a7ad-28609906b8b8)

make test will run unit tests (of CDF).

We may want to view usage info by running cdf -h

We may then try an example such as the rsaenc interface against the RSA OAEP Go and CryptoPP examples.

Viewing CryptoPP as our reference, you can test the Go implementation by doing:
cdf rsaenc /examples/oaep_rsa2048_go /examples/oaep_rsa2048_cryptopp

This command will perform various tests specific to the rsaenc interface.
 
 ![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/77d45e11-76f4-4f70-b6f8-5bbed457c558)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/29203625-0aa5-41a6-b016-3a4f76bae950)


In this example, CDF should complain about the maximum public exponent size the Go implementation support.
If we check its code we can see the public exponent is being stored as a normal integer, whereas in CryptoPP (and most other implementations), it is stored as a big integer.
This is however by design and will likely not be changed.
