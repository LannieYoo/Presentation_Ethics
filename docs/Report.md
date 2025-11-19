# Ethical AI Impact Assessment for the City of Ottawa GenAI Internal Research Tool

**Team Members:** Member1, Member2, Member3, Member4  
**Application Area:** Internal GenAI research and summarization tool for municipal staff  
**Date:** November 15, 2025

---

## Table of Contents

1. [Project Overview and Objectives](#1-project-overview-and-objectives) - **Member1**
2. [System Background and Technical Context](#2-system-background-and-technical-context) - **Member2**
3. [Stakeholder Mapping](#3-stakeholder-mapping) - **Member2**
4. [Data Flow and Sensitive Information](#4-data-flow-and-sensitive-information) - **Member2**
5. [Ethical Risk Analysis](#5-ethical-risk-analysis) - **Member3**
6. [Risk Register Summary](#6-risk-register-summary) - **Member3**
7. [Regulatory and Policy Context](#7-regulatory-and-policy-context) - **Member3**
8. [Ethical Tools and Mitigation Strategies](#8-ethical-tools-and-mitigation-strategies) - **Member4**
9. [Governance Workflow and Accountability](#9-governance-workflow-and-accountability) - **Member4**
10. [Recommendations and Guidelines](#10-recommendations-and-guidelines) - **Member4**
11. [Conclusion](#11-conclusion) - **Member1**
12. [References](#12-references) - *(Not presented)*

---

## 1. Project Overview and Objectives

**Primary Responsibility:** *Member1*

### 1.1 Project Description

The City of Ottawa GenAI Internal Research Tool is a large language model system using Retrieval-Augmented Generation (RAG) technology. It supports municipal staff in conducting research, policy analysis, and drafting internal reports by querying municipal documents in natural language and receiving synthesized answers with citations.

### 1.2 Problems Being Solved

- **Inefficient Information Retrieval:** Manual searching through lengthy municipal documents is time-consuming
- **Knowledge Accessibility:** Institutional knowledge is distributed across many documents and systems
- **Research Speed:** Policy analysts need faster access to relevant information for decision-making
- **Consistency:** Standardizing how staff access and reference municipal policies

### 1.3 Main Ethical Questions

1. How can the City protect privacy and confidentiality of municipal records when using GenAI systems?
2. What measures are needed to prevent bias and ensure equitable representation in AI-assisted policy analysis?
3. How can the system ensure verifiability and accountability when AI-generated content influences municipal decisions?
4. What governance mechanisms are necessary to maintain transparency and public trust?

---

## 2. System Background and Technical Context

**Primary Responsibility:** *Member2*

### 2.1 System Architecture

The system uses **LLM + RAG architecture**:
- **Data Ingestion:** Municipal documents (council minutes, policy manuals, briefings) are collected and indexed
- **Retrieval:** Semantic search locates relevant paragraphs/documents from the secure index
- **Generation:** LLM generates answers based on retrieved municipal resources with citations

### 2.2 Key Technical Features Influencing Ethics

- **Retrieval and Indexing:** Coverage decisions affect bias - underrepresented communities/policy areas will be systematically overlooked
- **Prompt Controls:** System prompts influence how the model handles uncertainty and points to sources
- **Access Controls:** Role-based permissions and query logging determine who can access what information
- **Model Lifecycle:** LLM updates can alter behavior without obvious signals to users

---

## 3. Stakeholder Mapping

**Primary Responsibility:** *Member2*

### 3.1 Key Stakeholder Groups

**Internal Stakeholders:**
- **Primary Users:** Policy analysts, planners, project managers, frontline staff
- **Compliance Teams:** Legal counsel, ATIP officers, corporate security
- **Technical Teams:** IT, Data, and Innovation team
- **Leadership:** Senior management, elected officials

**External Stakeholders:**
- **Ottawa Residents:** Affected by policies developed with AI assistance
- **Community Organizations:** Monitor fairness, transparency, service quality
- **Regulatory Bodies:** Information and Privacy Commissioner of Ontario, provincial regulators
- **Vendors:** Cloud service providers and model suppliers

### 3.2 Distribution of Benefits and Risks

**Primary Beneficiaries:**
- Policy analysts and IT teams gain efficiency and easier access to knowledge
- Senior leadership benefits from faster reporting and positive image

**Higher Risk Bearers:**
- Residents and community groups bear privacy risks, misinformation, and biased analysis consequences
- Frontline workers face surveillance and work pressures if AI outputs become performance benchmarks
- Compliance officers have limited influence over technical design despite responsibility for violations

---

## 4. Data Flow and Sensitive Information

**Primary Responsibility:** *Member2*

### 4.1 Data Flow Process

1. **Data Ingestion:** Municipal documents collected and imported into secure index
2. **Storage:** Documents stored in versioned system within city's secure environment
3. **RAG Processing:** Semantic search retrieves relevant excerpts, ranked and assembled with user query
4. **User Interaction:** LLM generates answers with citations; queries/responses may be logged

### 4.2 Sensitive Information Types

- **Personal Information:** Resident data (names, addresses), employee records, contractor information
- **Confidential Municipal Records:** Internal policy drafts, legal advice, financial information, security documents
- **Business Information:** Proprietary vendor data, economic development negotiations

### 4.3 Privacy Concerns

Under **MFIPPA** (Municipal Freedom of Information and Protection of Privacy Act), personal information must be protected from unauthorized use or disclosure. Risks exist at multiple layers:
- **Document Storage:** Indexed content may contain sensitive information
- **Retrieval Layer:** Retrieved documents may expose information beyond authorized scope
- **Interaction Logs:** Questions and responses may contain personal or sensitive information

---

## 5. Ethical Risk Analysis

**Primary Responsibility:** *Member3*

### 5.1 Privacy and Confidentiality Risks

**Risk Description:** Employee queries may inadvertently leak sensitive information or circumvent traditional "need-to-know" boundaries, allowing personal information to be searchable beyond authorized scope.

**Scenario:** A policy analyst queries "affordable housing eligibility criteria in downtown Ottawa." The system retrieves internal reports containing personal information about specific residents who applied for housing assistance. The analyst, who should not have access under normal controls, can now see resident names, addresses, and application details.

**Impact:** Privacy rights violations, compliance risks, loss of public trust, legal liability under MFIPPA

### 5.2 Bias and Inequitable Policy Impacts

**Risk Description:** GenAI systems inherit patterns from historically biased data. Decision support systems trained on biased data often replicate or amplify inequalities, even without explicit sensitive attributes.

**Scenario:** The indexed corpus contains disproportionately high reports on certain neighborhoods. When an analyst queries "areas requiring urban planning attention," the tool consistently flags these same neighborhoods as "problem areas," overlooking communities with similar needs but less historical documentation.

**Impact:** Underrepresented communities further overlooked, less equitable resource allocation, biased outcomes disguised as "neutral insights," erosion of citizen trust

### 5.3 Hallucinations, Verifiability, and Accountability

**Risk Description:** LLMs frequently generate fluent yet false statements with high confidence. This structural feature poses danger in law and public policy where references must be precise and verifiable.

**Scenario:** An analyst queries "zoning requirements for mixed-use development." The system generates a confident summary with a specific bylaw citation. The analyst uses this in a memo to city council, but the citation is incorrect and criteria are outdated, potentially leading to incorrect policy decisions.

**Impact:** Compromised decision accuracy, eroded trust in municipal expertise, legal liability, difficulty assigning responsibility due to LLM opacity

### 5.4 Transparency and Explainability

**Risk Description:** The opacity of large language models complicates transparency and public trust. When residents are affected by decisions made through opaque models, accountability becomes difficult.

**Impact:** Undermined citizen confidence, difficult to challenge or appeal decisions, compliance challenges with public sector accountability expectations

---

## 6. Risk Register Summary

**Primary Responsibility:** *Member3*

### Priority Risks (High Likelihood/Impact)

| Risk ID | Risk Description | Likelihood | Impact |
|---------|------------------|------------|--------|
| R4 | Hallucinated information presented as factual | High | High |
| R3 | Bias in policy recommendations due to unrepresentative data | High | Medium |
| R5 | Over-reliance on AI outputs (automation bias) | High | Medium |
| R1 | Unauthorized access to personal information through AI queries | Medium | High |
| R2 | Privacy breach through data retention in LLM or logs | Medium | High |

**Key Findings:**
- Highest priority: Hallucinated information (High/High) - LLMs structurally prone to false but confident statements
- High likelihood risks: Bias and automation bias reflect systematic human-AI interaction patterns
- High impact privacy risks: Unauthorized access and data retention violate MFIPPA requirements

---

## 7. Regulatory and Policy Context

**Primary Responsibility:** *Member3*

### 7.1 Key Regulations

**MFIPPA (Municipal Freedom of Information and Protection of Privacy Act):**
- Municipal authorities must provide access to records AND protect personal information
- System must enforce access controls consistent with MFIPPA requirements
- Query logs and interaction records must comply with privacy protection standards

**AODA (Accessibility for Ontarians with Disabilities Act):**
- System interface must be accessible to users with disabilities
- Generated content should be accessible and understandable

**City of Ottawa Internal Policies:**
- ATIP office oversees privacy obligations
- System design must align with municipal data protection policies

### 7.2 Regulatory Impact on Design

- **Access Control Design:** Must respect "need-to-know" boundaries, prevent circumvention through AI queries
- **Data Minimization:** Only necessary personal information should be indexed; logging minimized and anonymized
- **Transparency Requirements:** Documentation, audit trails, mechanisms for challenging AI-assisted decisions

---

## 8. Ethical Tools and Mitigation Strategies

**Primary Responsibility:** *Member4*

### 8.1 Fairness Audits with Aequitas

**Tool:** Aequitas - open-source bias auditing toolkit calculating group fairness metrics

**Application:** Audit structured outputs (e.g., "high priority" classifications, "problem area" flags) alongside demographic/geographic metadata

**Mitigates:** Bias in policy recommendations (R3), Over-reliance on AI outputs (R5)

**Limitations:** Requires structured outputs; audits are retrospective; surrogate metrics may not capture all fairness dimensions

### 8.2 Interpretability Workflows with LIME

**Tool:** LIME (Local Interpretable Model-agnostic Explanations) - provides localized explanations

**Application:** Display which input paragraphs/terms contributed to outputs, with links to original records

**Mitigates:** Hallucinated information (R4), Lack of transparency (R6), Over-reliance (R5), Bias (R3)

**Limitations:** Local explanations may be unstable; increases computational overhead; may be misinterpreted as guarantees

### 8.3 Differential Access Controls and Logging

**Strategy:** Role-based access controls varying by document sensitivity; differential logging (minimal for low-risk, detailed for high-risk)

**Mitigates:** Unauthorized access (R1), Privacy breach through retention (R2), Hallucinated information (R4)

**Limitations:** May reduce system utility if too restrictive; logging creates its own privacy concerns

### 8.4 Human-in-the-Loop Review

**Strategy:** Mandatory human review for high-risk outputs (eligibility determinations, sensitive communities, policy recommendations)

**Mitigates:** Hallucinated information (R4), Over-reliance on AI (R5), Bias (R3), Unauthorized access (R1)

**Limitations:** May reduce efficiency gains; requires training and clear guidelines; reviewers may still exhibit automation bias

---

## 9. Governance Workflow and Accountability

**Primary Responsibility:** *Member4*

### 9.1 Governance Workflow

**Data Review and Approval:**
- Data governance team, ATIP officers, and legal counsel review before adding datasets
- Privacy impact assessment for datasets containing personal information

**Model Updates:**
- IT team, data governance team, senior management approve changes
- Ethical and privacy impact assessments, testing, staged deployment

**Monitoring and Incident Handling:**
- Continuous monitoring of access patterns and query logs
- Incident response team (IT, legal, privacy officers) responds to breaches, bias issues, errors

**Escalation Paths:**
- Technical issues: User → IT Support → IT Lead → Senior Management
- Privacy concerns: User → ATIP Officer → Privacy Commissioner → Legal Counsel
- Bias/fairness: User → Data Governance → Equity Office → Senior Management

### 9.2 Accountability Roles

- **System Owners (IT Team):** Technical implementation, infrastructure security, performance
- **Data Protection Officers (ATIP Office):** Privacy compliance, access control enforcement, breach response
- **Policy Owners (Department Managers):** Appropriate use, verification of AI outputs, final responsibility for recommendations
- **End Users:** Understanding limitations, verifying critical information, reporting errors
- **Senior Management:** Strategic direction, final accountability, legal/financial liability

---

## 10. Recommendations and Guidelines

**Primary Responsibility:** *Member4*

### 10.1 High-Priority, Must-Do Actions

**Data and Access Governance:**
1. Enforce role-based permissions at retrieval layer and user interface
2. Classify all indexed corpora according to MFIPPA-based access rules
3. Minimize logging, anonymize where feasible, implement strict retention limits
4. Complete privacy and algorithmic impact assessments before major deployments

**System and Model Design:**
1. Limit retrieval to curated, versioned municipal corpora
2. Include source citations in all responses, display uncertainty/confidence metrics
3. Integrate LIME-style explanations for critical queries
4. Conduct regular fairness audits using Aequitas for structured outputs

**Human Oversight:**
1. Require verification against source records before using AI outputs in official recommendations
2. Mandate explicit approval workflows for high-risk use cases
3. Provide comprehensive training on privacy obligations, bias concepts, explanation interpretation

### 10.2 Recommended Improvements

- Implement automated monitoring of access patterns and query types
- Develop Model Cards and System Cards documenting capabilities, limitations, risks
- Establish regular review cycles (monthly usage patterns, quarterly fairness audits, annual assessments)
- Create channels for user feedback and reporting problematic outputs

---

## 11. Conclusion

**Primary Responsibility:** *Member1*

### 11.1 Summary of Key Findings

The City of Ottawa GenAI Internal Research Tool offers significant advantages in efficiency, institutional memory preservation, and evidence-based policy-making. However, three primary ethical concerns require attention:

1. **Privacy and Confidentiality:** System processes sensitive municipal records requiring robust access controls and privacy protection to comply with MFIPPA
2. **Bias and Representational Issues:** AI-assisted analysis may perpetuate inequalities if historical data reflects biases
3. **Hallucination and Accountability:** LLMs prone to false but confident statements, creating risks when outputs influence policy decisions

Stakeholder analysis shows efficiency gains concentrated among internal staff and management, while residents and frontline workers disproportionately bear privacy risks and consequences of biased/erroneous analysis.

### 11.2 Critical Requirements

At the municipal level, these issues directly impact legal compliance, distributive justice, and democratic legitimacy. The City cannot treat this as a one-off innovation project but must manage it as an ongoing socio-technical system with:
- Continuous monitoring of privacy safeguards and equity metrics
- Clear remediation pathways when harm occurs
- Multi-layered technical, organizational, and procedural safeguards

### 11.3 Final Recommendations

To leverage GenAI while fulfilling obligations to protect rights, ensure accountability, and maintain public trust, the City must:
1. Implement comprehensive data and access governance as highest priority
2. Design system safeguards preventing bias, ensuring transparency, enabling verification
3. Establish human oversight workflows treating GenAI as decision support, not decision-maker
4. Create clear accountability structures across all roles
5. Maintain continuous monitoring and improvement processes

---

## 12. References

**Note:** References section is not included in the presentation.

Amazon Web Services. (n.d.). What is RAG (retrieval-augmented generation)? AWS. https://aws.amazon.com/what-is/retrieval-augmented-generation/

Microsoft. (n.d.). Retrieval augmented generation (RAG) in Azure AI Search. Microsoft Learn. https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview

Municipal Freedom of Information and Protection of Privacy Act, R.S.O. 1990, c. M.56 (Ontario). https://www.ontario.ca/laws/statute/90m56

Information and Privacy Commissioner of Ontario. (2014). Ontario's Municipal Freedom of Information and Protection of Privacy Act: A mini guide. https://www.ipc.on.ca/sites/default/files/legacy/Resources/municipal%20guide-e.pdf

Carlini, N., Tramèr, F., Wallace, E., Jagielski, M., Herbert-Voss, A., Lee, K., Roberts, A., Brown, T., Song, D., Erlingsson, U., Oprea, A., & Raffel, C. (2021). Extracting training data from large language models. In 30th USENIX Security Symposium (USENIX Security 21). https://www.usenix.org/system/files/sec21-carlini-extracting.pdf

Carlini, N. (2020, December 15). Privacy considerations in large language models. Google Research Blog. https://research.google/blog/privacy-considerations-in-large-language-models/

City of Ottawa. (n.d.). Access to information and protection of privacy. https://ottawa.ca/en/city-hall/open-transparent-and-accountable-government/access-information-and-protection-privacy

The Greenlining Institute. (2021). Algorithmic bias explained: How automated decision-making becomes automated discrimination. https://greenlining.org/wp-content/uploads/2021/04/Greenlining-Institute-Algorithmic-Bias-Explained-Report-Feb-2021.pdf

Krištofík, A. (2025). Bias in AI (supported) decision making: Old problems, new technologies. International Journal for Court Administration. https://doi.org/10.36745/ijca.598

Alon-Barkat, S., & Busuioc, M. (2023). Human–AI interactions in public sector decision making: "Automation bias" and "selective adherence" to algorithmic advice. Journal of Public Administration Research and Theory, 33(1), 153-169. https://doi.org/10.1093/jopart/muac007

Ada Lovelace Institute. (2021). Algorithmic accountability for the public sector: Learning from the first wave of policy implementation. https://www.adalovelaceinstitute.org/report/algorithmic-accountability-public-sector/

Dahl, M., Magesh, V., Suzgun, M., & Ho, D. E. (2024). Large legal fictions: Profiling legal hallucinations in large language models. Journal of Legal Analysis, 16(1), 64–93. https://doi.org/10.1093/jla/laae003

Government of Canada. (2025). Algorithmic impact assessment tool. https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai/algorithmic-impact-assessment.html

Saleiro, P., Kuester, B., Hinkson, L., London, J., Stevens, A., Anisfeld, A., Rodolfa, K. T., & Ghani, R. (2018). Aequitas: A bias and fairness audit toolkit. arXiv. https://arxiv.org/abs/1811.05577

Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). "Why should I trust you?": Explaining the predictions of any classifier. In Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (pp. 1135–1144). https://doi.org/10.1145/2939672.2939778

---

## Appendix: Team Responsibilities for Presentation

**Presentation Duration:** 15-20 minutes total

This report is organized to support team presentations where each member presents their assigned sections:

- **Member1:** Sections 1 (Project Overview and Objectives) and 11 (Conclusion) - Introduction and Conclusion
  - Approximately 2 sections, opening and closing of presentation
  
- **Member2:** Sections 2 (System Background), 3 (Stakeholder Mapping), and 4 (Data Flow and Sensitive Information)
  - Approximately 3 sections covering system architecture, stakeholders, and data privacy
  
- **Member3:** Sections 5 (Ethical Risk Analysis), 6 (Risk Register Summary), and 7 (Regulatory and Policy Context)
  - Approximately 3 sections covering ethical risks, risk prioritization, and regulatory framework
  
- **Member4:** Sections 8 (Ethical Tools and Mitigation Strategies), 9 (Governance Workflow), and 10 (Recommendations)
  - Approximately 3 sections covering mitigation tools, governance, and actionable recommendations

**Note:** Section 12 (References) is not included in the presentation. Full reference list may appear on final slide if required by citation guidelines.
