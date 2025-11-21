# 🔑 Task 6: Password Strength Evaluation and Best Practices

## Task Objective
The objective was to understand the technical factors contributing to a strong password (entropy), evaluate multiple password variations using professional tools, and synthesize best practices for creating secure, resilient passwords.

## 🛠 Tool Used
* **Online Password Strength Checkers:** Used to provide real-time metrics (e.g., complexity score, time to crack).

## 📊 Password Evaluation Results

The evaluation tested three password types: a weak dictionary word, a complex but common pattern, and a long, high-entropy passphrase.

| Password Category | Example Format | Complexity Score (Low/Med/High) | Estimated Crack Time | Lessons Learned |
| :--- | :--- | :--- | :--- | :--- |
| **Weak (Dictionary)** | `password123` | **Low** | Instantaneous | Easily defeated by **Dictionary Attacks** and common patterns. |
| **Medium (Complex Pattern)** | `P@$$w0rd!2025` | **Medium** | Seconds to Minutes | Meets most complexity rules but is still vulnerable due to **Substitutions** (`@` for `a`, `0` for `o`). |
| **Strong (Passphrase)** | `Correct-Horse-Battery-Staple` | **High** | Centuries / Infinite | Long length greatly increases **Entropy**, defeating brute-force attacks effectively. |


## 💡 Best Practices for Password Creation

The evaluation demonstrated that security relies on **unpredictability** and **length** rather than simple substitutions.

### 1. Prioritize Length Over Complexity
* **Recommendation:** Use **passphrases** (e.g., three or more random, unrelated words) rather than short, complex passwords. A phrase like `RedTruckBlueLamp` has higher entropy than `R3dTrck!`.
* **Reasoning:** Increasing the length by just one character can exponentially increase the time required for a **brute-force attack**.

### 2. Maximize Character Space (Complexity)
* **Recommendation:** While length is key, combine **uppercase, lowercase, numbers, and symbols** (a high **character space**) to make dictionary and guessing attacks impossible.
* **Reasoning:** This prevents **dictionary attacks** and requires the attacker to check a much larger set of possibilities.

### 3. Avoid Common Substitutions
* **Recommendation:** Do not use common substitutions like `@` for 'a', `$` for 's', or `0` for 'o', as these are included in modern **rule-based attacks** (hybrid attacks).

### 4. Implement Unique Passwords
* **Recommendation:** Use a **Password Manager** to store and generate a unique, highly complex password for every account.
* **Reasoning:** This prevents a single compromise (like the phishing attempt analyzed in Task 2) from leading to an **Account Takeover** across multiple platforms.

## 🔬 Password Attack Mechanisms

The goal of a strong password is to resist these common attack methods:

* **Brute-Force Attack:** Systematically trying every possible combination of letters, numbers, and symbols until the correct password is found. **Strong passwords defeat this by increasing the time required to an astronomical figure (e.g., thousands of years).**
* **Dictionary Attack:** Using a large list of words, phrases, and common passwords (including pattern variations like "password123!") to gain access quickly. **Strong passphrases composed of unrelated words defeat this.**
* **Credential Stuffing:** Using stolen username/password combinations from one data breach to try and log into other services (due to password reuse).

---

## 📈 Summary: Complexity and Security

Password **complexity** and **length** directly translate to cryptographic strength, a metric known as **Entropy** (measured in bits).

{Entropy} = L \times \log_2(C)

Where $L$ is the **Length** of the password, and $C$ is the size of the **Character Set** used.

The evaluation confirmed that maximizing both $L$ (Length) and $C$ (Character Set/Complexity) is the most effective security control against automated password guessing and brute-force attacks. A high-entropy password ensures that the computational effort required to crack it exceeds the attacker's resources and time limits.
