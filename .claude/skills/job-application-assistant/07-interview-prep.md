---
framework_version: 1.0.0
---

# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

<!-- These are populated by /setup from your actual experience. Below are templates showing the format. -->

### 1. SQL Studio Frontend Optimization (Technical Excellence & Performance)
**S:** SQL Studio is an open-source Rust-powered SQL explorer with 3.7k+ GitHub stars. The frontend (React, Vite, Monaco Editor) was becoming slow under heavy user load, affecting usability across different database backends (PostgreSQL, MySQL, SQLite, DuckDB).
**T:** Optimize the frontend performance without compromising functionality or introducing breaking changes.
**A:** Analyzed rendering bottlenecks using browser profiling tools; implemented lazy loading for large result sets; optimized Monaco Editor initialization and state management; added memoization to prevent unnecessary re-renders; refined Vite build configuration for smaller bundle size.
**R:** [Complete manually: what was the measured performance improvement? Time to interact? User feedback?]
**Use for:** "Tell me about a time you optimized system performance", "Describe a challenging technical problem you solved", "How do you approach performance bottlenecks?"

### 2. gob.do & Citizen-Facing Platforms (Large-Scale Systems & Ownership)
**S:** National Competitiveness Council platforms serve thousands of concurrent users accessing digital government services (gob.do, Registro de Cuenta Única, citas.conadis.gob.do, internal Meetings system). Platforms needed to scale reliably and maintain uptime during peak load.
**T:** Own the frontend architecture and performance optimization for mission-critical citizen-facing systems serving a large user base.
**A:** Designed React architecture with Zustand state management for scalability; implemented performance monitoring and optimizations; participated in architectural decisions across the stack; collaborated with cross-functional teams to define requirements and deliver iteratively under Agile workflows.
**R:** [Complete manually: what metrics improved? Uptime? Response times? User satisfaction?]
**Use for:** "Tell me about your largest-scale project", "How do you handle high-traffic systems?", "Describe your role in a mission-critical application"

### 3. AI/LLM Integration (Learning & Innovation)
**S:** Multiple production applications needed AI-powered features to automate workflows: content generation, summarization, data transformation. Team had limited prior LLM integration experience.
**T:** Design and implement AI/LLM integrations for production systems using OpenAI and Claude APIs; optimize for performance, cost, and user experience.
**A:** Designed prompt engineering strategies for consistent, high-quality outputs; implemented streaming responses for perceived performance improvements; built backend orchestration handling retries, error cases, and response parsing; optimized API usage to reduce costs while maintaining quality; integrated Claude Code for automation tasks.
**R:** Achieved 40-50% reduction in manual user workload; improved content processing speed by ~50%; successfully deployed AI features serving thousands of users; established patterns other teams now follow.
**Use for:** "Tell me about learning a new technology on the job", "Describe your experience with AI/LLM", "How do you approach unfamiliar problems?", "What's a recent innovation you implemented?"

### 4. Content Migration WordPress→Contentful (Project Management & Technical Leadership)
**S:** Large-scale content migration project needed to move content from WordPress to Contentful headless CMS, then rebuild delivery using modern frameworks (Next.js, Astro). Complex data transformation and custom platform development required.
**T:** Lead the end-to-end migration effort, building automation scripts and new frontend platforms to handle the transition.
**A:** Built automation scripts to streamline content transformation and migration; designed custom web platforms for content delivery; coordinated with stakeholders on timeline and requirements; implemented data validation to ensure integrity; deployed incrementally to minimize disruption.
**R:** [Complete manually: was the migration on-time? How much content was migrated? What was the adoption like?]
**Use for:** "Tell me about a time you led a complex project", "Describe project management experience", "How do you handle migrations or large refactors?"

### 5. Open-Source Contributions - PearOS ISO (Technical Initiative & Problem-Solving)
**S:** PearOS ISO build pipeline was failing across different Linux distributions (CachyOS, Manjaro, other Arch-based distros) due to cross-distro compatibility issues. Project had 328+ stars but was blocked on these build failures.
**T:** Diagnose and fix the underlying build issues to enable successful ISO compilation across multiple distributions.
**A:** Investigated build configuration and identified cross-distro compatibility problems; implemented fixes handling distribution-specific differences; contributed back to the open-source project; improved documentation for future maintainers.
**R:** ISO now compiles successfully on multiple Arch-based distributions; unblocked downstream projects and users; demonstrated expertise in systems-level problems and Linux tooling.
**Use for:** "Tell me about open-source contributions", "Describe a time you solved a complex technical problem", "How do you debug infrastructure issues?"

## Common Tough Questions

### "Why did you leave [previous company]?"
> [PREPARE YOUR ANSWER - be honest, forward-looking, no negativity about former employer]

### "You don't have [specific skill/experience]."
> [PREPARE YOUR ANSWER - acknowledge the gap, bridge to adjacent experience, show willingness to learn]

### "Where do you see yourself in 5 years?"
> [PREPARE YOUR ANSWER - show ambition aligned with the role's growth path]

### "What's your biggest weakness?"
> [PREPARE YOUR ANSWER - genuine weakness with concrete mitigation strategy]

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
