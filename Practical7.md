# Practical 7: Privacy-Enhancing Technologies (PETs)

## Aim

To study different Privacy-Enhancing Technologies (PETs), understand their working principles, and analyze how they can reduce privacy risks while allowing organizations to use data for legitimate purposes.

---

## Introduction

**Privacy-Enhancing Technologies (PETs)** are technologies and methods that help organizations use and process information while reducing unnecessary exposure of personal data.

Traditional security mainly focuses on preventing unauthorized access. PETs go one step further by reducing the amount of personal information that needs to be exposed even during legitimate data processing.

PETs are useful in:

* Online education
* Healthcare
* Banking
* Artificial Intelligence
* Cloud computing
* Digital identity
* Data analytics
* Research

---

# Major Privacy-Enhancing Technologies

## 1. Encryption

Encryption converts readable information (**plaintext**) into an unreadable form (**ciphertext**) using a cryptographic key.

```text
Plaintext
    ↓
Encryption + Key
    ↓
Ciphertext
```

Only an authorized party with the appropriate key can decrypt the information.

### Examples

* AES
* RSA
* TLS/HTTPS

### Uses

* Protecting login credentials
* Securing communication
* Protecting stored personal information

---

## 2. Tokenization

**Tokenization** replaces sensitive information with a randomly generated token.

```text
Original Data
     ↓
Tokenization
     ↓
Random Token
```

Example:

```text
Student ID: STU2026456
        ↓
Token: TKN_8F42X91
```

The token does not directly reveal the original information. The original value is kept separately in a protected system.

### Uses

* Payment systems
* Student databases
* Customer databases
* Healthcare systems

### Benefit

If a tokenized database is exposed, the attacker does not automatically obtain the original sensitive information.

---

## 3. Pseudonymization

Pseudonymization replaces direct identifiers with artificial identifiers.

Example:

```text
Name: Rahul Sharma
       ↓
Pseudonymous ID: USER_1045
```

Unlike complete anonymization, the original identity may still be recovered when additional information is available.

### Uses

* Research
* Data analytics
* User behavior analysis
* Internal enterprise systems

---

## 4. Anonymization

Anonymization modifies or removes identifying information so that an individual cannot reasonably be identified from the resulting dataset.

Example:

```text
Before:

Name       Age   City
Rahul      21    Delhi
Aman       22    Delhi

After:

Age Group    Region
20-25        North India
20-25        North India
```

### Uses

* Statistical reports
* Academic research
* Public datasets
* Population analysis

---

## 5. Differential Privacy

**Differential Privacy** is a mathematical technique that introduces carefully controlled randomness into query results or statistical analysis.

```text
Private Dataset
       ↓
Differential Privacy Mechanism
       ↓
Noise Added
       ↓
Statistical Result
```

The goal is to make it difficult to determine whether a particular individual's information was included in the dataset.

### Example

Instead of reporting:

```text
Exactly 1,254 students used the platform.
```

a privacy-preserving statistical system may release a slightly perturbed aggregate value.

### Uses

* Statistical analysis
* Public reports
* Large-scale data analytics
* Machine learning datasets

---

## 6. Federated Learning

**Federated Learning** allows machine-learning models to be trained across multiple devices or organizations without directly collecting all raw training data in one central location.

```text
Device A ──┐
Device B ──┼──→ Model Updates ──→ Central Model
Device C ──┘
```

The raw data remains closer to where it was generated.

### Uses

* Mobile applications
* Healthcare
* Personalized applications
* Privacy-sensitive AI systems

### Advantage

It can reduce the need to transfer raw personal data to a central server.

---

## 7. Homomorphic Encryption

Homomorphic Encryption allows certain mathematical operations to be performed on encrypted information.

```text
Original Data
      ↓
Encryption
      ↓
Encrypted Data
      ↓
Computation on Encrypted Data
      ↓
Encrypted Result
      ↓
Decryption
      ↓
Final Result
```

The processing system can perform supported computations without directly seeing the plaintext.

### Uses

