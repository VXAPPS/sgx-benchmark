# SGX Benchmark
Intel SGX Benchmark.

## Systems
1.
Intel NUC7PJYH
Pentium Silver J5005 CPU @ 1.50GHz
8 GB RAM

Ubuntu 20.04
Intel DCAP driver
EPC section in Processor Reserved Memory, 94 M

2.
Dell Precision 5750
Xeon W-10885M CPU @ 2.40GHz
64 GB ECC RAM

Ubuntu 22.04
Driver from Kernel 5.13
EPC section in Processor Reserved Memory, 93 M

3.
HP
Xeon E5-1234G
128 MB Enclave Memory
32 GB RAM
RHEL8.5
Intel DCAP driver

4.
SuperMicro X12SPM
Xeon Gold 5318Y
64 GB Enclave Memory
512 GB ECC RAM
Ubuntu 22.04
Driver from Kernel 5.13

Find all detailed information from dmidecode and test-sgx under *system* folder.

## Benchmarks
Benchmark are time-based. The tests runs 1.000 times and the mid-time is used for this document. The tests are runned in release-mode with mitigations of CVE-2020-0551 and without.

All systems run with PSW 2.15.1.

Find the complete running data inside *data* folder.

### Enclave Size
Run an empty enclave by 1,000 iterations.

Find the code under source/enclave_size.

#### 1 MB Enclave
TDB

#### 10 MB Enclave
TDB

#### 100 MB Enclaves
TDB

#### 1 GB Enclaves
TDB

#### 10 GB Enclaves
TDB
