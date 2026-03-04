---
name: china-medical-ad-compliance
description: Provides comprehensive guidance on China's laws and regulations for medical device advertising. Use this skill to review advertising copy, ensure compliance with national and local regulations (including Beijing and Shanghai), and differentiate between rules for public and private promotional channels.
---

# China Medical Device Advertising Compliance Skill

This skill provides the necessary knowledge and workflow to ensure that advertising content for medical devices complies with Chinese law.

## Core Principle

All advertising activities for medical devices in China must be **truthful, legal, and based on official documentation**. The primary sources for any claims must be the product's **registration certificate, approved manual, and technical specifications**. Avoid any creative embellishments or claims that cannot be substantiated by these documents.

## Workflow

When a user asks for a review of their medical device advertising copy or has questions about compliance in China, follow these steps:

### 1. Load Compliance Knowledge

First, read the core reference document to load the detailed compliance rules into your context. This guide is based on the latest national and local regulations.

```
print(default_api.file(action='read', path='/home/ubuntu/skills/china-medical-ad-compliance/references/compliance_guide.md'))
```

### 2. Analyze User's Request

Thoroughly review the user's provided advertising copy, marketing plan, or specific questions. Identify the key claims, target audience, and intended channels (public vs. private).

### 3. Conduct Compliance Review

Cross-reference the user's material against the rules detailed in `compliance_guide.md`. Pay special attention to the following areas:

- **Negative Checklist**: Scrutinize the copy for any prohibited content, such as guarantees of efficacy, assertions of safety (e.g., "no side effects"), use of absolute terms ("best," "#1"), or endorsements by individuals/organizations.
- **Required Disclaimers**: Ensure all mandatory statements are present and clearly displayed, such as "Please read the product manual carefully or purchase and use under the guidance of medical personnel."
- **Content Consistency**: Verify that all claims about the product's name, scope of application, and mechanism of action do not exceed what is stated in the official product manual and registration documents.

### 4. Formulate and Deliver Recommendations

Provide a clear, structured, and actionable response to the user.

- **Structure your response** based on the sections in `compliance_guide.md` (e.g., Core Principles, Negative Checklist, Public vs. Private Channels).
- **Cite specific risks**: For each potential violation, explain the risk and reference the specific rule from the guide.
- **Provide concrete suggestions**: Instead of just pointing out problems, offer compliant alternatives. For example, if the user wrote "cures insomnia," suggest changing it to a description of the product's approved application scope from the manual.
- **Differentiate channel advice**: Clearly distinguish your recommendations for **public domain advertising** (which requires formal pre-approval and is highly restricted) versus **private domain content** (such as educational materials, which have more flexibility but must not function as disguised ads).

### Example Interaction

**User:** "Can you check if this ad copy is compliant: 'Our new light therapy device is the best on the market and is guaranteed to cure seasonal affective disorder. Recommended by Dr. Li.'''

**Agent's Action (following the skill):**
1.  Read `compliance_guide.md`.
2.  Analyze the copy: identifies "best on the market" (absolute term), "guaranteed to cure" (efficacy guarantee), and "Recommended by Dr. Li" (expert endorsement).
3.  Formulate a response explaining that all three claims violate the advertising law as detailed in the negative checklist. Suggest removing them and replacing them with approved language from the product's manual.
