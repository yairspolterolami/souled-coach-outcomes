## Shared knowledge — Olami/Souled wiki

Before answering any domain question about coaches, coach-student
relationships, meetings, capacity, or payroll, read
`~/knowledge/wiki/index.md` first. Most relevant pages:

- `~/knowledge/wiki/concepts/relationship.md` — coach↔student pairing
- `~/knowledge/wiki/concepts/touch-point.md` — coach-reported meetings
- `~/knowledge/wiki/concepts/coach-supervision.md`
- `~/knowledge/wiki/concepts/coach-capacity.md` — history coverage caveats
- `~/knowledge/wiki/concepts/workday.md`
- `~/knowledge/wiki/concepts/coach-pay-period.md`
- `~/knowledge/wiki/concepts/coach-times.md`
- `~/knowledge/wiki/concepts/api-name-typos.md`

Treat the wiki as authoritative. Hard rules relevant here:

- `Welcome_Feedback_Coach_Relatrionship__c` (stray `r`) on Relationship is
  a real field.
- `Current_Growth_Cyvle_Focus__c` (v instead of c) on Touch_Point is real.
- `Weekly_Coach_Pay_Period_c__c` on Workday has a double-`_c` suffix; the
  field name really does end in `_c` before Salesforce's standard `__c`.
- `Coach_Timezone_Abbreviation__c` vs `Coach_Timezone_Abbreviation1__c` on
  Coach_Times — both exist; the `1` variant is usually the newer, correct
  one. Verify empirically.
- Fields suffixed `_del__c` (e.g. `Last_meeting_date_and_time_del__c`) are
  deprecated; don't write to them.
- Test-record exclusion: `Test_Old__c = false AND NOT Name LIKE '%test%'`.

If the wiki is missing a topic that comes up here, flag it.
Wiki repo: github.com/Olami-Souled/knowledge.