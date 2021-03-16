# Security Challenge 2 (60 pts.)

Your second challenge will be around [OWASP Benchmark](https://owasp.org/www-project-benchmark/), a Java test suite for evaluating the accuracy, coverage, and speed of automated software vulnerability detection tools. OWASP Benchmark is designed as an open source web application with thousands of exploitable test cases, each mapped to specific [CWEs](https://cwe.mitre.org/). Some test cases are truly vulnerable/expoloitable and others are not.

In this challenge, pick 10 truly vulnerable test cases of your choice, provided that they map to different CWEs. 

## Vulnerability Identification and Analysis (30 pts.)
For each test case:
1. Specify the corresponding CWE(s) (10 x 0.5 pts)
2. Analyze the source code and explain in details the root cause of the weakness (10 x 2 pts)
3. Specify the threatened security requirement(s) (10 x 0.5 pts)

## Exploit Design and Penetration Testing (30 pts.)
Install and run OWASP Benchmark (You may want to use docker). Pick 3 out of the 10 already chosen test cases and For each:
1. Handcraft and describe a corresponding exploit (3 x 5 pts)
2. Test your exploit and describe the outcome (3 x 5 pts)
