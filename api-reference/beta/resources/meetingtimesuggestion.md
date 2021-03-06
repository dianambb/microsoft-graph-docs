---
title: "meetingTimeSuggestion resource type"
description: "A meeting suggestion that includes information like meeting time, attendance likelihood, individual "
localization_priority: Normal
author: "angelgolfer-ms"
ms.prod: "outlook"
---

# meetingTimeSuggestion resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A meeting suggestion that includes information like meeting time, attendance likelihood, individual 
availability, and available meeting locations.

## JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestion"
}-->

```json
{
  "attendeeAvailability": [{"@odata.type": "microsoft.graph.attendeeAvailabilityDataModel"}],
  "confidence": 1024.0,
  "locations": [{"@odata.type": "microsoft.graph.locationDataModel"}],
  "meetingTimeSlot": {"@odata.type": "microsoft.graph.meetingTimeSlotDataModel"},
  "order": 1024,
  "organizerAvailability": "String",
  "suggestionReason": "String"
}

```
## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|attendeeAvailability|[attendeeAvailabilityDataModel](attendeeavailabilitydatamodel.md) collection|An array that shows the availability status of each attendee for this meeting suggestion.|
|confidence|Double|A percentage that represents the likelhood of all the attendees attending.|
|locations|[locationDataModel](locationdatamodel.md) collection|An array that specifies the name and geographic location of each meeting location for this meeting suggestion.|
|meetingTimeSlot|[meetingTimeSlotDataModel](meetingtimeslotdatamodel.md)|A time period suggested for the meeting.|
|organizerAvailability|availabilityStatus| Availability of the meeting organizer for this meeting suggestion. Possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.|
|suggestionReason|String|Reason for suggesting the meeting time.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/meetingtimesuggestion.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
