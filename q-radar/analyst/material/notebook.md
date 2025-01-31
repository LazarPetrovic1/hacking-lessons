1. *Offense magnitude*
  - The **magnitude** rating of an offense in your environment is a *measure of importance* of the offense in your environment. Magnitude rating used to prioritize offenses and help you determine which offense to investigate first. **Rating of offense magnitude is re-evaluated whenever new events are added to the offense**.
2. *Offense retention*
  - **Active** - When new events are evaluated, the offense clock is reset to keep the offense active for another half an hour.
  - **Dormant** - If new events or flows are not added to the offense within 30 min or if QRadar did not process any events within 4 hours. An offense remains dormant for 5 days. If event is added while an offense is in a dormant state, the 5 day counter is automatically reset.
  - **Inactive** - An offense becomes inactive after 5 days in dormant state. New events that trigger the offense are added to a new offense instead of resetting the counter.
  - **Closed** - Offenses are removed after the retention period elapses. If more events occur for an offense that is closed, a new offense is created.
3. *Protecting offenses*
  - You can protect offenses to prevent them from being removed from QRadar after the retention period has elapsed.
4. *Showing hiddewn offenses*
  - To view hidden offenses, **clear the filter to `Exclude Hidden Offenses`** or perform a search that includes hidden offenses.
5. *Marking an offense for follow-up*
  - When you want to flag it for further investigation.
6. *The URL-domain*
  - **The URL-domain** is a custom property from *proxy logs*
7. *Which of the following is a property of flows, but not that of events?*
  - magnitude
  - network
  - bytes
  - log source
8. *How events appear on the status bar?*
  - Average per second.
9. *What is the maximum time interval at which QRadar coalesces identical events?*
  - Ten seconds.
10. *How many timestamps does an event have?*
  - Three timestamps.
11. *As a security analyst, you've noticed that the event processor stores unparsed events in the data nodes. Why is this happening?*
  - Parsing error
  - **Events-per-Second (or EPS)** is 20000
  - The system is under high load
12. *You select to follow-up on an offense from the offense list. What happens to this offense?*
  - All analysts receive mail.
  - Only you can close this offense.
  - A flag appears next to the offense.
  - This offense is now flagged for further investigation.
13. *Local and global rules* - **5 login failures in 10 min from the same user**
  - consult the drawing [Notebook]
14. *Chart types*
  - Dashboard
    + Bar
    + Pie
    + Table
    + Time series
  - Report
    + Line
    + Stacked line
    + Bar
    + Stacked bar
    + Pie
    + Table
15. *Advanced search*
  - Advanced search uses **AQL** search strings
16. *Quick search filter*
  - Search event and flow payloads by typing a text search string that **uses simple words and phrases**
17. *Closed offense*
  - Can't be reopened
18. *Response limiter*
  - You can, for example, receive more mails than the configured limit if a rule fires with a separate **Custom Rule Event (or CRE)**
  - Respond no more than ***once per hour per custom property***. If the rule fires for the second time with a `null` property within 1 hour, an e-mail will not be sent.
19. *Searching asset profile*
  - 2010-000
20. *Super-flow types*
  - Threshold
  - Anomaly rulse (***looks at a change in a short-term***)
  - Behavioural
21. *Research asset vulnerabilities*
  - Vulnerability information is located in the **Asset** tab.
22. *Confidence factor*
  - Use confidence factor to limit the number of offenses triggered by rules. Depending on the level of protection that you want **you adjust the confidence factor values to a level that best matches your network environment**. On assets of **lower importance** => **higher conf. factor** for **more secure** areas => **lower the conf. factor**
23. *Sending mail*
  - On the **Offense** tab; **Action => mail**
24. *Base64*
  - **Payload => Base64**
25. *The time that QRadar received raw event from log source*
  - ***Start time***
26. *AQL-1*
```sql
  SELECT LOGSOURCENAME(logsourceid),
  * from events WHERE
  RULENAME(custom_rule_event_list) ILIKE '%suspicious'
```
27. *Unknown (unparsed, sim audit, sim generic)*
  - **Event was parsed, but not mapped**
28. *Exporting events*
  - Export to CSV => **visible columns**
29. *When a new offense arrives, what is the first action the security team must do?*
  - View the attack path of the offense
30. *Anomaly detection rules*
  - Anomaly detection rules test the results of saved flow or event searches **to detect when unusual traffic patterns occur in your network**
31. *Time series chart*
  - For *short-term and long-term* trending of data. Using time series chart, you can **access, navigate and investigate** connections from various views and perspectives.
32. *Custom rule testing*
  - The **tests in a rule are executed in the order that they are displayed in the user interface**.
33. *AQL-2*
  - `/.*pdf/` or `/.*exe/`
34. *Schedule report is every Monday and first day of the month. When they want report on Thursday*.
  - MON-WED
  - MON-THU (THU-WED)
  - ***whole last week*** (!this!)
  - from last week to THU
35. *Dashboard (nwe custom dashboard)*
  - A new custom dashboard is empty, you must add items. **Type unique new name**.
36. *DSSE (device stop sending events)*
  - Runs on the absence of events.
37. *Wizard uses the following key elements to create report*
  - **layout**, **container**, **content**
38. *Search for all viruses*
  - some search option
39. *Manually generating report*
  - Does not restart the existing report schedule
40. *Notes and annotations*
  - Bottom offense **Summary** page
41. *for 10min 15 mails received and see only 1 offense*
  - all mails in one offense (limiter?)
42. *Additional information for offense*
  - Payload => in payload information box review, the raw events valuable for investigation
43. *VPN log source*
  - Advanced Persistent Threat
44. *What is displayed in offense columns by default?*
  - QID
  - Log source
45. *Where are offenses collected?*
  - console (!this!)
  - node
  - processor
  - collector
46. *Check point*
  - OPSEC LEA/Syslog
47. *New log source was created and low level category is stored*.
  - Events are not correctly parsed
  - Admin tab => log sources => parsing order
