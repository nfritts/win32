---
Description: 'The Managed Object Format (MOF) file that creates a namespace can also define the security descriptors for the namespace by including the NamespaceSecuritySDDL qualifier with the security descriptor in security descriptor definition language (SDDL) format.'
audience: developer
author: 'REDMOND\\markl'
manager: 'REDMOND\\markl'
ms.assetid: 'eeda3351-11ec-4064-90dd-f67ccf5c8cb6'
ms.prod: 'windows-server-dev'
ms.technology: 'windows-management-instrumentation'
ms.tgt_platform: multiple
title: Setting Namespace Security When the Namespace is Created
---

# Setting Namespace Security When the Namespace is Created

The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-security-descriptor-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](https://msdn.microsoft.com/library/windows/desktop/aa379567) format.

You can use **NamespaceSecuritySDDL** to secure any namespace. You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace. The SDDL string is processed by WMI to establish the namespace security but is not stored as a string. If no security descriptor is specified, the default security is used. For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).

The following procedure sets the security descriptor for the *root\\MyNamespace* namespace. The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](https://msdn.microsoft.com/library/windows/desktop/ms721573#-security-discretionary-access-control-list-gly) that is inherited by child namespaces. The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**. For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).

**To set a namespace DACL**

1.  Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.

    The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Be aware that the SDDL string is case-sensitive: the letters must be capitalized.

    The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.

    **c:\\mofcomp MyNamespace\_security.mof**

    In C++, use the [**IMoFCompiler**](imofcompiler.md) methods.

4.  If your attempt to set the namespace DACL fails, consider the following error messages:

    

    | Error                           | Description                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **WBEM\_E\_INVALID\_PARAMETER** | There is no inherited DACL. Alternately, the caller has violated the DACL or the SD in the parent namespace. |
    | **WBEM\_E\_ACCESS\_DENIED**     | The caller does not have permission to update the SDDL in MOF.                                               |

    

     

## Related topics

<dl> <dt>

[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Namespace Access Rights Constants**](namespace-access-rights-constants.md)
</dt> <dt>

[**Namespace ACE Flag Constants**](namespace-ace-flag-constants.md)
</dt> <dt>

[Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 


