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

Lab: Our First Jira Team-managed Project
Estimated time: 5 minutes
Note: This lab is optional. It assumes that you have done the previous company-managed version of
this lab. If you are not interested in working with team-managed projects, you can skip this lab.
In this lab, you will:
1. Create a team-managed kanban project.
2. Create issues.
1: Create a team-managed kanban project.
Note: These instructions assume that you are using Jira Software Cloud. Because features are rolled
out in stages to groups of users, the details that you see may be slightly different.
Note: These instructions DO NOT APPLY to company-managed projects. The previous lab is the
company-managed version of this lab.
1. Log in to Jira (if necessary). You can log in using https://[your_site_name].atlassian.net or find your
site name at https://my.atlassian.com
2. Click the Projects dropdown in the top navigation.
3. Select Create project.
4. On the Project templates screen, select Software development on the left and select the Kanban
template. Click Use template.
5. Click Select a team-managed project.
6. In the Create project window, enter projectAteam for the project name (the team is for teammanaged).
7. If you are using the free plan, you should notice that anyone with access to your site (meaning that
they were added as a user of the site) can access and and administer this project. If you are not
using the free plan, there should be an Access dropdown. Team-managed projects are designed for
members of teams to create and configure. The configuration is simple, though usually not as
powerful as the configuration of company-managed projects. The Access dropdown is used to
easily limit access to the project, if desired. If available, you should set the access to Open. (The
other options are "Limited" and "Private".)
8. You can leave the Key value at its default value.
9. Verify that Template is Kanban.
10. Click Create. You should see the kanban board for your project.
Congratulations, you have created a team-managed kanban project.
2: Create issues.
The planned work of a project is broken down into issues. Issues are also known as work items, stories
and more. We will start with three simple issues, named "add item 1", "add item 2" and "add item 3".
1. Create an issue named "add item 1":

Click the Create button (or +) in the top navigation to create an issue. If you see + Create
issue at the bottom of a column, you could also click that.
Under Summary (or "What needs to be done?"), enter add item 1 .
The Issue Type should be Task (a blue check box)..
Click Create or Enter.
2. Create an issue named add item 2 .
3. Create an issue named add item 3 .
4. On your kanban board, you should see your three issues in the To Do column.
Congratulations, you have created three issues and completed this lab.
Copyright © 2021 Atlassian

Lab: Scrum (Team-managed)
Estimated time: 20 minutes
In this lab, you will:
1. Create a team-managed scrum project.
2. Create issues.
3. Create and plan a sprint.
4. Execute a sprint.
5. Complete a sprint.
1: Create a team-managed scrum project.
This lab creates a team-managed scrum project. These instructions DO NOT APPLY to companymanaged scrum projects.
1. Log into Jira (if necessary). https://[your_site_name].atlassian.net
2. Click the Projects dropdown in the top navigation.
3. Select Create project.
4. On the Project templates screen, select Software development on the left and select the Scrum
template. Click Use template.
5. Click Select a team-managed project.
6. In the Create project window, enter projectBteam for the project name.
7. If you are using the free plan, you should notice that anyone with access to your site (meaning that
they were added as a user of the site) can access and and administer this project. If you are not
using the free plan, there should be an Access dropdown. You should set the access to Open.
8. You can leave the Key value at its default value.
9. Verify that Template is Scrum.
10. Click Create. You should see your projectBteam project.
11. Click Project settings. Click Features. Notice that the Backlog and Sprints features are
automatically turned on for team-managed scrum projects. Navigate back to the project.
Congratulations, you have created a scrum project.
2: Create issues.
1. The issues of your project are initially placed in the product backlog. Click the Backlog tab to view
it. It should be empty.
2. Create three issues of type Story in the product backlog with summaries of add item 1 , add
item 2 and add item 3 . You can do this by clicking on Create (or the + sign) or by typing directly
in the Backlog.
Congratulations, you have created a product backlog with three issues.

3: Create and plan a sprint.
A sprint is a period of time where you complete a certain number of issues.
1. Click on the Backlog tab.
2. If you do not see sprint 1, click Create sprint. You should see an empty Sprint 1 along with the
product backlog.
The start of the sprint includes a sprint planning meeting. In this meeting, the sprint team
usually decides on the sprint goal, estimates the amount of work of issues and decides which
issues to complete during the sprint. The development team decides how to accomplish the
work of the sprint. All projects and sprint planning meetings are unique.
3. Add estimates as story points to the issues. We will arbitrarily say that add item 1 is 1 point, add
item 2 is 2 points and add item 3 is 4 points.
Click on each issue in the product backlog and add its estimate under the Story point
estimate field.
The development team usually is responsible for estimating story points. Story points are
relative units indicating the effort involved in completing the issue.
4. Prioritize the product backlog. We will arbitrarily give the 2 point story ( add item 2 ) the highest
priority and the 4 point story the lowest priority.
Drag and drop the stories into their correct order in the backlog. (With add item 2 at the
top.)
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
2. The Board tab should be selected, and you should see the board for your current sprint. Notice that
you have two issues in the TO DO column. Notice that the other columns are IN PROGRESS and
DONE . Notice the sprint goal under the sprint name. Notice the the story point estimate is shown on
the cards.

