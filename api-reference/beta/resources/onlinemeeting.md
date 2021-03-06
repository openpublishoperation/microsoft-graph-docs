# onlineMeeting resource type

> **Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.

Captures information about the meeting, including the join URL, the attendees list, and the description.

## Methods

| Method         | Return Type | Description |
|:---------------|:--------|:----------|
| [Get onlineMeeting](../api/onlinemeeting_get.md) | [onlineMeeting](onlinemeeting.md) | Read properties and relationships of onlineMeeting object. |

## Properties

| Property                  | Type                                                   | Description                                                                                                                |
| :------------------------ | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| accessLevel               | String                                                 | The access level that controls admission to the online meeting. Possible values are: `everyone`, `invited`, `locked`, `sameEnterprise`, `unknown`. |
| audioConferencing         | [audioConferencing](audioconferencing.md)              | Represents phone access information for an onlineMeeting. |
| canceledTime              | DateTime                                               | The time when the meeting was canceled. |
| chatInfo                  | [chatInfo](chatinfo.md)                                | The chat associated with this meeting. |
| creationTime              | DateTime                                               | The time when the meeting was created. Readonly.
| endTime                   | DateTime                                               | End time of the meeting. |
| entryExitAnnouncement     | Boolean                                                | The attendance announcements status for the online meeting. When attendance announcements are enabled, the online meeting will announce the names of the participantswho join the meeting through audio. |
| expirationTime            | DateTime                                               | The absolute Coordinated Universal Time (UTC) date and time after which the online meeting can be deleted.The day and time must be between one year before, and ten years after, the current date and time on the server. |
| id                        | String                                                 | The ID associated with the online meeting. Used in a GET HTTP request as the ID. Read-only. Server generated. |
| isCancelled               | Boolean                                                | Whether the meeting has been canceled. |
| joinUrl                   | String                                                 | The URL that is used when the online meeting is joined from the web. |
| meetingType               | String                                                 | Possible values are: `meetNow`, `calendar`, `recurring`, `broadcast` |
| participants              | [meetingParticipants](meetingparticipants.md)          | The participants associated with the online meeting.  This includes the organizer and the attendees. |
| startTime                 | DateTime                                               | Start time of the meeting. |
| subject                   | String                                                 | The subject of the online meeting. |

## Relationships
None

## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onlineMeeting"
}-->
```json
{
  "accessLevel": "everyone | invited | locked | sameEnterprise",
  "audioConferencing": {"@odata.type": "#microsoft.graph.audioConferencing"},
  "canceledTime": "String (timestamp)",
  "chatInfo": {"@odata.type": "#microsoft.graph.chatInfo"},
  "creationTime": "String (timestamp)",
  "endTime": "String (timestamp)",
  "entryExitAnnouncement": true,
  "expirationTime": "String (timestamp)",
  "id": "String (identifier)",
  "isCancelled": false,
  "joinUrl": "String",
  "meetingType": "meetNow | calendar | recurring | broadcast",
  "participants": {"@odata.type": "#microsoft.graph.meetingParticipants"},
  "startTime": "String (timestamp)",
  "subject": "String"
}
```

