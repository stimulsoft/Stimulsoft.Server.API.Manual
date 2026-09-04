# Items

Items object describes the data items supported by the system. This is an abstract class that combines different types of elements. At creation of an element its type is specified in the Ident field and never changes:


| **Object** | **Description** | **Ident** |
| --- | --- | --- |
| `StiCalendarItem` | Calendar, used to create schedules. | CalendarItem |
| `StiCloudFileItem` | Cloud file, used to connect to external data files. | CloudFileItem |
| `StiCloudStorageItem` | Cloud storage, used to create directories for storing the contents of cloud items. | CloudStorageItem |
| `StiContactListItem` | Contact list, used to send data via email. | ContactListItem |
| `StiDashboardItem` | Dashboard template. | DashboardItem |
| `StiDataQueryItem` | Data Query, used to retrieve data from SQL data sources. | DataQueryItem |
| `StiDataRelationItem` | Data Relation, used to join data sources. | DataRelationItem |
| `StiDataSnapshotItem` | Data Snapsot, used to store a point-in-time copy of a dataset | DataSnapshotItem |
| `StiDataSourceItem` | Data source, used to connect to external data | DataSourceItem |
| `StiDataTableItem` | Data table, used to structure data from data sources. | DataTableItem |
| `StiExcelTableItem` | Excel table, used to structure data from Excel data sources. | ExcelTableItem |
| `StiFileItem` | File, used to connect to external data files. | FileItem |
| `StiFileStorageItem` | File storage, used to create directories for storing the contents of server items. | FileStorageItem |
| `StiFolderItem` | Folder, provides a hierarchical structure for organizing elements. | FolderItem |
| `StiReportSnapshotItem` | Report snapshot, a rendered report containing data. | ReportSnapshotItem |
| `StiReportTemplateItem` | Report template. | ReportTemplateItem |
| `StiSchedulerItem` | Scheduler, used to automate actions. | SchedulerItem |
| `StiMailingItem` | Mailing, used to automate email distribution. | MailingItem |
| `StiLinkItem` | Link, used to create a shortcut to a report or dashboard. | LinkItem |

To get the list of elements, modify the data, and to create new elements in the current workspace and removing existing elements, use command Items with various methods. Each element has a unique key, which uniquely identifies it in the list of elements. Data hierarchy as a tree is realized by an element type StiFolderItem, key element it is specified in the field of FolderKey as designation of the parental folder of an element. The identifier of this element is specified in the FolderKey of other elements and provides identification of the parent folder of an element. If this field is empty or not initialized to any value, then the element belongs to the root folder.


| **Name** | **Description** |
| --- | --- |
| [GET List](GET_List.md) | Getting a list of elements in a workspace of the logged-in user. The list is returned to the specified folder. |
| [GET Info](GET_Info.md) | Getting information about the element in a workspace of the logged-in user. |
| [POST Create](POST_Create.md) | Creating a new element in a workspace of the logged-in user. To successfully run the command you must fill in the fields Ident (assigned a value in accordance with the required type of item has one of the values listed in the table above), and Name. `FolderKey` field may contain the key of the parent folder, making sure that the element in the tree. If `FolderKey` empty or not specified, the item is displayed in the root folder. |
| [PUT Edit](PUT_Edit.md) | Changing element in a workspace of the logged-in user. This command does not allow change of the unique item key, which is used as an identifier (field Key), and the type (field Ident). Changing field `FolderKey` can move an item to another folder in the tree (the root, if you specify a null value). |
| [DELETE](DELETE.md) | Removing an element from the current workspace. However, the use of this command does not guarantee the immediate removal of the element from a tree, because the command only creates an internal task of server to delete the item and the actual deletion may be delayed for some time. |