* Secure cloud computing
* Healthcare analytics
* Financial calculations
* Sensitive data processing

### Limitation

Homomorphic encryption can require significant computational resources depending on the scheme and operation.

---

## 8. Secure Multi-Party Computation (SMPC)

**Secure Multi-Party Computation** allows multiple parties to jointly calculate a result without directly revealing their private input to one another.

Example:

```text
Company A ── Private Data ──┐
                            ├──→ Secure Computation
Company B ── Private Data ──┘
                                      ↓
                              Shared Result
```

Neither organization needs to directly reveal its complete private dataset to the other party.

### Uses

* Joint research
* Financial analysis
* Healthcare research
* Cross-organization analytics

---

## 9. Trusted Execution Environment (TEE)

A **Trusted Execution Environment** is a protected area of a computer's processor where sensitive code and data can be processed with additional hardware-based isolation.

```text
        Application
             ↓
   +-------------------+
   | Trusted Execution |
   |    Environment    |
   |                   |
   | Sensitive Data    |
   | Sensitive Code    |
   +-------------------+
             ↓
       Secure Result
```

### Uses

* Cloud computing
* Secure authentication
* Confidential data processing
* Protection of cryptographic keys

---

## 10. Zero-Knowledge Proofs

A **Zero-Knowledge Proof (ZKP)** allows one party to prove that a statement is true without revealing the underlying secret information.

### Example

A user wants to prove:

> "I am above the required age."

Instead of revealing their complete date of birth, a ZKP-based system could allow them to prove the required condition without revealing the exact birth date.

### Uses

* Digital identity
* Privacy-preserving authentication
* Blockchain applications
* Access-control systems

---

# PET Comparison

| PET                        | Main Privacy Objective                            | Example Use                 |
| -------------------------- | ------------------------------------------------- | --------------------------- |
| **Encryption**             | Protect information from unauthorized access      | HTTPS                       |
| **Tokenization**           | Replace sensitive data with tokens                | Payment systems             |
| **Pseudonymization**       | Hide direct identifiers                           | Data analytics              |
| **Anonymization**          | Reduce the possibility of identifying individuals | Research datasets           |
| **Differential Privacy**   | Protect individuals in statistical analysis       | Usage statistics            |
| **Federated Learning**     | Keep raw training data decentralized              | Privacy-preserving AI       |
| **Homomorphic Encryption** | Perform computations on encrypted data            | Cloud analytics             |
| **SMPC**                   | Compute jointly without exposing private inputs   | Multi-organization analysis |
| **TEE**                    | Protect data while it is being processed          | Confidential computing      |
| **Zero-Knowledge Proofs**  | Prove information without revealing the secret    | Digital identity            |

---

# PETs in an Online Coding Platform

Consider an online coding platform such as **LeetCode** that processes user profiles, coding submissions, performance statistics, and platform-usage information.

Different PETs could be applied to different activities:

### Encryption

Used to protect information while it travels between the user's browser and the server.

### Tokenization

Internal systems could use tokens instead of directly exposing sensitive identifiers during selected processing activities.

### Pseudonymization

User IDs can be replaced with pseudonymous identifiers when performing internal analytics.

### Differential Privacy

Aggregate statistics such as participation trends could be released with privacy protection so individual users are harder to identify.

### Federated Learning

If personalized machine-learning models were developed across multiple user devices, federated learning could reduce the need to centralize raw training data.

### Zero-Knowledge Proofs

A future identity system could allow users to prove specific eligibility conditions without revealing unnecessary personal information.

### Synthetic Data

Synthetic datasets could be used during software development and testing instead of exposing real users' information.

---

# New PET: Synthetic Data

**Synthetic data** is artificially generated data designed to reproduce useful characteristics of real datasets without directly copying real individuals' records.

Example:

```text
Real Student Data
       ↓
Data Generation Process
       ↓
Synthetic Dataset
       ↓
Software Testing / Research
```

For example, developers can test an analytics application using synthetic student records instead of real student information.

### Benefits

* Reduces exposure of real personal data
* Useful for software testing
* Useful for development environments
* Can support research and experimentation

