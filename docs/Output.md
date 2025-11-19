Ethical AI Impact Assessment Site

City of Ottawa GenAI Internal Research Tool

This markdown is for Cursor.

Goal

Turn the submitted report into a small one page or multi page ethics project site.

Navigation menus follow the teacher guide and the team work plan, so each member has a clear presentation section.

Main navigation structure

Menu Home  Project overview and summary  presenter  all members

Menu System  System overview and technical context  presenters  Huaqing Zheng  Jiaxing Yi

Menu Risks  Ethical issues and risk register  presenter  Jiaxing Yi

Menu Stakeholders  Stakeholder mapping and distribution of benefits and risks  presenters  Hye Ran Yoo  Peng Wang

Menu Tools  Ethical tools and mitigation strategies  presenters  Hye Ran Yoo  Peng Wang

Menu Governance  Data access governance and workflow recommendations  presenters  Hye Ran Yoo  Peng Wang  all members

Menu Conclusion  Overall findings and significance  presenter  all members

Menu References  Reference list in APA format  presenter  all members

Home  overview and summary  all members

Section id home

Page purpose

Short project landing section that explains what the tool is and why ethics matters.

Content source

Use the Summary section from Report docx.

Content outline

Heading

Ethical AI Impact Assessment for the City of Ottawa GenAI Internal Research Tool

Paragraphs

Explain that the tool is an internal GenAI research and summarization system for municipal staff, built with LLM and retrieval augmented generation.

Mention that staff can ask questions over municipal documents and receive synthesized answers and citations.

Highlight why ethical assessment is needed

handling sensitive municipal information

risks around privacy and confidentiality

risks of bias and unequal impacts

hallucinations and misleading advice

unclear accountability when staff rely on AI.

End with one short paragraph that states the goal of the report

to analyze these risks in the public sector context and propose mitigation and governance measures.

System  overview and technical context  Huaqing Zheng and Jiaxing Yi

Section id system

Page purpose

Explain how the GenAI tool works at a high level and which technical choices create ethical concerns.

Content source

Use Background, System overview, and Key technical features influencing ethical concerns from Report docx.

Subsections

System overview

Summarize

internal GenAI research tool for City of Ottawa staff

types of users such as policy analysts, planners, legal advisors

question and answer workflow over bylaws, council reports, strategies, historical decisions

use of LLM with retrieval augmented generation

documents stored in secure city environment and retrieved for each query.

Technical features that affect ethics

Describe in separate short paragraphs

decisions about indexing and retrieval

which repositories are included

refresh frequency

language handling

effect of underrepresentation in the corpus.

Explain prompt and instruction controls

how system prompts and templates influence uncertainty handling and citation behavior.

Explain access controls and logging

how authentication, role based permissions, and query logs protect privacy but also create new records that need governance.

Explain model lifecycle

how switching models, fine tuning, or safety filter changes can suddenly alter system behavior and therefore must be governed and documented.

Risks  ethical issues and risk register  Jiaxing Yi

Section id risks

Page purpose

Show the main ethical issues, linked to teacher guide items on ethical analysis and risk register.

Content source

Use Ethical Issues Analysis section from Report docx and expand into a visible risk list.

Subsections

Major issues list

Create a numbered list for three headline risks

1 privacy and confidentiality of municipal records

2 bias, representation, and inequitable policy impacts

3 hallucinations, verifiability, and accountability.

Privacy and confidentiality

Summarize how importing and indexing internal documents interacts with MFIPPA obligations.

Mention

personal information in municipal records

risk of widening access beyond original need to know

model memorization concerns from research

importance of strict access control at storage, retrieval, and logging layers

role of ATIP office and potential consequences for public trust.

Bias and representation

Summarize how LLMs and historical records can reproduce inequalities.

Mention

examples from other domains

concept of AI supported decision making and automation bias in public sector

risk that some communities become invisible in analysis

need for documentation of datasets, ongoing monitoring of output patterns, and mechanisms for contesting biased outputs.

Hallucinations and accountability

Summarize

tendency of LLMs to hallucinate facts and citations

special risk in law and policy domains

how automation bias can combine with hallucinations

need for documentation, audit trails, and clear guidance that the tool is assistive only and must be verified.

Risk register summary

Add a bullet list that the detailed risk register exists in internal material and that risks are rated by likelihood and impact for

privacy breaches

biased or inequitable analysis

misleading or hallucinated content

governance or accountability failure.

Stakeholders  mapping and equity  Hye Ran Yoo and Peng Wang

Section id stakeholders

Page purpose

Follow teacher guide on stakeholder mapping and show who benefits and who carries risks.

Content source

