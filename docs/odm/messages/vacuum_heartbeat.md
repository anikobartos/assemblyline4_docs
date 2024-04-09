[comment]: # (AUTOGENERATED MARKDOWN CONTENT. UPDATES TO ODM DOCUMENTATION SHOULD BE DONE THROUGH ASSEMBLYLINE-BASE REPO!)
# VacuumMessage
> Model of Vacuum Heartbeat Message

| Field | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| msg | [Heartbeat](/assemblyline4_docs/odm/messages/vacuum_heartbeat/#heartbeat) | Hearbeat message | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |
| msg_loader | Enum | Loader class for message<br>Values:<br>`"assemblyline.odm.messages.vacuum_heartbeat.VacuumMessage"` | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `assemblyline.odm.messages.vacuum_heartbeat.VacuumMessage` |
| msg_type | Enum | Type of message<br>Values:<br>`"VacuumHeartbeat"` | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `VacuumHeartbeat` |
| sender | Keyword | Sender of message | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |


[comment]: # (AUTOGENERATED MARKDOWN CONTENT. UPDATES TO ODM DOCUMENTATION SHOULD BE DONE THROUGH ASSEMBLYLINE-BASE REPO!)
## Heartbeat
> Heartbeat Model

| Field | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| metrics | [Metrics](/assemblyline4_docs/odm/messages/vacuum_heartbeat/#metrics) | Vacuum metrics | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |


[comment]: # (AUTOGENERATED MARKDOWN CONTENT. UPDATES TO ODM DOCUMENTATION SHOULD BE DONE THROUGH ASSEMBLYLINE-BASE REPO!)
### Metrics
> Vacuum Stats

| Field | Type | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| ingested | Integer | Files ingested | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |
| safelist | Integer | Files safelisted | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |
| errors | Integer | None | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |
| skipped | Integer | None | <div style="width:100px">:material-checkbox-marked-outline: Yes</div> | `None` |