### Limitation

Synthetic data must be carefully generated and evaluated because it can still create privacy risks if it closely reproduces identifiable characteristics of real individuals.

---

# Selecting the Appropriate PET

Different privacy problems require different technologies.

| Privacy Problem                                   | Suitable PET                    |
| ------------------------------------------------- | ------------------------------- |
| Data transmitted over the Internet                | Encryption                      |
| Sensitive identifier exposed internally           | Tokenization / Pseudonymization |
| Publishing statistics                             | Differential Privacy            |
| Training AI without centralizing raw data         | Federated Learning              |
| Processing encrypted information                  | Homomorphic Encryption          |
| Joint analysis between organizations              | SMPC                            |
| Protecting data during computation                | TEE                             |
| Proving a condition without revealing information | Zero-Knowledge Proof            |
| Testing software without real user data           | Synthetic Data                  |
| Publishing datasets for research                  | Anonymization                   |

---

# Benefits of PETs

PETs can provide the following benefits:

* Reduce unnecessary exposure of personal information.
* Minimize privacy risks during data processing.
* Support privacy-preserving analytics.
* Reduce the need to share raw personal data.
* Improve user confidence.
* Support privacy-by-design.
* Enable organizations to perform useful computations while limiting access to sensitive information.

---

# Limitations of PETs

PETs are not a complete replacement for traditional security controls.

Some limitations include:

1. **Computational cost** – Some technologies such as homomorphic encryption can require significant processing resources.
2. **Implementation complexity** – Advanced PETs require specialized technical knowledge.
3. **Accuracy trade-offs** – Techniques such as differential privacy can introduce noise into results.
4. **Key management** – Encryption requires secure management of cryptographic keys.
5. **Configuration risks** – Poorly configured privacy mechanisms may provide insufficient protection.
6. **Scalability** – Some advanced privacy technologies can become difficult to operate at very large scale.
7. **No universal solution** – Different PETs address different privacy threats.

---

# Recommendations

* Select PETs according to the data type and threat model.
* Use encryption for sensitive information in transit and at rest.
* Use tokenization or pseudonymization where direct identifiers are unnecessary.
* Apply differential privacy when releasing aggregate statistics.
* Consider federated learning when raw training data should remain decentralized.
* Use SMPC when multiple organizations need to perform joint analysis.
* Consider homomorphic encryption for appropriate privacy-sensitive computations.
* Use synthetic data during development and testing where appropriate.
* Combine PETs with authentication, authorization, access control, and monitoring.
* Regularly evaluate the effectiveness and performance of deployed PETs.

---

# Result

Different Privacy-Enhancing Technologies were studied and their applications, benefits, and limitations were analyzed. Technologies including **encryption, tokenization, anonymization, pseudonymization, differential privacy, federated learning, homomorphic encryption, secure multi-party computation, trusted execution environments, zero-knowledge proofs, and synthetic data** were examined.

---

# Conclusion

Privacy-Enhancing Technologies provide technical mechanisms for reducing privacy risks while allowing organizations to continue using data for legitimate purposes.

Different PETs solve different problems. **Encryption** protects data from unauthorized access, **differential privacy** protects individuals in statistical analysis, **federated learning** reduces the need to centralize raw training data, while **SMPC, homomorphic encryption, TEEs, and zero-knowledge proofs** provide more advanced methods for privacy-preserving computation and verification.

PETs should be combined with traditional security practices such as access control, authentication, secure software development, data minimization, and monitoring.

Therefore, PETs are an important part of a **privacy-by-design approach** to modern software and data-processing systems.

---

# References

1. NIST Privacy Framework – https://www.nist.gov/privacy-framework
2. NIST Privacy-Enhancing Cryptography – https://csrc.nist.gov/projects/pec
3. NIST Cryptography – https://www.nist.gov/cryptography
4. NIST Differential Privacy – https://www.nist.gov/itl/applied-cybersecurity/privacy-engineering
5. LeetCode Privacy Policy – https://leetcode.com/privacy/
