# Jira
Lab: Configuring Issues (Company-managed Projects)
Estimated time: 25 minutes
In this lab, you will:
1. Add labels to issues.
2. Search for issues by label.
3. Hide a field shown in issue details.
4. Create and display a custom field.
Note: These instructions assume that you have Jira Administrator permission. They also assume that
you created a company-managed kanban project named projectA in an earlier lab.
These instructions DO NOT APPLY to team-managed projects.
1: Add labels to issues.
1. Add labels named refactor and/or database to some of the issues in projectA . You do this by
adding entries to the Labels field of an issue.
2. In board settings, click the Card layout tab and configure your board to show labels on the cards.
View your board to verify that the labels appear.
Congratulations, you have added labels to issues.
2:Search for issues by label.
1. Open an issue with a label of database .
2. Under Labels , click on the database label. You should be brought to the Filters area with a
search for all issues with the database label. This is the easiest way to search for issues with a
certain label.
3. Use basic search to search for issues with a label of refactor . You will have to use the More
dropdown to add Label as a search criteria.
4. In JQL search, search for issues with a label of refactor but not database .
5. Create other searches related to labels.
Congratulations, you have searched for issues by label.
3: Hide a field shown in issue details.
1. Open an issue of type Story in your projectA project.
2. Notice that the Components field is a secondary field, meaning that you must click Show more to
see it.
3. Select the more icon (...) in the upper right. Select Configure. You are brought to the Issue
layout screen under Project settings for the projectA project (you could have navigated there 


directly). This screen shows the primary and secondary fields that are shown on the issue details
screen for users of this project.
4. Explore this issue layout screen. Notice that any changes we make here will apply to all of the issue
types of this project, except for bugs.
5. Let's assume that your project doesn't use components. Drag the Components field to the right so
that it becomes a hidden field.
6. Click Save changes.
7. View the issue details for any issue types other than bugs and notice that the Components field is
no longer displayed.
8. Open an issue of type "bug" and notice that the Components field is still there. To remove this field
for bug issues, open a bug issue and configure the Components field to be hidden, as you did for
the other issue types.
It's important to always understand the scope of changes that you are making with companymanaged Jira projects. In this case, because the configuration is done using project settings for
the projectA project, only users of this project will see this behavior. Also, we saw on the
issue layout screens that this change will apply to all issue types, including bugs.
9. Configure the Components field to again be shown as a secondary field for all issue types. Verify
your changes.
4: Create and display a custom field.
We will assume that our project team would like to include a field named "Acceptance Criteria" for
issues of the project. This is not a field that is provided out-of-the-box by Jira. You will create this
field, then later configure your issue screens for the project to show this field.
Creating a custom field in company-managed projects is a Jira application-level change.
1. Click the gear icon near your user avatar.
2. Under Jira Settings, select Issues.
3. Click Custom fields.
4. Explore the existing fields in your Jira application.
5. Click the Create custom field button at the top of the page.
6. In Select a Field Type, select the Text Field (multi-line) option. Click Next.
7. Enter Acceptance Criteria for the field name. For Description, enter A list of usercentered tests that must pass for the story to be considered done. . Click Create.
8. In Associate field Acceptance Criteria to screens, select the Kanban Default Issue Screen
associated with your project. The Acceptance Criteria field will only be added to screens of this
project (excluding bugs). Click Update.
9. You should now see your Acceptance Criteria custom field in the list of custom fields. It should
be associated with your Kanban Default Issue Screen.


10. Navigate to your projectA project and view the issue details for an issue of any type except bug.
You should see an Acceptance Criteria text area. In the text area, you can enter User must be
able to enter an email address. .
11. Open the create issue dialog and verify that your Acceptance Criteria field is available when
creating issues.
You can now use your custom Acceptance Criteria field like other fields in Jira.
Congratulations, you have created a custom field and added it to issue details screens of a project.
You have completed this lab.
Copyright © 2021 Atlassian


