# agentforce-grantmaking-grantee-progress-report-agent
OVERVIEW

Grantee submits progress reports (Funding Award Requirements) which can be summarized on the Requirement (including Requirement Sections and all associated Files), the Funding Award, and eventually through program summary to state effectiveness of awards. 

Lucid-Based Flow Documentation: 

https://lucid.app/lucidchart/0d67d704-3da7-4383-a710-39676959653e/edit?invitationId=inv_fd9467d2-b6a3-4be9-86f2-63fc15cbf73e&page=0_0


Implementation Considerations: 

* Deploy the flow & prompt launcher(s) as a button in order to control flex credit consumption
* Expose flow & prompt launcher to a smaller subset of users when testing to evaluate patterns of credit consumption
* If you receive requirement documents in other languages, add the specific language the prompt should use for the summary output
* If you receive PII as part of your requirements, be advised that the document may not mask all PII prior to sending to the LLM



Known Issues:

* Summaries will only review PDF formatted documents in v1



Project Parking Lot:

* Enhancement - Comparison of Intended Outcomes vs Funding Award Summarization
* Enhancement - Provide automated way for Requirement summaries to be retained in a Note upon a re-summarization of the Requirement
* Enhancement - Agentic actions for creating/updating Outcome-related objects when the prompt analyzes the Requirement doc(s) 

_______________________________________

Object Usage:

* Funding Award: Used to capture award of grant, will serve as summary base to capture what was submitted on requirements as well as manual input of goals/outcomes awardee is working towards (used in comparison process)
* Funding Award Requirement: Used to capture submission of reporting/updates by grantee to document progress on intended goals
* Funding Award Requirement Section (Optional): Used to capture multiple steps/submission parts of Funding Award Requirements, submitted data/files will be accounted for on summary of Funding Award Requirement


Custom Fields:

* Funding Award | Award Summary: Used to summarize all summaries generated on child Funding Award Requirements
* Funding Award | Intended Outcomes: Used to capture Awardees intended Goals/Outcomes (to be manually populated), will be used in comparison of submitted requriements and intended goals
* Funding Award | Summary Vs Intended Outcomes Comparison: Used to track progess against intended outcomes
* Funding Award Requirement | Requirement Summary: Used to summarize triggering Funding Award Requirement, associated Funding Award Requirement Sections, and all associated Files


Flows:

* Funding Award Summary Comparison - Button
* Funding Award Summary - Button
* Funding Award Requirement Summary - Button


Quick Actions
* Funding Award | Summarize Requirements
* Funding Award | Compare Summary/Outcomes
* Funding Award Requirement | Summarize Requirement


Prompts
* File Summary - Summarizes Files associated to Funding Award Requirement or Funding Award Requirement Section
* Funding Award Summaries - Summarizes all Requirement Summaries associated to Funding Award
* Requirement Summary - Summarizes each individual Funding Award Requirement or Funding Award Requirement Section
* Full Requirement Summary - Summarizes all summaries generated from Requirement Summary Prompt
* Funding Award Summary Comparison - Compares Award Summary and Intended Outcomes


Agentforce Credit Usage:

* Requirement Summary Generation: 
Opportunity for high credit usage depending on # of files, document size/content, and requirement sections
* Funding Award Summary Generation
* Funding Award Comparison (summary to goals)


General Notes:

* File summarization will only process PDF Files
