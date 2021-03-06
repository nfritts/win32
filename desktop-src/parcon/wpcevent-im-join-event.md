---
Description: Per-user event generated by an Instant Messaging application when an entity attempts to join a conversation in progress in Parental Controls.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN event (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
---

# WPCEVENT\_IM\_JOIN event

Per-user event generated by an Instant Messaging application when an entity attempts to join a conversation in progress in Parental Controls.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
```



## Parameters

<dl> <dt>

*AppName* 
</dt> <dd>

The name of the application that is generating the event.

</dd> <dt>

*AppVersion* 
</dt> <dd>

The version string for the application that is generating the event.

</dd> <dt>

*AccountName* 
</dt> <dd>

The instant messaging account identity string for this user.

</dd> <dt>

*ConvID* 
</dt> <dd>

The identifier for this conversation.

</dd> <dt>

*JoiningIP* 
</dt> <dd>

A string that contains the IP address of the computer that is joining this conversation.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

The instant messaging account identity string for the user who is joining.

</dd> <dt>

*Reason* 
</dt> <dd>

A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.

</dd> <dt>

*MemberCount* 
</dt> <dd>

The count of participants who are in the conversation and who have identities defined in the member field.

</dd> <dt>

*Member* 
</dt> <dd>

A delimited string that contains instant messaging account identity strings for all current members of this conversation.

</dd> <dt>

*Sender* 
</dt> <dd>

The instant messaging account identity string for the user who is making the request to join the conversation.

</dd> </dl>

## Requirements



| Requirement | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | None supported<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## See also

<dl> <dt>

[Using Logging APIs for Parental Controls](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC\_ARGS\_CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