Lab: Issue Types (Company-managed)
Estimated time: 30 minutes
In this lab, you will:
1. Create issues of different types.
2. Create subtasks.
3. Add a custom issue type to your project.
4. Create a swimlane for the custom issue type.
Note: These instructions assume that you have Jira Administrator permission. They also assume that
you created a company-managed kanban project named projectA in an earlier lab.
These instructions DO NOT APPLY to team-managed projects.
1: Create issues of different types.
1. Navigate to your projectA company-managed kanban project.
2. If your kanban board has a separate backlog (a Backlog tab), move the backlog back to the board
using the Columns tab under board settings. This is so you can see the issues on the board when
you create them.
3. Create an issue with a summary/title named add item 4 (or the next item number on your board).
Assign an Issue Type of Story to the issue.
4. Create an issue with a summary/title named fix bug 1 . Assign an Issue Type of Bug to the issue.
5. Create an issue with a summary/title named complete task 1 . Assign an Issue Type of Task to
the issue.
6. Move the issues through some of the statuses on the board. Notice that they all behave in the same
way, because they all use the same workflow.
Congratulations, you have created issues of different types.
2: Create subtasks.
1. Using the same procedure as in the previous step, try to create an issue with an issue type of
Subtask . Notice that this option is not available. This is because subtasks must have a parent
issue. Cancel the attempt to create this issue.
2. From the board, open the add item 4 issue. Click on Create subtask to create a subtask for this
story.
3. Create a subtask with a summary/title of add item 4a . Notice that a new issue key and status are
assigned to the subtask.
4. Create another subtask with a summary/title of add item 4b .
5. View the board. Notice that the subtasks have been added under the add item 4 story in the
BACKLOG status, independent of the status of the parent issue.
6. Move the subtasks to different statuses. Notice that subtasks have independent statuses.

7. On the project's sidebar, select Issues and filters to view the issues of the project. Click on All
issues. Notice that the subtasks are shown in the list. Subtasks are issues- they just need to have a
parent issue.
8. Select the add item 4b subtask. Click the more icon (...) on the right to bring up a menu. Convert
the subtask to an issue by selecting Convert to Issue. Select Story as the new issue type. Select
the defaults for other values and click Finish to convert the issue. Notice by the icon that what was a
subtask is now a story.
9. View the kanban board. Move the add item 4 story to the Selected for Development status.
Move the add item 4a subtask to the Done status. Jira should notice that all of the subtasks for
the story are done and ask you if you want to update the parent issue to match the status. Click
Update to move the parent issue to the Done status.
10. Add subtasks to the fix bug 1 and complete task 1 issues. Notice that subtasks for bugs and
tasks behave the same way as with stories.
Congratulations, you have created subtasks.
3: Add a custom issue type to your project.
Custom issue types allow your team to create issues that are appropriate for the types of work that the
team does.
1. With your projectA project selected, click Project settings from the sidebar.
2. Click on Issue types. You are shown the issue type scheme for your project. An issue type scheme
is the collection of issue types used by your project. You should see the default issue types for
company-managed kanban projects. (These are also the default issue types for company-managed
scrum projects.)
3. In the upper-right corner, click Actions, then select Edit issue types.
4. Notice that the default issue type is Story . This is the issue type that will be selected by default
when you first create an issue. View the order of the issue types under Issue Types for Current
Scheme. You can rearrange these to change the order of the types in Jira dialogs.
5. In the upper right corner, click + Add issue type. Name the type Small . Add a description of A
work item that is tracked but takes a small amount of time to complete. For the
Type, keep the current value of Standard Issue Type. Click Add to add the issue type to your
project. You should now see your custom issue type at the bottom of the list on the left. You can
rearrange the order if you would like.
6. Click Save to save your issue type scheme.
7. Change the avatar (icon) of your issue type.
Because an issue type can be used by any project, the configuration is under the Jira
application settings. To reach Jira settings, click on the gear icon near your user avatar.
Click Issues, and then Issue types.
Click the Edit link to the right of the Small issue type.
Click select image to change the issue type avatar.
Select the minus (-) sign, or upload your own avatar for your issue type.


Click Update to update the avatar for your issue type. The Small issue type should now have
the new icon.
8. Navigate back to your projectA project. Create an issue of type Small named small item 1 .
View the item on the kanban board. Notice your icon. Open the issue and notice that you can add
subtasks to the issue.
Congratulations, you have added a custom issue type to your project.
4: Create a swimlane for the custom issue type.
1. Use basic search to search for issues of your new custom type. There should be a single issue.
Switch to JQL search and view the query. Copy the query to your clipboard.
2. Navigate to the Swimlanes tab under the the projectA board's settings.
3. Explore the Base Swimlanes on dropdown to view the options for swimlanes. For example, you can
create swimlanes for each team member easily by selecting Assignees .
4. Under Base Swimlanes on select Queries.
5. Add a swimlane named Small Tasks , paste the JQL issuetype = Small and a description of
Issues that should be tracked but take a small amount of time. . Make sure to click
Add .
6. View your swimlane on the board.
7. Experiment with other swimlanes.
Congratulations, you have created a swimlane for the custom issue type and completed this lab.
Copyright © 2021 Atlassian


Kanban
Lab: Our First Jira Company-managed Project
Estimated time: 20 minutes
In this lab, you will:
1. Sign up for a Jira Software Cloud account (if necessary).
2. Create a company-managed kanban project.
3. Create issues.
1:Sign up for a JiraSoftware Cloud account (if necessary).
1. If you already have a Jira Software Cloud account in which you are a Jira administrator, you can use
it for this course. If you do not have a Jira Software Cloud account, you can use the following link to
create a free account for up to 10 users.
https://www.atlassian.com/software/jira/free?
utm_source=coursera&utm_medium=jira&utm_campaign=agile
This course uses Jira Software. You can also install free versions of Confluence and/or Jira
Service Management at any time, but they are not covered in this course.
When you are asked to provide a site name, you can enter any name that you want, such as
your team name or your first name and last name initial (if it is available). This name is used to
access your Jira account at (https://[your_site_name].atlassian.net).
If you are asked onboarding questions such as "What type of team do you work in?", click
Skip question or Skip. You are ready to create a project when you reach the "Project
templates" screen.
Please make a note of your site name and the email address that you used to sign up for the
account.
2. (Optional) Bookmark your home Jira page (https://[your_site_name].atlassian.net) in your browser.
2: Create a company-managed kanban project.
Note: These instructions assume that you are using Jira Software Cloud. Because features are rolled
out in stages to groups of users, the details that you see may be slightly different. If you use other Jira
versions, the details will also be different for you.
Note: These instructions DO NOT APPLY to team-managed projects. If you see messaging that you
have created a team-managed project, you are on the wrong path and should create a companymanaged project.
1. If this is your first project:
You may be asked questions related to your agile experience and type of project that you are
interested in creating. These questions help decide the template of your first project. On the
screens that you are shown, select Skip question or Skip, depending on the what the button
says.
On the Project templates screen, select Software development on the left and select the
Kanban template. Click Use template.
Click Select a company-managed project.
2. If this is not your first project (note: you may see some slightly different steps than listed here):

Log in to Jira (if necessary). You can log in using https://[your_site_name].atlassian.net or find
your site name at https://my.atlassian.com.
Click the Projects dropdown in the top navigation.
Select Create project.
On the Project templates screen, select Software development on the left and select the
Kanban template. Click Use template.
Click Select a company-managed project.
3. In the Create project window, enter projectA for the project name.
4. You can leave the Key value at its default value.
5. Verify that Template is Kanban.
A template is the initial configuration of your project. Each template provides different default
behavior and tools to the project. We are selecting the kanban template. Among other things,
this means that a kanban board will be included with the project. We will discuss kanban boards
later.
6. Click Create.
7. You should see the kanban board for your project.
Congratulations, you have created a company-managed kanban project.
3: Create issues.
The planned work of a project is broken down into issues. Issues are also known as work items, stories
and more. We will start with three simple issues, named "add item 1", "add item 2" and "add item 3".
1. Create an issue named "add item 1":
Click the Create button (or +) in the top navigation to create an issue.
Under Summary, enter add item 1 .
The Issue Type should be Story.
Since you are creating more issues after this one, you have the option to click the Create
another checkbox to expedite issue creation.
Click Create.
2. Create an issue named add item 2 .
3. Create an issue named add item 3 .
4. On your kanban board, you should see your three issues in the backlog column. We will discuss the
backlog later.
5. To view the project's issues in a list, click on the Issues and filters tab in the sidebar, then select All
issues.
6. Click on Back to project and then Kanban board to navigate back to the kanban board.
Congratulations, you have created three issues and completed this lab.
Copyright © 2021 Atlassian


Scrum
Lab: Scrum (Company-managed)
Estimated time: 25 minutes
In this lab, you will:
1. Create a scrum project.
2. Create issues.
3. Create and plan a sprint.
4. Execute a sprint.
5. Complete a sprint.
1: Create a scrum project.
This lab creates a company-managed scrum project. These instructions DO NOT APPLY to teammanaged scrum projects.
1. Log into Jira (if necessary). https://[your_site_name].atlassian.net
2. Click the Projects dropdown in the top navigation.
3. Select Create project.
4. On the Project templates screen, select Software development on the left and select the Scrum
template. Click Use template.
5. Click Select a company-managed project.
6. For the project name, enter projectB .
7. You can leave the Key value at its default value.
8. Verify that Template is Scrum.
9. Click Create. You should see your projectB project.
Congratulations, you have created a scrum project.
2: Create issues.
1. The issues of your project are initially placed in the product backlog. Click the Backlog tab to view
it. It should be empty.
2. Create three issues in the product backlog of type Story with summaries of add item 1 , add
item 2 and add item 3 . You can do this by clicking on Create (or the + sign) or by typing directly
in the Backlog .
Congratulations, you have created a product backlog with three issues.
3: Create and plan a sprint.
A sprint is a period of time where you complete a certain number of issues.
1. Click the Backlog tab.
2. Click Create sprint. You now should see Sprint 1 along with the product backlog.

The start of the sprint includes a sprint planning meeting. In this meeting, the sprint team
usually decides on the sprint goal, estimates the amount of work of issues and decides which
issues to complete during the sprint. The development team decides how to accomplish the
work of the sprint. All projects and sprint planning meetings are unique.
3. Add estimates as story points to the issues. We will arbitrarily say that add item 1 is 1 point, add
item 2 is 2 points and add item 3 is 4 points.
Click on each issue in the product backlog and add its estimate under the Story Points
field. After entering an estimate, you should see the estimate in gray next to each issue in the
product backlog.
The development team usually is responsible for estimating story points. Story points are
relative units indicating the effort involved in completing the issue.
4. Prioritize the product backlog. We will arbitrarily give the 2 point story ( add item 2 ) the highest
priority and the 4 point story the lowest priority.
Drag and drop the stories into their correct order in the backlog (with add item 1 at the
top).
The product owner is usually responsible for prioritizing stories in the product backlog.
5. Add stories to the sprint. We will arbitrarily assume that the team can execute up to four story points
per sprint. This is known as the team's velocity.
Drag the add item 2 and add item 1 stories to the sprint. The set of stories in the sprint
are called the sprint backlog.
6. Notice that the team has estimated that its velocity for this sprint will be 3 story points.
The development team is usually responsible for deciding how many of the top issues to move to
the sprint backlog.
Congratulations, you have created and planned a sprint.
4: Execute a sprint.
1. Click the Start sprint button associated with the sprint backlog. Change the duration of the sprint to
1 week . Add a sprint goal of Create the first product increment. Click Start.
The scrum team agrees to the sprint goal during the sprint planning meeting.
2. Under the Active sprints tab, you should see the board for your current sprint. Notice that you have
two issues in the TO DO column. Notice that the other columns are IN PROGRESS and DONE . Also
notice that the sprint goal is under the sprint name.
3. View the workflow for the issues. Do this by clicking Project settings > Workflows. Click on the
diagram link to view the workflow. Notice that there are three statuses in the workflow, TO DO , IN
PROGRESS and DONE . These are the default statuses in the workflow when you choose the scrum
template while creating a project. Notice that there is no BACKLOG status. Navigate out of the
project settings.
The workflow for projects created with the company-managed kanban template is different from
the workflow for projects created with the company-managed scrum template. The statuses in

the company-managed kanban template workflow are BACKLOG , SELECTED FOR DEVELOPMENT ,
IN PROGRESS and DONE .
4. Click the Backlog tab for your project. Click to view the status of the add item 3 issue that is still
in your product backlog. Notice that its status is To Do , the same status as the issues in the first
column of the sprint board. The items in the product backlog are there because they have not been
added to any sprints. In company-managed scrum projects, the status of each issue is independent
of the product backlog. (You could change the status of the add item 3 issue to IN PROGRESS
and it would not appear on the sprint board.)
The company-managed kanban backlog functions differently than the company-managed scrum
backlog. Unlike company-managed scrum, the items in the company-managed kanban backlog
are related to the issue's status.
5. Click the Reports tab. View the burndown chart for this sprint. Jira has added guidelines for story
point completion during the sprint. The starting value is the total number of story points that you
added to the sprint backlog. For the duration of the sprint, a linear decrease in the number
remaining story points is assumed, except for non-working days.
6. View the Sprint Report. Notice that this contains a burndown chart, as well as a list of issues in the
current sprint.
Sprint reports are a great way to quickly view the current status of the sprint.
7. Navigate back and view your board under the Active sprints tab. Let's assume that you are a
member of the development team and that you will work on the add item 2 issue. Open the issue.
Under the Assignee field, click Assign to me.
8. Navigate back to the sprint board. Notice your icon in the add item 2 card. Drag the add item 2
issue to the IN PROGRESS column.
9. Let's assume that you have finished the work of the add item 2 issue. Drag it to the DONE
column.
10. Repeat the process above and complete the add item 1 issue.
Congratulations, you have executed a sprint.
5: Complete a sprint.
1. Now that the issues of the sprint are done, you can end the sprint. In the upper right above the
board, click Complete sprint. Click Complete.
You usually only complete a sprint at the end of the planned sprint duration. We are ending it
early just for learning purposes.
2. View the sprint report. It shows a summary of the sprint, including the issues that were completed in
the sprint. The chart in this sprint report looks a little strange because we accelerated the
completion of this sprint.
3. Click on the tabs to view the other reports that are automatically created by Jira, such as the
velocity chart. You estimated and completed three story points in this sprint, so your velocity for
sprint 1 was three story points.
4. At this point, you would usually have a sprint review meeting to show the increment to the scrum
team and optionally to its stakeholders.

5. After the sprint review meeting is a meeting called the sprint retrospective. This is a meeting for the
scrum team to discuss how the team can execute better next time.
Congratulations, you have completed a sprint and completed this lab.
Copyright © 2021 Atlassian
