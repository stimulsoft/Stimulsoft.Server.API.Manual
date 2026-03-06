# REST API

REST API allows you quick and easy access to the main functions of **Stimulsoft Server** and automates user actions of the system in your application. Access points to the REST-services should be on your domain and be accessible via HTTP/HTTPS. For example, we will use the locally installed version of Stimulsoft Server with the URL **http://reports.stimulsoft.com**. A relative path begins with the prefix /1/ which means the first version of REST API.


**EndPoint**

**HTTP Verb**

**Action**

/1/login

GET

[Login registered user](Login.md)

/1/logout

DELETE

[User logout](Logout.md)

/1/signup

POST

[New user registration](Sign_Up.md)

/1/users

GET

[Getting a list of users](Users/GET_List.md)

/1/users

POST

[Creating a new user](Users/POST_Create.md)

/1/users/&lt;UserId&gt;

GET

[Getting information about the user <UserId>](Users/GET_Info.md)

/1/users/&lt;UserId&gt;

PUT

[Changing user information <UserId>](Users/PUT_Edit.md)

/1/users/&lt;UserId&gt;

DELETE

[Removing a user <UserId>](Users/DELETE.md)

/1/users/current

GET

[Getting information about the current user](Users/GET_Info.md)

/1/users/current

PUT

[Changing the current user information](Users/PUT_Edit.md)

/1/users/&lt;UserId&gt;/changepassword

PUT

[Change user password](Users/Change_password.md)

/1/users/current/changepassword

PUT

[Changing the password of the current user](Users/Change_password.md)

/1/users/&lt;UserId&gt;/resetpassword

PUT

[Initialize reset the user's <UserId>  password](Users/Reset_password.md)

/1/users/current/resetpassword

PUT

[Initialize the current user password reset](Users/Reset_password.md)

/1/resetpassword/secretcode

PUT

[Confirm password reset by a secret code](Users/Reset_password.md)

/1/roles

GET

[Getting a list of roles](Roles/GET_List.md)

/1/roles/&lt;RoleId&gt;

GET

[Getting information about the role <RoleId>](Roles/GET_Info.md)

/1/roles

POST

[Creating a new role](Roles/POST_Create.md)

/1/roles/&lt;RoleId&gt;

PUT

[Changing information about the role <RoleId>](Roles/PUT_Edit.md)

/1/roles/&lt;RoleId&gt;

DELETE

[Remove a role <RoleId>](Roles/DELETE.md)

/1/items

GET

[Getting a list of items](Items/GET_List.md)

/1/items/&lt;ItemId&gt;

GET

[Getting information about the element <ItemId>](Items/GET_Info.md)

/1/items

POST

[Create a new item](Items/POST_Create.md)

/1/items/&lt;ItemId&gt;

PUT

[Changing information about the element <ItemId>](Items/PUT_Edit.md)

/1/items/&lt;ItemId&gt;

DELETE

[Deleting an element <ItemId>](Items/DELETE.md)

/1/items/&lt;ItemId&gt;/share

GET

[Getting information about public access to the element <ItemId>](Items/Share/GET_Info.md)

/1/items/&lt;ItemId&gt;/share

PUT

[Changing data on public access to the element <ItemId>](Items/Share/PUT_Edit.md)

/1/items/&lt;ItemId&gt;/share

DELETE

[Removing an element <ItemId> from public access](Items/Share/DELETE_Reset.md)

/1/schedulers

GET

[Getting a list of schedulers](Schedulers/GET_List.md)

/1/schedulers/&lt;SchedulerId&gt;

GET

[Getting information about the scheduler <SchedulerId>](Schedulers/GET_Info.md)

/1/schedulers

POST

[Creating a new scheduler](Schedulers/POST_Create.md)

/1/schedulers/&lt;SchedulerId&gt;

PUT

[Changing information about the scheduler <SchedulerId>](Schedulers/PUT_Edit.md)

/1/schedulers/&lt;SchedulerId&gt;

DELETE

[Removal of scheduler <SchedulerId>](Schedulers/DELETE.md)

/1/schedulers/&lt;SchedulerId&gt;/status

GET

[Getting information about the state of the scheduler <SchedulerId>](Schedulers/GET_Info_Status.md)

/1/schedulers/&lt;SchedulerId&gt;/status

PUT

[Setting state of scheduler <SchedulerId>](Schedulers/PUT_Edit_Status.md)

/1/schedulers/&lt;SchedulerId&gt;/run

PUT

[Immediate start of scheduler <SchedulerId>](Schedulers/Run.md)

/1/files

GET

[Getting a list of files](Files/GET_List.md)

/1/files/&lt;FileId&gt;/

GET

[Downloading a file <FileId>](Files/GET_Download.md)

/1/files

POST

[Creating a new file](Files/POST_Create.md)

/1/files/&lt;FileId&gt;/

PUT

[Appending a new chunk to file <FileId>](Files/PUT_Append.md)

/1/files/&lt;FileId&gt;/

DELETE

[Removing a file <FileId>](Files/DELETE.md)

/1/reporttemplates

GET

[Getting a list of report templates](Report_Template/GET_List.md)

/1/reporttemplates/&lt;ReportTemplateId&gt;/

GET

[Getting information about the report template <ReportTemplateId>](Report_Template/GET_Info.md)

/1/reporttemplates

POST

[Creating a new report template](Report_Template/POST_Create.md)

/1/reporttemplates/&lt;ReportTemplateId&gt;/

DELETE

[Removing a report template <ReportTemplateId>](Report_Template/DELETE.md)

/1/reporttemplates/&lt;ReportTemplateId&gt;/run

PUT

[Build the report template and save result to another item](Report_Template/Run.md)

/1/reporttemplates/&lt;ReportTemplateId&gt;/duplicate

POST

[Creating a new copy of the report template in a workspace of the logged-in user.](../../Stimulsoft_Cloud/REST_API/Report_Template/POST_Duplicate.md)

/1/reportsnapshots

GET

[Getting a list of report snapshots](Report_Snapshot/GET_List.md)

/1/reportsnapshots/&lt;ReportSnapshotId&gt;/

GET

[Getting information about the report snapshot <ReportSnapshotId>](Report_Snapshot/GET_Info.md)

/1/reportsnapshots

POST

[Creating a new report snapshot](Report_Snapshot/POST_Create.md)

/1/reportsnapshots/&lt;ReportSnapshotId&gt;/

DELETE

[Removing a report snapshot <ReportSnapshotId>](Report_Snapshot/DELETE.md)

/1/reportsnapshots/&lt;ReportSnapshotId&gt;/export

PUT

[Export data from report snapshot](Report_Snapshot/Export.md)
