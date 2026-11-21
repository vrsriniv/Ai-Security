---
name: morning-brief
description: Build and deliver the user's daily 7:30 AM IST Life OS brief (security news, today's plan, one well-being/family/social nudge) by Gmail and WhatsApp. Use when asked for the morning brief or when a scheduled task fires it.
---
# Morning brief

1. Read the private profile (see CLAUDE.md). Note today's date in IST and the weekday.
2. **Security news (last 24–36h)** — use WebSearch (send searches in parallel). Cover, in this order,
   skipping any with nothing material:
   - AI/LLM security (prompt injection, agent attacks, model supply chain, AI red teaming, new OWASP/MITRE ATLAS guidance)
   - Critical CVEs & exploits (CISA KEV additions, CVSS ≥ 9, public PoCs, actively exploited)
   - Attack techniques & red-team tradecraft (new TTPs, tools, notable write-ups/bug bounty)
   - AI in blue teaming (vuln management, SOC automation, detection engineering) and industry shifts
   - India: CERT-In advisories, RBI/SEBI cyber circulars, DPDP Act, notable Indian breaches
   Each item: one-line headline, 1–2 lines "why it matters to a fintech security pro", source link.
   Max 8 items. End with "Try today": one hands-on thing (a lab, a PoC to read, a detection to write).
3. **Today's plan** — if Google Calendar is connected, list today's events; otherwise list the top 3
   priorities from the profile/planner. Add the weekly/monthly review if it's Sunday / the 1st.
4. **Nudge** — rotate by weekday: Mon/Thu fitness, Tue/Fri stress & sleep, Wed kids activity idea,
   Sat social (someone to call / an event this weekend in Bangalore), Sun FIRE check-in.
5. **Deliver**
   - Gmail: send to the user's own address, subject `Morning Brief — <DD Mon YYYY>`, HTML or clean text.
   - WhatsApp (Zapier "WhatsApp Notifications", template `message_reminder`): the template only carries
     a short `name` and a `link_to_reply`, so send name = "Morning Brief <DD Mon>: <top headline, ~60 chars>"
     and link = a Gmail search link for the brief's subject. If it fails, say so in the email footer.
6. Don't commit the brief to this public repo.
