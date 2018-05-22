---
title: The AudioOutput Object
description: The AudioOutput Object
ms.assetid: '7c1c6079-f445-4980-9559-8d26b6014e89'
---

# The AudioOutput Object

\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]

This object provides access to audio output properties maintained by the server. The properties are read-only, but the user can change them in the Microsoft Agent property sheet.

If you declare an object variable of type [**IAgentCtlAudioObjectEx**](lwef-iagentctaudioobjectex), you will not be able to access all properties for the [**AudioOutput**](https://msdn.microsoft.com/library/windows/desktop/ms697310) object. While Agent also supports [**IAgentCtlAudioObject**](lwef-iagentctaudioobject), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.

-   [**Enabled**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Status**](status-property.md)

 

 