Lab: Configure a Company-managed Kanban Board
Estimated time: 25 minutes
In this lab, you will:
1. Move issues through a workflow.
2. View the default kanban workflow.
3. View the board's current column configuration.
4. Add a Review column to the board.
5. Verify that your Review column is working.
6. Configure board cards.
Note: These instructions assume you have created a projectA company-managed kanban project
with issues.
1: Move issues through a workflow.
1. Log into Jira (if necessary). https://[your site name].atlassian.net
2. Navigate to your projectA project. This is your company-managed kanban project. These
instructions DO NOT APPLY to team-managed projects.
3. Click on the Kanban board tab in the sidebar to view your board (if necessary, click the Back to
project link first). This board was automatically created when you created the project and selected
Kanban for the project template.
4. You should see three issues on the board from the previous company-managed kanban lab.
5. Drag issues to new columns.
6. Click on an issue to open its details. Notice that the dropdown value in the upper right matches the
name of the column on the board. This is the Status field value of the issue. Change the status
value. Close the issue details and notice that your issue has changed columns on the board.
7. Again view an issue's details. Notice that the Assignee field is Unassigned . Click on the
Unassigned value and select Assign to me. This lets the team know that you are responsible for
working on the issue in this status. Close the issue details and notice that your user avatar appears
with the issue on the board.
Congratulations, you have moved issues through a workflow, both by dragging and dropping and by
changing the issue's status field value.
2: View the default kanban workflow.
1. While viewing your projectA project, click on the Project settings tab in the sidebar. The scope
of these settings is limited to the project.
2. Click on the Workflows tab in the sidebar to view the workflow(s) for your project.
3. You should see one workflow. Click on the (View as) diagram link to view the workflow. Notice that
the workflow contains the four default statuses of projects created with the kanban template. Also
notice that when you create an issue, its status will automatically be set to Backlog (as indicated

by the circle pointing to it). The All boxes means that all of the other statuses in the workflow can
transition to this status.
4. Close the workflow diagram.
Congratulations, you have viewed a diagram of the default kanban workflow.
3: View the board's current column configuration.
Note: The set of columns on a kanban board are related to the workflow that your issues go through.
To add a column with a new status, you must be a project administrator for the project.
1. (You can skip this step if you are on the free plan, because all users of a site are project
administrators for all projects.) Add yourself as a project administrator for the project:
With your project selected, click Project settings.
Select People.
(If the "Add people" button is disabled, you are on the free plan and can skip this step) Click
Add people and add yourself (begin typing in your name) with a role of Administrators .
2. Navigate out of project settings and view the kanban board for the project.
3. Click the ... (more) button in the upper right and select Board settings.
4. Click the Columns tab.
5. Notice that the four columns of the board are shown in the order that they appear on the board.
6. Below the horizontal bar in each column, you should see the workflow status name for the column.
The color of the status name represents the category of the status. The BACKLOG and SELECTED
FOR DEVELOPMENT status names are gray, which means that issues with these statuses have a
category of To Do . The IN PROGRESS status name is blue, indicating that issues with this status
have a category of In Progress . The DONE status name is green, indicating that issues with this
status have a category of Done .
Congratulations, you have viewed the board's current configuration.
4: Add a Review column to the board.
1. Under the Columns tab of your board settings, verify that the Add status button is enabled. Even
though we won't click this button directly in this lab, you need to have the permissions to add a
status to the workflow. If the Add status button is not enabled, you need to add yourself as a project
administrator for the project. These steps do not apply if you are using the free plan.
With your project selected, click Project settings.
Click People.
Click Add people and add yourself (type in your email address to find yourself) with a role of
Administrators .
Navigate back to the board settings for your board and verify that the Add status button is
now enabled.
2. Under the Columns tab of your board settings, click the Add column button.

3. In the Add column window, name the column Review and specify a category of In Progress .
Click Add to add the column to the board.
4. You should now see the Review column before the Done column. Below the blue bar, you should
see that Jira has created a REVIEW status for you, matching the name of your column. The text of
the REVIEW status is blue, indicating that the category for the REVIEW status is In Progress . In
the REVIEW status, the Set resolution checkbox should remain UNCHECKED. Checking this would
set an issue's resolution field when it is moved to the Review status. We don't want to check
this, because checking it would mean that issues in this status were resolved or closed.
5. Click the Back to board link in the upper right. You should see the Review column on your board.
Congratulations, you have added a column to your board.
5: Verify that your Review column is working.
1. On your board, drag issues to the Review column.
2. View an issue's details and change the Status to and from a value of Review . The issue should
move to the new column on the board.
3. From the board, open any issue. In the dropdown in the upper right, change the status of an issue to
Done . Notice that a checkmark and Done indicator are shown next to the status. This indicates that
the Resolution field is set to Done . Change the status to Review . Notice that the Done
checkmark and indicator are gone. This is because we didn't check the Set resolution checkbox
when configuring the Review column. The Resolution field is cleared.
4. Using the same procedure that you used earlier, view the workflow diagram under Project settings.
You should see the Review status. You should also see that all other statuses are allowed to
transition to Review . Jira added this status to the workflow when you added the Review column.
The actual order of the statuses in this diagram does not matter, since all statuses are allowed to
freely transition to other statuses. The order on a board is specified in board settings.
5. Navigate back to your board.
Congratulations, you have verified that your Review column is working.
6: Configure board cards.
1. View a card on your board and identify all of the fields that are displayed.
2. Add the created field to the cards, which will display the date and time that the issue was created:
Under the Card layout tab of your board settings, add the Created field to the cards. Click
the Add button.
3. View your board. You should see the created date on all cards.
4. Use the Card colors tab of board settings to show a vertical color bar based on the issue's
assignee:
Change the Colors based on field to Assignees .
View your board.

