# Demo Script – Identity Security GRC Copilot

## Scenario: Enterprise Identity Security Risk Analysis

---

## Step 1 – Overall Identity Security Posture

User:
"What are the main identity security risks in our environment?"

Expected Agent Response:

Risk Level: CRITICAL

Top Findings:

1. Missing MFA enforcement
   - Impact: High likelihood of credential compromise
   - Reason: Weak authentication controls across users
   - Why #1 priority: Affects large portion of users and enables direct account takeover
   - Exploitation Scenario:
     - Password spray attacks
     - MFA fatigue attacks
   - Framework Mapping:
     CIS: Enforce MFA
     ISO: Access Control / Authentication
     Zero Trust: Verify explicitly

2. Legacy authentication enabled
   - Impact: Bypass of modern security controls
   - Exploitation Scenario:
     - Credential stuffing attacks
   - Framework Mapping:
     CIS: Disable legacy auth
     ISO: Access Control
     Zero Trust: Assume breach

3. Privileged accounts exposure
   - Impact: Full tenant compromise potential
   - Exploitation:
     - Privilege escalation attacks
   - Framework Mapping:
     CIS: Least privilege enforcement
     ISO: Access Control
     Zero Trust: Least privilege

Patterns Observed:
- Systemic MFA gaps
- Weak Conditional Access enforcement
- Overexposed privileged identities

---

## Step 2 – MFA Coverage Analysis

User:
"Do we have any gaps in MFA enforcement?"

Expected Agent Response:

MFA Coverage Analysis:

- Current MFA coverage: 72%
- Estimated unprotected users: ~3,200

Risk Assessment:
- High exposure to identity-based attacks
- Weak authentication posture

Exploitation Scenario:
- Password spray attacks targeting weak accounts
- MFA fatigue attacks on push-based authentication

Framework Impact:
- CIS violation: MFA not enforced
- ISO gap: Authentication controls
- Zero Trust violation: Verify explicitly

Business Impact:
- Increased probability of unauthorized access
- Potential lateral movement inside environment

---

## Step 3 – ISO 27001 Compliance Evaluation

User:
"Are we compliant with ISO 27001?"

Expected Agent Response:

ISO 27001 Compliance Status:

- Overall Status: NON-COMPLIANT

Key Gaps:
- Lack of MFA enforcement (Authentication control failure)
- Weak access control for privileged accounts
- Missing monitoring for risky sign-ins

Affected Domains:
- Access Control
- Authentication
- Monitoring and Logging

Compliance Risk Level: HIGH

Reasoning:
- Authentication controls are not consistently enforced
- Privileged access is not properly restricted
- Detection capabilities for identity threats are limited

---

## Step 4 – Conditional Access & Policy Weaknesses

User:
"What issues exist in Conditional Access?"

Expected Agent Response:

Conditional Access Analysis:

Key Issues:
- Missing policies for privileged users
- No enforcement of device compliance
- Weak authentication strength requirements
- Excessive policy exclusions

Risk Impact:
- Increased attack surface
- Lack of protection for sensitive accounts

Zero Trust Impact:
- Violates "Verify explicitly"
- Fails to enforce adaptive access controls

---

## Step 5 – Attack Scenario Simulation

User:
"What attacks are possible in this environment?"

Expected Agent Response:

Threat Scenarios:

1. Password Spray Attack
   - Enabled by weak or missing MFA
   - Targets large number of user accounts

2. MFA Fatigue Attack
   - Exploits push-based MFA methods
   - User can be tricked into approving access

3. Token Theft / Session Hijacking
   - Attackers reuse stolen session tokens
   - Bypasses authentication entirely

4. Privilege Escalation
   - Compromise of admin accounts leads to full control

Business Impact:
- Unauthorized access to sensitive data
- Data exfiltration
- Full tenant compromise (worst-case scenario)

---

## Step 6 – Impact Simulation

User:
"What happens if we fix these issues?"

Expected Agent Response:

Impact Simulation:

If MFA is enforced:
- Reduces credential-based attacks dramatically
- Eliminates majority of unauthorized access attempts

If Conditional Access is strengthened:
- Reduces attack surface
- Improves access control precision

If privileged access is secured (PIM):
- Limits blast radius of compromised accounts
- Prevents lateral movement

Overall Result:
- Significant reduction in identity-related risk
- Improved compliance posture
- Strong alignment with Zero Trust principles

---

## Step 7 – Recommendations

User:
"What should we fix first?"

Expected Agent Response:

Priority Actions:

1. Enforce MFA for all users and privileged accounts
2. Disable legacy authentication protocols
3. Implement Conditional Access policies for high-risk scenarios
4. Introduce Privileged Identity Management (PIM)
5. Reduce policy exclusions and enforce device compliance

High-Impact Outcome:
- Immediate reduction of identity attack risk
- Improved compliance (ISO / CIS)
- Stronger Zero Trust posture
