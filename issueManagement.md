# Runtime Issue Lifetime Management Process
This document explains the current runtime issue management process in order to provide clarity on the topics such as triage process and serve as a central place with pointers to related documents.

## Goal of Issue Lifetime Management
The goal of issue lifetime management is to manage an issue effectively throughout the lifetime of the issue from open to close and to communicate the status of it to relevant participants such as author, assignee(s), commenter(s), area owner(s) and team(s) for timely responses and actions.

## Issue Submission
An issue is first created when an author submits one to dotnet/runtime Github repo at https://github.com/dotnet/runtime/issues/new/choose. There are multiple issue templates that a user can use depending on the nature of the issue. Currently, there are four runtime issue templates for bug report, API suggestion, performance issue report, and security vulnerability issue. If an issue does not fit those categories, `Blank issue` template can be used. 
The runtime issue submission website also has links to issue submission pages of other repos such as ASP.NET Core, .NET SDK, Entity Framework, Roslyn compiler, Windows Forms, and WPF. It is essential to submit an issue to a correct repo for timely treatment of it.

## Triaging an issue
Once an issue is created, it is triaged to an area and milestone through triaging process. Triaging is performed collaboratively by dotnet-issue-labeler bot, msftbot, feature area owners and feature area team members. When an issue is successfully triaged, it will be assigned an area, milestone and optionally assignee and/or project.
- "Assign an area": We try to assign an area immediately via our "dotnet-issue-labeler" bot, but it may take longer if the bot cannot determine an area to assign. If the bot cannot determine an area, "runtime owner" will manually assign an area.
-- List of runtime areas and owners can be found in https://github.com/dotnet/runtime/blob/main/docs/area-owners.md.
- "Labeling": The bot also initially puts determined area label and `untriaged` label to the issue. If the bot cannot determine an area, runtime owner will put area label.
- "Assign milestone": Once an area is assigned, an "area owner" will further triage it by assigning "milestone" and optionally "assignee". If the area owner cannot determine the milestone immediately, for example, because more investigation is needed, the area owner will remove `untriaged` label and put `needs further triage` label.
-- When the assigned milestone is not specific product but `future`, it means that it will be kept as backlog.
- "Assign Assignees": Issue can be effectively handled when there is an owner. An issue can be initially assigned to a subject expert or an area owner. When an action or follow-up is required from other person, assign the issue to the person.

## Criteria to determine milestone
Many different criteria can be considered in determining milestone. Some of them include but are not limited to the following:
- Significant customer feedback or impact
- Broken or significantly incomplete scenario
- Blocking key partner scenarios
- High impact feature or performance regression from last release
- Compliance or security issues
- Number of comments from community
- Number and kind of reactions from community, for example, number of likes

## Labels
Runtime currently has 267 labels (https://github.com/dotnet/runtime/labels). Putting right and relevant labels will help handling issues faster and easier. We use bots to automate some process. msftbot puts some labels automatically.
Some labels that are worthwhile to mention are as following:
- `Needs author feedback`: It is used when additional input is needed from an author. If the author does not respond in time, the issue will be closed automatically. Please refer `no recent activity` label for details.
- `no recent activity`: If there is no activity for 14 days after `needs author feedback` label is added, `no recent activity` label is added. If there is no further activity for 7 more days, an issue will be closed automatically.
- `untriaged`: New issue has not been triaged by the area owner
- `needs further triage`: Issue has been initially triaged, but needs deeper consideration or reconsideration
- `question`: The issue is user question.
- `duplicate`: The issue duplicate of another issue.
- `off-topic`: The issue is not related to the goals of our project.
- `Priority 0`: Critical to the release
- `Priority 1`: Very important to release, not a ship blocker
- `Priority 2`: Moderately important
- `Priority 3`: Nice to have
- `User Story`: Short requirements or requests written to enable user scenario
- `epic`: Large work that can be broken down into a number of smaller user stories
- `tenet-performance`: Performance related issue
- `bug`: The issue is about broken feature.
- `api-suggestion`: Early API idea and discussion. it is NOT ready for implementation.
- `api-approved`: API was approved in API review. It can be implemented.

## Closing an Issue
An issue can be closed by multiple different reasons:
- Fixed in PR: If a PR that fixes the issue is merged
- Duplicate: If an issue is duplicate of another issue
- Off topic: If an issue is not related to the goals of our project and thus not actionable
- No recent activity: No response for extended days after author feedback is requested
- Not an issue: when an area owner determines that it is by design
- Not reproducible: Failure or issue is not reproducible, maybe because it was fixed in previous code changes

## Bots
[Placeholder] What are automated by bots?