5. Undo the previous two changes to the cards on your board.
Congratulations, you have configured board cards and completed this lab.
Copyright © 2021 Atlassian


Lab: Configure a Team-managed Kanban Board
Estimated time: 15 minutes
Note: This lab is optional. If you are not interested in working with team-managed projects, you can
skip this lab.
In this lab, you will:
1. Move issues through a workflow.
2. Add a Review column to the board.
3. Verify that your Review column is working.
Note: These instructions assume you have created a projectAteam team-managed kanban project
with issues.
1: Move issues through a workflow.
1. Log into Jira (if necessary). https://[your site name].atlassian.net
2. Navigate to your projectAteam project (click the Projects dropdown in the top navigation). This is
your team-managed kanban project. These instructions DO NOT APPLY to company-managed
projects.
3. Click on the Board tab in the sidebar to view your board. This board was automatically created when
you created the project and selected Kanban for the project template.
4. You should see three issues on the board from the previous team-managed kanban lab.
5. Drag and drop issues to new columns.
6. Click on an issue to open its details. Notice that the dropdown in the upper right matches the name
of the column on the board. This is the value of the Status field for the Jira issue. Change the status
value. Close the issue details and notice that your issue has changed columns on the board.
7. Again view an issue's details. Notice that the Assignee field is Unassigned . Click on the
Unassigned value and select Assign to me. This lets the team know that you are responsible for
working on the issue in this status. Close the issue details and notice that your user avatar appears
with the issue on the board.
Congratulations, you have moved issues through a workflow, both by dragging and dropping and by
changing the issue's status field value.
2: Add aReview column to the board.
1. To create a column, click on the plus sign (+) the right of the DONE column. This feature is available
to administrators of the board and to Jira administrators. The user that created the board is
automatically an administrator of the board. In the free version of Jira, all users can administer the
board.
2. Name the column Review and click the check mark.
3. Drag the header of the REVIEW column so that DONE is the last column on the board.

Congratulations, you have added a column to your board.
3: Verify that your Review column is working.
1. On your board, drag issues to the Review column.
2. View an issue's details and change the Status to and from a value of Review . The issue should
move to the new column on the board.
Congratulations, you have verified that your Review column is working.
Copyright © 2021 Atlassian

Lab: Kanban (Company-managed)
Estimated time: 20 minutes
In this lab, you will:
1. Configure a kanban board to use a separate backlog.
2. Assign work in progress limits on kanban board columns.
3. Add a "Development Done" column as a queue.
4. View a cumulative flow diagram.
5. View a cycle time control chart.
Note: These instructions assume that you have created a company-managed kanban projectA
project. They also assume that you are a project administrator for the project (see the previous lab).
1: Configure a kanban board to use a separate backlog.
1. In your company-managed projectA project, move some issues to the BACKLOG column of your
kanban board.
2. Navigate to the board settings (... > Board settings) .
3. Click the Columns tab.
4. Drag the BACKLOG status (the box at the bottom of the Backlog column- not the column itself)
from the first column to the Kanban backlog section on the left. You should now see the BACKLOG
status in the kanban backlog and the Backlog column of the board should not contain any
statuses.
Note: You can drag any status(es) except DONE to the kanban backlog. The status does not
have to be named BACKLOG .
5. View your kanban board. You should now see SELECTED FOR DEVELOPMENT as the first column. The
BACKLOG column has been moved to the kanban backlog.
6. Click on the Backlog tab (this was added by Jira when you enabled the kanban backlog).
7. Move issues between the backlog and the first visible column on the kanban board ( Selected for
Development ). This is where you can work on the backlog while the rest of the team is focussing on
the issues that are ready to be worked on.
Congratulations, you have configured a kanban backlog.
2: Assign work in progress (WIP) limits on kanban board columns.
Work in progress limits help ensure that started work gets finished and allows the team to easily see
bottlenecks in their workflow. You must be a project administrator or board administrator to specify
WIP limits. Project administrators are specified under the People tab of Project settings. Board
adminstrators are configured under the Administrators heading of the General tab in Board settings.
1. From your projectA kanban board, click the ... button and select Board settings.
2. Click the Columns tab.

3. Verify that the Column Constraint is set to Issue Count .
4. In the Selected for Development column, specify a minimum issue count of 2 . This means that
the column will be highlighted if there are less than two issues in the column, notifying the team that
more issues need to be added to the column.
5. In the In Progress column, specify a maximum issue count of 2 . This means that the column
will be highlighted if there are more than two issues in the column, notifying the team that there is
too much work-in-progress in that column.
6. Click Back to board.
7. You should now see a Min 2 indication in the Selected for Development column and a Max 2
indication in the In Progress column. These are the WIP limits.
8. Drag issues to the columns to violate the constraints. You may need to change the status of issues
in the backlog. You should see a highlighted column when the minimum or maximum constraint is
violated.
Congratulations, you have created WIP limits.
3: Add a "Development Done" column as a queue.
Right now, your kanban board should have a Review column before the Done column (the previous
lab added a Review column). In this part of the lab, you will add a Development Done column
before the Review column. This is so that an issue can be moved to Development Done when the In
Progress work is complete. When a reviewer is ready for another issue, they can pull the issue from
the Development Done column. This prevents a developer from pushing an issue into the Review
column directly.
1. Using a procedure similar to the previous lab, add a Development Done column (which also adds a
status) to your kanban board. Make sure to drag it to the column before Review .
2. Using a procedure similar to this lab, set a WIP limit of Max 2 for the Development Done column.
3. Test that your new column is working as expected.
Congratulations, you have added a queue to your board.
4: View a cumulative flow diagram.
1. Move all issues of the project to the Done column.
2. Click on the Reports tab in the sidebar.
3. Click on Cumulative Flow Diagram. Notice that Jira automatically creates reports for you. This
report might not look that great, but it shows the changing of issues' status that you have done so
far.
4. Zoom into any section of the report by clicking and dragging the cursor across the top chart or the
small chart below it. You can double-click on the small chart to reset the top chart.
Congratulations, you have viewed a cumulative flow diagram.

5: View a cycle time control chart.
1. Click on the Control Chart tab.
2. View the chart. This shows the cycle time for the issues of the project. This is the time between
when an issue is moved from the backlog to In Progress until the time that the issue is moved to
the Done column. Use the controls below the chart to change the horizontal timeframe of the chart.
This chart also might not look that great. A continuously improving team should show a cycle time
that decreases over time.
3. Explore the other reports related to your kanban project. Jira provides a lot of ways to analyze what
your team is doing.
Congratulations, you have viewed a cycle time control chart and completed this lab.
Copyright © 2021 Atlassian

Lab: Kanban (Team-managed)
Estimated time: 10 minutes
In this lab, you will:
1. Turn on the backlog feature.
2. Create a WIP (work in progress) limit.
Note: This lab is optional. If you are not interested in working with team-managed projects, you can
skip this lab.
Note: These instructions assume that you have created a team-managed kanban projectAteam
project.
1: Turn on the backlog feature.
Notice that by default, there is no separate backlog for a team-managed kanban project. The separate
backlog is implemented as a feature in team-managed projects. Features are turned on by the project
team as they are needed. Features are turned on under Project settings for the project.
Note: As an alternative to creating a separate backlog, as we will do here, you could create a Backlog
column on the board, similar to creating the Review column in the previous lab. Unlike turning on the
backlog feature, this creates a Backlog status.
1. Navigate to your projectAteam project.
2. In the sidebar, click Project settings and then Features.
3. Browse through the list of features. Notice, that some features are already turned on, some are off
and some may be disabled (grayed out).
4. Turn on the Backlog feature for this project by clicking the slider. The slider should turn green
(assuming it wasn't already turned on).
5. Navigate back to the board and notice that there is now a Backlog tab in the sidebar. This is a
separate location for issues. You may be prompted to move issues in your first column to the
backlog. If so, select yes. This will move the issues to the backlog. It does not change their status. In
team-managed projects, the backlog is a location for issues, not a status. Issues with any status can
be in the backlog.
6. Click on the Backlog tab in the sidebar. Notice the following:
You can view all of the issues that are on the board and in the backlog.
You can move issues from the board to the backlog. Notice that this doesn't change the
issue's status. The separate backlog is a location, not a status.
You can move issues from the backlog to the board. An issue's status is not changed.
You can create issues on the board or in the backlog. The created issues by default will have
the status of the first column on the board ( To Do in our case).
To the right, you can see the circled number of issues in each general category. Gray means
to do , blue means in progress and green means done . (Categories were discussed in
more detail in a previous lab.)
7. Move issues between the backlog and the board. This is where you can work on the backlog while
the rest of the team is focussing on the issues that are ready to be worked on.

Congratulations, you have turned on the backlog feature.
2: Create aWIPlimit.
Work in progress limits help ensure that started work gets finished and allows the team to easily see
bottlenecks in their workflow. You must be a project administrator or Jira administrator to specify WIP
limits. Project administrators are specified under the People tab of Project settings.
1. From your projectAtea, board, highlight the heading for the In Progress column, select ... and
select Set column limit.
2. Under Maximum issues, specify 2 . This means that the column will be highlighted if there are
more than two issues in the column, notifying the team that there is too much work-in-progress in
that column. Click Save.
3. You should now see a Max: 2 indication in the In Progress column. This is the WIP limit.
4. Drag issues to the column to violate the constraint. You may need create issues or move them out of
the backlog. You should see a highlighted column when the maximum constraint is violated.
At the time of this writing, minimum WIP limits are not a feature of team-managed boards.
Congratulations, you have created a WIP limit and completed this lab.
Copyright © 2021 Atlassian

Lab: Configuring Issues (Team-managed Projects)
Estimated time: 15 minutes
In this lab, you will:
1. Add labels to issues.
2. Search for issues by label.
3. Turn on estimation and enter story points.
4. Create a custom field.
Note: These instructions assume that you have created a team-managed kanban project named
projectAteam in an earlier lab.
These instructions DO NOT APPLY to company-managed projects.
1: Add labels to issues.
1. Add labels named refactor and/or database to some of the issues in projectAteam. If you
hover over an issue's card on the board, you can click on the more icon (...) and select Add label.
You could also do this by adding entries to the Labels field of an issue. Make sure to click the
checkmark to add the label.
2. View your board to verify that the labels appear. Team-managed project cards are automatically
configured to show labels.
Congratulations, you have added labels to issues.
2:Search for issues by label.
1. Open an issue with a label of database.
2. Under Labels, click on the database label. You should be brought to the Filters area with a search
for all issues with the database label. This is the easiest way to search for issues with a certain
label.
3. Use basic search to search for issues with a label of refactor. You will have to use the More
dropdown to add Label as a search criteria.
Congratulations, you have searched for issues by label.
3: Turn on estimation and enter story points.
1. While in your projectAteam project, click Project settings > Issue types.
2. If Story does not show as an issue type, click + Add issue type and add Story.
3. Create an issue of type story, with a summary of add item X , where X is the next item number for
your board.
4. Open the new story and verify that Story Point Estimate is not shown. This is because story points
are not commonly used in kanban projects and the estimation feature is turned off.
5. Click on the more icon (...) in the upper right and select Configure. You are brought to the Project
settings > Issue types > Story screen. Notice that Story Points are not present. This is because the

estimation feature is not enabled.
6. While in your projectAteam project, navigate to Project settings > Features and turn on
Estimation.
7. From the board, open the story and verify that there is now a Story point estimate field. Enter a
story point value for the issue.
8. Navigate to Project settings > Issue types > Story and notice that Story point estimate is now a
primary field. This is because you turned on the Estimation feature.
Congratulations, you turned on estimation and entered story points.
4: Create a custom field.
1. From your projectAteam project board, open an issue of type Story.
2. Click on the more icon (...) in the upper right and select Configure. This takes you to Project
settings > Issue types > Story.
3. In the toolbar on the right, click the Short text icon under CREATE A FIELD.
4. The field will be added under Context fields.
5. Enter a new field named Acceptance Criteria . For Describe how people should use this field,
enter A list of user-centered tests that must pass for the story to be considered
done. .
6. Drag and drop to reorder the fields as desired.
7. Click Save changes.
8. Verify that your new Acceptance Criteria field is shown when you view a story's details. In the text
area, enter something like User must be able to enter an email address. .
9. Open the create issue dialog and verify that your Acceptance Criteria field is available when
creating issues.
This new Acceptance Criteria field only applies to the projectAteam project. Unlike with
company-managed projects, adding a custom field to a team-managed project is not a global
configuration. This keeps each project configuration separate and in control of the project team.
10. Perform an advanced/JQL search for issues with an Acceptance Criteria field that is not empty.
Type A and notice that there are now two Acceptance Criteria field choices (assuming you did the
company-managed version of this lab). One of those choices is the globally configured field from
the company-managed lab and the other is the field created in this lab. You can query for one of
those choices by selecting from autocomplete, or query for all issues that have a non-empty
Acceptance Criteria field using "Acceptance Criteria" is not EMPTY .
Congratulations, you have created a custom field and completed this lab.
Copyright © 2021 Atlassian

Lab: Configuring Issues (Team-managed Projects)
Estimated time: 15 minutes
In this lab, you will:
1. Add labels to issues.
2. Search for issues by label.
3. Turn on estimation and enter story points.
4. Create a custom field.
Note: These instructions assume that you have created a team-managed kanban project named
projectAteam in an earlier lab.
These instructions DO NOT APPLY to company-managed projects.
1: Add labels to issues.
1. Add labels named refactor and/or database to some of the issues in projectAteam. If you
hover over an issue's card on the board, you can click on the more icon (...) and select Add label.
You could also do this by adding entries to the Labels field of an issue. Make sure to click the
checkmark to add the label.
2. View your board to verify that the labels appear. Team-managed project cards are automatically
configured to show labels.
Congratulations, you have added labels to issues.
2:Search for issues by label.
1. Open an issue with a label of database.
2. Under Labels, click on the database label. You should be brought to the Filters area with a search
for all issues with the database label. This is the easiest way to search for issues with a certain
label.
3. Use basic search to search for issues with a label of refactor. You will have to use the More
dropdown to add Label as a search criteria.
Congratulations, you have searched for issues by label.
3: Turn on estimation and enter story points.
1. While in your projectAteam project, click Project settings > Issue types.
2. If Story does not show as an issue type, click + Add issue type and add Story.
3. Create an issue of type story, with a summary of add item X , where X is the next item number for
your board.
4. Open the new story and verify that Story Point Estimate is not shown. This is because story points
are not commonly used in kanban projects and the estimation feature is turned off.
5. Click on the more icon (...) in the upper right and select Configure. You are brought to the Project
settings > Issue types > Story screen. Notice that Story Points are not present. This is because the

estimation feature is not enabled.
6. While in your projectAteam project, navigate to Project settings > Features and turn on
Estimation.
7. From the board, open the story and verify that there is now a Story point estimate field. Enter a
story point value for the issue.
8. Navigate to Project settings > Issue types > Story and notice that Story point estimate is now a
primary field. This is because you turned on the Estimation feature.
Congratulations, you turned on estimation and entered story points.
4: Create a custom field.
1. From your projectAteam project board, open an issue of type Story.
2. Click on the more icon (...) in the upper right and select Configure. This takes you to Project
settings > Issue types > Story.
3. In the toolbar on the right, click the Short text icon under CREATE A FIELD.
4. The field will be added under Context fields.
5. Enter a new field named Acceptance Criteria . For Describe how people should use this field,
enter A list of user-centered tests that must pass for the story to be considered
done. .
6. Drag and drop to reorder the fields as desired.
7. Click Save changes.
8. Verify that your new Acceptance Criteria field is shown when you view a story's details. In the text
area, enter something like User must be able to enter an email address. .
9. Open the create issue dialog and verify that your Acceptance Criteria field is available when
creating issues.
This new Acceptance Criteria field only applies to the projectAteam project. Unlike with
company-managed projects, adding a custom field to a team-managed project is not a global
configuration. This keeps each project configuration separate and in control of the project team.
10. Perform an advanced/JQL search for issues with an Acceptance Criteria field that is not empty.
Type A and notice that there are now two Acceptance Criteria field choices (assuming you did the
company-managed version of this lab). One of those choices is the globally configured field from
the company-managed lab and the other is the field created in this lab. You can query for one of
those choices by selecting from autocomplete, or query for all issues that have a non-empty
Acceptance Criteria field using "Acceptance Criteria" is not EMPTY .
Congratulations, you have created a custom field and completed this lab.
Copyright © 2021 Atlassian

Lab: Filters
Estimated time: 30 minutes
In this lab, you will:
1. Explore default filter queries.
2. Create a starred filter.
3. Explore and create quick filters.
4. Explore existing board filters.
5. Create a board.
Note: These instructions assume that you have projects from the previous labs. If you have other
projects, you can modify the queries to make them work for your projects.
1: Explore default filter queries.
1. Click on the Filters tab. You may need to click the Jira icon in the upper left to see it.
2. Click on each of the tabs/filters to view and execute each query. In JQL search, view the JQL and
explore any fields and/or functions that you are not familiar with. Notice that some of the queries can
not be displayed with basic search, because the user interface elements don't support the query.
Congratulations, you have explored the default filter queries.
2: Create a starred filter.
1. In basic or JQL search, create and execute a query that searches for all issues with a
statusCategory of In Progress that are assigned to the currentUser()``. (If the search
returns no issues, you may want to move an issue to the In Progress or Review column
in projectA` and assign yourself to the issue.)
Using "statusCategory" in this query instead of "status" has the advantage of including issues in
any column where the work is in progress, such as the Review column that you created in the
earlier lab. There are only three statusCategories: To Do, In Progress and Done, so this is a very
flexible query if teams add columns/statuses to the boards.
2. Click the Save as link to save the query as a filter. Name the filter My in progress . After you
create the filter, it should show under the Starred category in the sidebar. You may need to refresh
your browser to see it.
3. In Filters click the View all filters tab. This tab is at the bottom of the sidebar. You should see your
My in progress filter in the list of filters.
4. Click on the more (...) icon to the right of your new filter and select Edit. View and change any of the
metadata details if you would like.
5. Execute the filter by clicking on it. Change the query slightly (for example, swap the order of the
fields) and re-save the filter.
6. Experiment with creating other filters.
Congratulations, you have created and edited a starred filter.

3: Explore and create quick filters.
1. View your projectA company-managed kanban board.
2. Enter some text in the text search box below the board name to show only issues containing that
text.
3. Clear the search text and click on your user icon at the top to view only your issues.
4. Click on your user icon to clear the user filter and use the quick filters to the right of the user icons
to change the issues viewed on the board.
5. Navigate to board settings and view the quick filters for the board (under the Quick Filters tab).
6. Add a quick filter named Stale Issues that displays non-done issues that have not been updated
in the last day. (Hint: updated < -1d AND statusCategory != Done ). It is a good practice to test
your JQL in advanced/JQL search before placing it in a user interface element that expects JQL.
7. Verify that your quick filter is working by navigating back to the board and clicking on Stale
Issues . You may need to change the query and/or issues' status to see results.
8. Experiment with creating other quick filters.
9. (Optional) View your projectAteam team-managed board. You can filter by entering text or
clicking on a user's icon. Quick filters (and the features in the rest of this lab) are currently not
available for team-managed projects.
Congratulations, you have explored and created quick filters.
4: Explore existing board filters.
1. Navigate to the kanban board for projectA .
2. In the board's settings, navigate to the General tab.
3. Under the Filter heading, view the name of the filter used as the board's filter. View the associated
Filter Query, also under the Filter heading.
4. Click Edit Filter Query. You will be brought to Filters with the board's filter executed. These are the
issues that appear on the board.
5. Under Filters, scroll down and click View all filters. Notice that the board's filter is a standard filter.
Also notice that it is not starred. This is because board filters are usually not useful as standalone
queries.
Congratulations, you have explored existing board filters.
5: Create a board.
1. Create a board's filter using the steps below. This board will be used to show all issues that are in
projectA or projectB .
Navigate to View all filters.
Copy the board's filter for projectA by selecting its More icon (...) and selecting Copy filter.
Name the filter Projects A and B . We will use this filter as a starting point for our new

board's filter.
Using JQL search, modify and save the query so that it meets the requirements described
above. Reuse the ORDER BY clause from the board filter for projectA . Hint: Here is a query
that would work: project in (projectA, projectB) ORDER BY Rank ASC .
2. Create a board in your profile:
From your projectA project, click the board dropdown under the project name in the
sidebar.
Click Create board.
Click Create a Kanban board. (Notice that you could create a new board with sample data.
This will create a new project in your account. This is good for looking at reports with more
realistic data than what we have seen in this course.)
In Create a board, select Board from an existing Saved Filter. Click Next.
In Name this board, name the board Projects A and B and select your Projects A and
B saved filter. Set the location to your profile (under Personal).
Click Create board. You should see your new board. You can also find the board using the
VIEW ALL link that you saw when creating the board.
3. View the board's settings and verify that the filter that you created above is being used as the
board's filter.
4. Configure the board's columns.
Click the Columns tab in the board's settings. Notice that the columns of the board are the
same names as the three statusCategory values (To Do, In Progress, Done). The statuses in
each column are arranged by statusCategory.
Notice that multiple statuses are included in a single board column. If you would like, you
could create a Review column on the board and move the Review status to that column. You
could also do this for other statuses.
5. View your new board and verify that it looks and behaves as expected. You should see issues from
both of your projects.
6. Verify that your board is accessible in your profile. Click your user icon and select Your boards or
Personal boards.
7. Change the board's location to the projectA project. You can change this under the General tab
for the board's settings (under Location). Verify that projectA now has two boards. Use the board
switcher dropdown in the upper left to switch between boards.
8. Move your new board back to your user profile.
Congratulations, you have created a board containing issues that span multiple projects and
completed this lab.
Copyright © 2021 Atlassian

Lab: JQL
Estimated time: 30 minutes
In this lab, you will:
1. Create a basic search and view the JQL query.
2. Create JQL queries with the help of autocomplete and column sorting.
3. Use functions as values.
4. Use time unit qualifiers.
5. Use various operators.
6. Use Boolean operators.
Note: These instructions assume that you have projects from the previous labs. If you have other projects, you
can modify the queries to make them work for your projects.
1:Createabasicsearchandview theJQLquery.
1. Open basic search by clicking on Filters. If needed, click on the Switch to basic link to view basic search.
2. In basic search, search for all issues of projectA .
3. Click on the Switch to JQL link to enter advanced/JQL search. View the JQL query associated with the
basic search. You can use this technique of switching from basic to advanced/JQL search to help "write"
JQL queries. This is helpful because you might need to copy the JQL to other parts of the Jira interface (or
to other products like Confluence).
4. Click on column headers in list view to sort the results. Notice the changes to the query.
5. Experiment with creating other basic searches and viewing the resulting JQL query.
Congratulations, you have created a basic search and viewed the resulting JQL query.
2:CreateJQLqueries withthehelpofautocompleteandcolumnsorting.
1. Enter advanced/JQL search (if necessary).
2. Clear the current JQL query.
3. Create and execute a query that finds all issues in the projectA project:
With the JQL textbox selected, press p and select project from the autocomplete dropdown.
Press the space bar to view operator autocomplete.
Select the equals (=) operator.
Press the space bar to view value autocomplete.
Select projectA .
Press Enter to execute the query.
4. Add an ORDER BY clause to the query by clicking on the Summary heading in list view.
5. Experiment with creating other JQL queries.
Congratulations, you have created JQL queries with the help of autocomplete and column sorting.

3:Usefunctionsasvalues.
1. In advanced/JQL search, use autocomplete to find all issues assigned to you using the currentUser()
function. assignee = currentUser()
2. Find all issues that were created since the startOfWeek() . You will use the > operator.
3. In a separate browser window, perform a web search for Jira advanced searching functions
reference . Click on the Atlassian documentation link. Click on Cloud in the upper right. View the
available advanced/JQL searching functions.
4. Back in Jira, experiment with other searches that use functions as values.
Congratulations, you have used functions as values.
4:Usetimeunitqualifiers.
1. In advanced/JQL search, enter the query updated > -2d to find issues that were updated in the past 48
hours.
2. Modify the previous query to find issues updated in the past two hours.
3. Using basic search (you may need to clear the existing advanced/JQL search and press Enter to enable the
basic search link), find all issues that were updated in the past hour. Switch to advanced/JQL search and
notice that a time unit qualifier is used in the query. This is a helpful way to write queries with time unit
qualifiers.
4. In advanced/JQL search, find all issues that were updated yesterday or today. (Hint: use the startOfDay()
function with an argument of a time unit qualifier of -1d .)
5. Experiment with other searches that use time unit qualifiers.
Congratulations, you have used time unit qualifiers.
5:Usevariousoperators.
1. In advanced/JQL search, enter assignee and press the space bar to view the available operators.
2. Select the is operator and press the space bar. Notice that the only valid value is EMPTY . Select it.
3. Execute the query to find all unassigned issues.
4. Execute the query text ~ "item 1 NOT 2" to find issues with text fields that contain item and 1
but not 2 .
5. Modify the previous query to capitalize ITEM and verify that text strings are not case-sensitive.
6. Modify the previous query to change not to lowercase and verify that the query results are different. The
NOT keyword in text field searches is case-sensitive. This query is the same as item 1 2 and probably
returns no issues because no issues have a 1 and a 2.
7. In a separate browser window, perform a web search for Jira advanced searching operators
reference . Select the Atlassian documentation. Click on Cloud in the upper right. Explore the reference.

8. Back in Jira, experiment with using other operators.
Congratulations, you have used various operators.
6:Use Booleanoperators.
1. In advanced/JQL search, use a Boolean operator to find issues with an assignee of currentUser()
and a status of Done .
2. Use the NOT Boolean operator to find issues that do not have a status of Backlog . Verify that this
query is equivalent to status != Backlog .
3. Use the OR operator to find issues with a status of Selected for Development or In Progress .
4. Create a query that is equivalent to the previous query using the in operator. (See answer at the end of
lab.)
5. Create a query containing multiple Boolean operators that returns different results depending on if you use
parentheses in the query. Examples: NOT (project = projectA OR project = projectB)
(status = Done OR status = "To Do") AND summary ~ "item 1" .
6. Experiment with other Boolean operators.
Congratulations, you have used Boolean operators and completed this lab.
Answer to 6.4: status in ("Selected for Development", "In Progress")
Copyright © 2020 Atlassian

Lab: Quick Search and Basic Search
Estimated time: 20 minutes
In this lab, you will:
1. Perform quick searches.
2. Perform basic searches.
3. Work with search results.
Note: These instructions assume that you have projects from the previous labs. If you have other
projects, you can change the search to provide results for your project.
1:Perform quick searches.
1. Click in the search box in the upper right to view quick search. Notice that you have access to recent
issues, boards, projects and filters.
2. Search for "item". As you type, the search results will change. This searches issues with fields of
types text, board names, filter names and project names. Press Enter. You will be taken to the
Filters section with the associated text-based search of issues.
3. Use quick search to search for "item 2".
4. Search for "ITEM 2" and verify that search terms are not case-sensitive.
5. Search for "item AND 2". The results should be the same as the previous search. The terms of a
query are joined with AND by default.
6. Search for "item NOT 1". The NOT keyword should exclude the "add item 1" issues.
7. Search for "item not 1". This should return the "add item 1" issues. This is because "not" is in
lowercase, and it is such a common word that it is excluded from the search (a reserved or stop
word). This is the same as searching for "item 1".
8. In another browser window or tab, perform a general web search for "Jira search syntax for text
fields". Click on the Atlassian documentation. Click on Cloud in the upper right. Scroll down to the
"Reserved words" heading and verify that "and" and "not" are reserved words for searches of text
fields.
9. Back in Jira, perform any quick searches that interest you.
Congratulations, you have performed quick searches.
2:Perform basic searches.
1. Click the search box in the upper right and select Advanced issue search. This takes you to the
Filters section of your site.
2. Click the All issues tab on the left. You should be viewing all of the issues of the projects in your
site.
3. Verify that you are in the basic search. You should see a row of interface elements under All issues
and a Switch to JQL link to the right. If you see a Switch to basic link, click on it to change from
JQL to basic search.

4. Click on the Project dropdown in the row of interface elements to view the issues of any one of your
projects.
5. Use the Contains text box in the basic search row to further limit your results. Press Enter or click
on the search hourglass to perform the search. Verify that the NOT keyword works in the basic
search.
6. Use quick search (like you did earlier in the lab) to type in "item" and click Enter. You should be
brought to *Filters area with basic search. Verify that the text that you entered is in the textbox.
7. Clear the existing search by clicking Search issues or All issues in the sidebar.
8. In basic search, click on the More dropdown and search for issues that have been updated
(Updated Date field) in the last hour, day and week. Your results depend on when you performed
the previous labs.
9. Perform any basic searches that interest you.
Congratulations, you have performed basic searches.
3:Work with search results.
1. Toggle between List View and Detail View using the Change View icon to the right of the basic
search elements.
2. In List View, click on the Columns dropdown to change the columns that are displayed in the results.
Click Restore defaults to undo what you have changed.
3. Reorder the first two columns by dragging and dropping the column header. Change it back.
4. Click on a column header to sort by that column. Click on the column header again to reverse the
sorting.
5. In the basic search "Contains text" box, enter "item 2" and click Enter. Using the Share icon in the
upper right, email yourself a copy of the search results. You should receive an email with a link to the
underlying JQL query. Click on the link in the email and you should see your search in a new browser
window. Close the new browser window.
6. In the original browser window, click on the Export icon in the upper right. Select Export XML. You
should see the XML search results. View the issues' field names and values under an item. If the
XML displayed in your browser window, click the browser's back button to navigate back to Jira.
7. Change the Assignee of all of the issues of the project:
Search for all issues of your projectA project.
Click on the More icon (the three dots) in the upper right and select Bulk change all X
issue(s).
In step 1, select the issues that are Unassigned. (If they are all assigned, you can change this
exercise to unassigning them all.)
In step 2, select Edit Issues.
In step 3, click Change Assignee and click Assign to me.
In step 4, click Confirm.
Verify that your bulk changes were made.
8. Perform any other quick search or basic search operations that interest you.

Congratulations, you have worked with search results and completed this lab.
Copyright © 2021 Atlassian
