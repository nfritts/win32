---
title: JET_LS.Equals method (JET_LS)
TOCTitle: Equals method (JET_LS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39510488
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name: 
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type: 
- apiref
- kbSyntax
api_type: 
- Managed
api_location: 
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW

---

# JET_LS.Equals method (JET_LS)

Returns a value indicating whether this instance is equal to another instance.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## Syntax

``` vb
'Declaration
Public Function Equals ( _
    other As JET_LS _
) As Boolean
'Usage
Dim instance As JET_LS
Dim other As JET_LS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_LS other
)
```

#### Parameters

  - other  
    Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)  
    
    An instance to compare with this instance.

#### Return value

Type: [System.Boolean](/dotnet/api/system.boolean)  
True if the two instances are equal.  

#### Implements

[IEquatable\<T\>.Equals(T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## See also

#### Reference

[JET_LS structure](./jet-ls-structure.md)

[JET_LS members](./jet-ls-members.md)

[Equals overload](./jet-ls.equals-method.md)

[Microsoft.Isam.Esent.Interop namespace](./microsoft.isam.esent.interop-namespace.md)