Use Stakeholder Mapping section from Report docx.

Subsections

Stakeholder list

Internal stakeholders

policy analysts, planners, project managers

frontline staff and customer service representatives

legal counsel, ATIP officers, corporate security

IT, data, and innovation teams

senior management and elected officials.

External stakeholders

residents whose information appears in records

community organizations and advocacy groups

unions and employee representatives

local businesses and contractors

provincial regulators and oversight bodies

external vendors and cloud providers.

Distribution of benefits and risks

Explain that

efficiency gains and innovation reputation mainly benefit internal staff, management, and vendors

privacy risks, misrepresentation, and biased analysis are more heavily felt by residents, marginalized communities, and frontline workers

compliance officers carry responsibility but may have limited influence on technical design.

Close this page with one short paragraph that motivates why equity and participation from affected communities need to be included in governance.

Tools  ethical tools and mitigation strategies  Hye Ran Yoo and Peng Wang

Section id tools

Page purpose

Connect ethical issues to specific tools and methods that help manage them, following teacher guide on ethical tools.

Content source

Use Ethical Tools and Mitigation Strategies section from Report docx.

Subsections

Approach overview

State that the project proposes two main technical tool families plus governance practices

fairness audits using Aequitas

interpretability workflows using LIME

combined with policies for access control and oversight.

Fairness audits with Aequitas

Explain

Aequitas as open source toolkit for group fairness metrics

how it is applied to structured outputs of the GenAI tool

examples of outputs that can be audited such as project priority tags or flagged problem areas

how regular audits across communities or service areas can detect systematic under or over representation.

Interpretability workflows with LIME

Explain

LIME as model agnostic explanation method

how it can highlight which input paragraphs or terms most influenced a given answer or retrieval

how this supports analysts, legal, and privacy officers in understanding why the tool produced a certain summary.

Limitations

Mention briefly

fairness tools and explanation tools cannot fully solve privacy issues

local explanations can be unstable or misinterpreted

extra computation and interface complexity

need to combine with organizational rules and training.

Governance  data access and workflow recommendations  Hye Ran Yoo and Peng Wang and all members

Section id governance

Page purpose

Translate teacher guide expectations about recommendations and governance into a clear page, using Recommendations section from the report.

Content source

Use Recommendations section and any governance content in other sections.

Subsections

Data and access governance

Summarize key recommendations

classify and index corpora according to MFIPPA based access rules

enforce role based permissions at retrieval and user interface

log queries and disclosures with strict minimization and retention policies

perform privacy impact assessments and algorithmic impact assessments before deployment or major changes

allow ATIP and legal teams to pause or reconfigure high risk deployments.

System and model design

Summarize

curate and version municipal corpora with coverage reviews for communities and languages

limit retrieval to approved sources

run regular fairness audits and share results internally

always show citations and uncertainty indicators in the interface

provide simple explanation views for critical outputs.

Human oversight, workflows, and training

Summarize

position tool as decision support only

require verification of AI assisted analysis before making recommendations

define explicit approval and escalation paths for high risk use cases

train staff and managers on privacy, bias, fairness, and how to read audit or explanation outputs

create reporting channel for harmful or incorrect outputs.

Conclusion  overall findings and significance  all members

Section id conclusion

Page purpose

Wrap up the assessment and link back to public sector values, matching teacher guide on conclusion and significance.

Content source

Use Conclusion section from Report docx.

Subsections

Summary of key findings

Summarize

benefits of the GenAI tool for efficiency and institutional memory

three main risk areas

how stakeholders are differently affected

why fairness audits and interpretability are helpful but not sufficient without governance.

Significance and need for continuous management

Explain

impact on legal compliance and distributive justice

risk that opaque AI weakens transparency, challenge, and appeal in municipal decision making

need to treat the system as an ongoing sociotechnical system with continuous monitoring and remediation, not just a one time innovation project.

References  APA list  all members

Section id references

Page purpose

Display the reference list in APA style, satisfying teacher requirements.

Content source

Copy the full References list from Report docx with the same ordering and formatting.

Implementation note for Cursor

This section can be a simple list of reference paragraphs.

Implementation hints for Cursor

Do not show this part on the site if not needed. It is only for development.

The site can be implemented either as

one long scrolling page with in page anchor links that match the section ids above

or multiple sub pages with the same menu names.

Each section header in this file should become a visible heading on the page.

Under each section, put the corresponding text copied and lightly cleaned from Report docx. The current report already has strong academic wording that matches the teacher guide, so keep that language.

Make sure navigation labels match exactly

Home

System

Risks

Stakeholders

Tools

Governance

Conclusion

References
