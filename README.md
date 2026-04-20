# Threat_hunting_using_splunk

# Threat Hunting: Investigating 4798 Windows Events Using Splunk

## The Threat
Event ID 4798 (User group membership enumerated) occurs when someone looks up what groups a user belongs to.

**Why this matters:** Attackers enumerate group memberships to find:
- Admin accounts
- Privileged users
- Targets for lateral movement

Normal users rarely need to enumerate group memberships. When they do, it should be investigated.

---

## Investigation Question
Are there any suspicious 4798 events in my Windows Security logs?

---

## Hypothesis
If an attacker is inside my system, they will enumerate group memberships to find privileged accounts. This will appear as 4798 events:
- At unusual times (night, weekends)
- From unusual users (non-admins)
- In bursts (automated enumeration)

---

## Tools Used
- **Splunk Free** - Log analysis and search
- **Windows Event Logs** - Security logs from my system

---

## Investigation Steps

### Step 1: Establish Baseline
What does normal 4798 activity look like?
- How many per day?
- Which users?
- What time of day?

### Step 2: Hunt for Anomalies
Look for patterns that don't fit baseline:
- 4798 at 3 AM
- Non-admin users enumerating groups
- Bursts of activity

### Step 3: Investigate Findings
For each anomaly:
- What else happened at that time? (4624 logins, 4688 processes)
- Is there a legitimate explanation?
- Does this warrant further action?

---

## Current Status
🔴 Investigation in progress

---

## Findings
*(To be updated after analysis)*

| Date | Finding | Suspicious? | Action |
|:---|:---|:---|:---|
| TBD | TBD | TBD | TBD |

---

## Conclusion
*(To be updated after analysis)*

---

## Files in This Repo
- `splunk_queries.md` - All searches I ran
- `baseline.md` - What normal looks like
- `anomalies.md` - What I found
- `screenshots/` - Evidence from Splunk

---

## What I Learned
*(To be updated after project)*
