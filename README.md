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
