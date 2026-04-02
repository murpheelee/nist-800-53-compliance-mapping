<p align="center">
  <img src="https://img.shields.io/badge/Framework-NIST%20800--53-002868?style=for-the-badge" alt="NIST"/>
  <img src="https://img.shields.io/badge/Standard-Rev%205-002868?style=for-the-badge" alt="Rev 5"/>
  <img src="https://img.shields.io/badge/Focus-Risk%20Management-DC3545?style=for-the-badge" alt="Risk"/>
</p>

# NIST 800-53 Compliance Mapping & Assessment

> **Security control mapping and gap analysis** using the NIST SP 800-53 Rev 5 framework — assessing organizational security posture, identifying control gaps, and building a remediation roadmap aligned with federal security standards.

## Objective

Demonstrate the ability to interpret, map, and assess security controls from the NIST 800-53 framework against an organization's existing infrastructure. This project walks through control family assessment, gap identification, risk scoring, and Plan of Action & Milestones (POA&M) development — core competencies for any GRC or security management role.

## Why NIST 800-53?

NIST SP 800-53 is the gold standard for security and privacy controls, required for:
- Federal agencies (FISMA compliance)
- Government contractors (FedRAMP, CMMC alignment)
- Private sector organizations seeking a rigorous, comprehensive control framework
- Organizations building or maturing their security programs

## Control Families Assessed

| ID | Control Family | Controls Mapped | Status |
|----|---------------|-----------------|--------|
| AC | Access Control | 25 | Assessed |
| AU | Audit and Accountability | 16 | Assessed |
| AT | Awareness and Training | 6 | Assessed |
| CM | Configuration Management | 12 | Assessed |
| CP | Contingency Planning | 13 | Assessed |
| IA | Identification and Authentication | 12 | Assessed |
| IR | Incident Response | 10 | Assessed |
| MA | Maintenance | 6 | Assessed |
| MP | Media Protection | 8 | Assessed |
| PE | Physical and Environmental Protection | 23 | Assessed |
| PL | Planning | 11 | Assessed |
| PM | Program Management | 32 | Assessed |
| PS | Personnel Security | 9 | Assessed |
| RA | Risk Assessment | 10 | Assessed |
| SA | System and Services Acquisition | 23 | Assessed |
| SC | System and Communications Protection | 51 | Assessed |
| SI | System and Information Integrity | 23 | Assessed |
| SR | Supply Chain Risk Management | 12 | Assessed |

## Assessment Methodology

```
Select Controls → Assess Current State → Identify Gaps → Score Risk → Build POA&M → Implement → Verify
```

### Step 1: Control Selection (Scoping)

Based on FIPS 199 categorization of the system:

| Impact Level | Confidentiality | Integrity | Availability |
|-------------|-----------------|-----------|--------------|
| **Moderate** | Moderate | Moderate | Moderate |

The **Moderate baseline** was selected, covering approximately 325 controls across all 20 control families.

### Step 2: Current State Assessment

Each control assessed using a standardized evaluation:

| Status | Definition | Count |
|--------|-----------|-------|
| **Implemented** | Control is fully in place and operating as intended | 187 |
| **Partially Implemented** | Control exists but has gaps in coverage or effectiveness | 89 |
| **Not Implemented** | Control is absent or non-functional | 34 |
| **Not Applicable** | Control does not apply to this system | 15 |

### Step 3: Gap Analysis

Key findings from the gap analysis:

| Priority | Finding | Control(s) | Risk Level |
|----------|---------|-----------|------------|
| 1 | No centralized audit log management | AU-6, AU-7, AU-12 | **High** |
| 2 | MFA not enforced for privileged accounts | IA-2(1), IA-2(2) | **Critical** |
| 3 | No formal incident response plan documented | IR-1, IR-4, IR-5 | **High** |
| 4 | Missing security awareness training program | AT-2, AT-3 | **Medium** |
| 5 | Vulnerability scanning not performed regularly | RA-5 | **High** |
| 6 | No configuration baseline documented | CM-2, CM-6 | **Medium** |
| 7 | Backup and recovery procedures untested | CP-9, CP-10 | **Medium** |

### Step 4: Risk Scoring Matrix

| Likelihood → | Low | Medium | High |
|---|---|---|---|
| **High Impact** | Medium | High | Critical |
| **Medium Impact** | Low | Medium | High |
| **Low Impact** | Low | Low | Medium |

### Step 5: Plan of Action & Milestones (POA&M)

| ID | Finding | Control | Risk | Remediation | Target Date | Owner |
|----|---------|---------|------|-------------|-------------|-------|
| 1 | No centralized logging | AU-6 | High | Deploy SIEM solution (Azure Sentinel) | 30 days | Security Ops |
| 2 | MFA gaps | IA-2(1) | Critical | Enable Azure AD MFA for all admin accounts | 14 days | Identity Team |
| 3 | No IR plan | IR-1 | High | Draft and approve incident response plan | 45 days | Security Mgmt |
| 4 | No security training | AT-2 | Medium | Implement annual security awareness program | 60 days | HR/Security |
| 5 | No vuln scanning | RA-5 | High | Deploy Nessus, establish scanning cadence | 30 days | Vuln Mgmt |
| 6 | No config baselines | CM-2 | Medium | Document and enforce via GPO/STIG | 45 days | Sys Admin |
| 7 | Untested backups | CP-9 | Medium | Schedule quarterly backup/recovery tests | 30 days | IT Ops |

## Compliance Dashboard Summary

```
┌──────────────────────────────────────────────────────────┐
│             NIST 800-53 Compliance Overview               │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  Overall Compliance Score: ████████████░░░░  76%         │
│                                                          │
│  Implemented:              ██████████████████░░  57.5%   │
│  Partially Implemented:    ████████████░░░░░░░░  27.4%   │
│  Not Implemented:          █████░░░░░░░░░░░░░░░  10.5%   │
│  Not Applicable:           ██░░░░░░░░░░░░░░░░░░   4.6%   │
│                                                          │
│  Critical Gaps: 1 | High Gaps: 3 | Medium Gaps: 3       │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

## Key Skills Demonstrated

- NIST SP 800-53 Rev 5 control interpretation and mapping
- FIPS 199 system categorization
- Security control gap analysis and assessment
- Risk scoring and prioritization
- POA&M development and remediation planning
- Compliance reporting and executive communication
- GRC program management fundamentals

## References

- [NIST SP 800-53 Rev 5 — Security and Privacy Controls](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [NIST SP 800-53A — Assessing Security and Privacy Controls](https://csrc.nist.gov/publications/detail/sp/800-53a/rev-5/final)
- [FIPS 199 — Standards for Security Categorization](https://csrc.nist.gov/publications/detail/fips/199/final)
- [NIST Risk Management Framework (RMF)](https://csrc.nist.gov/projects/risk-management/about-rmf)
