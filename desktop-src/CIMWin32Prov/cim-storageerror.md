---
Description: 'The CIM\_StorageError class represents blocks of media or memory space that are mapped out-of-use due to errors. The key of the class is the StartingAddress property of the bytes in error.'
audience: developer
author: 'REDMOND\\markl'
manager: 'REDMOND\\markl'
ms.assetid: 'e786aa39-4718-416b-b659-bf4b8d3e2851'
ms.prod: 'windows-server-dev'
ms.technology:
- cimwin32
- 'windows-management-instrumentation'
ms.tgt_platform: multiple
title: 'CIM\_StorageError class'
---

# CIM\_StorageError class

The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors. The key of the class is the **StartingAddress** property of the bytes in error.

> \[!Important\]  
> The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built. WMI currently supports only the [CIM 2.x version schemas](Http://Go.Microsoft.Com/FWLink/p/?LinkID=309367).

�

The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties. Properties are listed in alphabetic order, not MOF order.

## Syntax

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## Members

The **CIM\_StorageError** class has these types of members:

-   [Properties](#properties)

### Properties

The **CIM\_StorageError** class has these properties.

<dl> <dt>

**DeviceCreationClassName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (256), [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")
</dt> </dl>

Scoping storage extent's creation class name.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (64), [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")
</dt> </dl>

Scoping storage extent's device identifier.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Ending address of the bytes in error.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157)
</dt> </dl>

Starting address of the bytes in error.

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/aa389763).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (256), [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")
</dt> </dl>

Scoping system's creation class name.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**Key**](https://msdn.microsoft.com/library/aa392157), [**MaxLen**](https://msdn.microsoft.com/library/aa393650) (256), [**Propagated**](https://msdn.microsoft.com/library/aa393650) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")
</dt> </dl>

Scoping system's name.

</dd> </dl>

## Remarks

WMI does not implement this class.

This documentation is derived from the CIM class descriptions published by the DMTF. Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server�2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



�

�



