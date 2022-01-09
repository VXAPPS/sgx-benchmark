# SGX Benchmark
Intel SGX Benchmark.

## Systems
Find all detailed information from dmidecode and test-sgx under *system* folder.

### Nuc NUC7PJYH (SGX1 & SGX2)
- Pentium Silver J5005 CPU @ 1.50GHz
- 8 GB RAM @ 2400 MHz

- Ubuntu 20.04
- Intel DCAP driver 1.41
- PSW 2.15.1
- EPC section in Processor Reserved Memory, 94 M

### Dell Precision 5750 (SGX1)
- Xeon W-10885M CPU @ 2.40GHz
- 64 GB ECC RAM @ 2667 MHz

- Ubuntu 20.04
- Intel DCAP driver 1.41
- PSW 2.15.1
- EPC section in Processor Reserved Memory, 93 M

### HP (SGX1)
- Xeon E5-1234G @ 111 GHz
- 32 GB RAM @ 2667 MHz

- RHEL8.5
- Intel DCAP driver 1.41
- PSW 2.15.1
- EPC section in Processor Reserved Memory, 93 M

### SuperMicro X12SPM-TF (SGX1 & SGX2)
- Xeon Gold 5315Y CPU @ 3.20GHz
- 512 GB ECC RAM @ 2667 MHz

- Ubuntu 20.04
- Intel DCAP driver 1.41
- PSW 2.15.1
- EPC section in Processor Reserved Memory, 65144 M

## Benchmarks
Benchmarks are time-based. The tests run 1.000 times, and the average is used for this document. The tests run in release mode without mitigation of CVE-2020-0551.

Find the complete running data inside *data* folder and the code inside *code* folder.

### Enclave Size
Run different sized enclaves by 1,000 iterations.

##### Overall

##### 1 MB Enclave
Pentium Silver J5005: 0,03 seconds
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 0,01 seconds
Less is better.

##### 10 MB Enclave
Pentium Silver J5005: 0,1 seconds
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 0,03 seconds
Less is better.

##### 80 MB Enclave
Inside SGX1 processor available memory. So this is mostly the last value, which will not swap EPC pages.

Pentium Silver J5005: 0,65 seconds
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 0,18 seconds
Less is better.

##### 100 MB Enclaves
Pentium Silver J5005: 1,2 seconds
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 0,22 seconds
Less is better.

##### 1 GB Enclaves
Pentium Silver J5005: 13,25 seconds
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 1,88 seconds
Less is better.

##### 10 GB Enclaves
Pentium Silver J5005: Not enough memory. But will swap to disk and will execute in about 57 minutes.
Xeon W-10885M:  seconds
Xeon Gold 5315Y: 18,56 seconds
Less is better.
