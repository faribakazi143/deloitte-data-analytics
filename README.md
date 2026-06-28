# Deloitte Australia – Data Analytics & Forensic Technology (Forage)

**Author:** Fariba Kazi · **Tools: Tableau · Excel**

Completed the Deloitte Australia Data Analytics virtual job simulation on Forage,
acting as a data analyst for the fictional client **Daikibo Industrials**. The work
covers two deliverables: an interactive machine-downtime dashboard and a forensic
pay-equality classification.

---

## Task 1 — Machine Downtime Dashboard (Tableau)
**Problem:** Daikibo unified one month of IoT telemetry from 4 global factories and
needed to know where machines were failing most, and why.

**Approach:** Built an `Unhealthy` measure (10 minutes of downtime per "unhealthy"
status message), created two bar charts (downtime per factory, downtime per device
type), and linked them into a dashboard where selecting a factory filters the device
breakdown.

**Result:** **Factory Seiko (Osaka)** accounted for the most downtime (480 min) —
and it traced entirely to a single **Laser Welder**, indicating one prolonged outage
rather than scattered failures across machines.

**Recommended action:** prioritise maintenance and root-cause investigation on the
Seiko Laser Welder, where one machine drove 100% of that factory's downtime.

![Daikibo downtime dashboard](daikibo-downtime-dashboard.png)

🔗 **[Open the interactive version on Tableau Public](https://public.tableau.com/app/profile/fariba.kazi/viz/DaikiboMachineDowntimeDashboard_17826783881480/DaikiboMachineDowntimeDashboard)**

---

## Task 2 — Gender Pay-Equality Classification (Excel)
**Problem:** Investigate internal complaints of pay inequality using a forensic
equality score (−100 to +100, 0 = ideal) per job role and factory.

**Approach:** Added an **Equality class** column classifying each score:
- **Fair** — within ±10
- **Unfair** — beyond ±10 up to ±20
- **Highly Discriminative** — beyond ±20

Implemented as a formula so it recalculates automatically:
`=IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative"))`

**Sample output:**

| Factory | Job Role | Equality Score | Equality class |
|---|---|---|---|
| Daikibo Factory Meiyo | C-Level | −25 | Highly Discriminative |
| Daikibo Factory Meiyo | Sr. Manager | −15 | Unfair |
| Daikibo Factory Meiyo | Sr. Engineer | −5 | Fair |
| Daikibo Berlin | Operational Support | 0 | Fair |
| Daikibo Shenzhen | Sr. Manager | −21 | Highly Discriminative |

**Recommended action:** review pay bands in the roles flagged Highly Discriminative
(e.g. Meiyo C-Level and senior roles) as the priority cases for the equality audit.

---

## Explore
- 🔗 **[View the interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/fariba.kazi/viz/DaikiboMachineDowntimeDashboard_17826783881480/DaikiboMachineDowntimeDashboard)** — live, clickable version
- **Dashboard screenshot:** `daikibo-downtime-dashboard.png`
- **Completed analysis:** `daikibo-equality-table-completed.xlsx`

## Skills
Tableau · Dashboard design · Interactive filtering · Excel logic · Forensic data
classification · Data storytelling
