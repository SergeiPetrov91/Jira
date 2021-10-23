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
