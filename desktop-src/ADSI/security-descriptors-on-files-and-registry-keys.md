---
title: 檔案和登錄機碼上的安全描述項
description: Active Directory 服務介面 (ADSI) 可以用來管理及保護組織內的檔案系統，包括在使用者建立的檔案或檔案共用上設定或修改 Acl 的能力。
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- 檔案和登錄機碼 ADSI 的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333218"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>檔案和登錄機碼上的安全描述項

Active Directory 服務介面 (ADSI) 可以用來管理及保護組織內的檔案系統，包括在使用者建立的檔案或檔案共用上設定或修改 Acl 的能力。 安全性介面（例如 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)、 [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)和 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) ）會在 Active Directory、Exchange、檔案、檔案共用或登錄機碼物件上設定 acl。 在使用這些介面之前，如果安全描述項使用介面中的不同格式，或您沒有安全描述項的 SACL 存取權限，則可能需要修改安全描述項，因為您不是安全性系統管理員群組的成員。

若要取得、設定或修改安全描述項，請使用 [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) 介面。 這個介面可讓您從各種資源（例如 ADSI 格式 [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)、原始安全描述項或十六進位字串）中取出安全描述項，Exchange 5.5 中使用。 在抓取之後，您可以將它轉換成另一種格式，例如從原始安全描述項轉換為 **IADsSecurityDescriptor**。 然後，您可以將新的格式寫回資源。

某些 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) 屬性值（例如 [**AccessMask**](iadsaccesscontrolentry-property-methods.md) 和 **AceFlags**）會因不同的物件類型而有所不同。 例如，Active Directory 物件會針對 **IADsAccessControlEntry. AccessMask** 屬性使用 ads [**\_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum)列舉的 **ads \_ RIGHT \_ 一般 \_ 讀取** 成員，但檔案物件的對等存取權限則是檔案 **\_ 一般 \_ 讀取**。 假設 Active Directory 物件和非 Active Directory 物件的所有屬性值都相同，並不安全。 下列清單顯示非 Active Directory 物件的不同 **IADsAccessControlEntry** 屬性，以及可取得適當值的位置。

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

如需詳細資訊以及檔案或檔案共用物件的可能值清單，請參閱檔案 [安全性和存取權限](/windows/desktop/FileIO/file-security-and-access-rights)。

如需登錄物件的可能值清單以及登錄物件的可能值清單，請參閱登錄機 [碼安全性和存取權限](/windows/desktop/SysInfo/registry-key-security-and-access-rights)。

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

如需詳細資訊，請參閱 [**ACE \_ 標頭**](/windows/desktop/api/winnt/ns-winnt-ace_header)結構的 **AceType** 成員。

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

如需詳細資訊，請參閱 [**ACE \_ 標頭**](/windows/desktop/api/winnt/ns-winnt-ace_header)結構的 **AceFlags** 成員。

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**標誌**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

包含來自 WinNT 的下列一或多個值的零或組合。

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_\_ \_ 存在** (1) 的物件類型
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) 包含有效的值。

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_繼承的 \_ 物件 \_ 類型 \_ 存在** (2) 
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) 包含有效的值。

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

如需詳細資訊，請參閱 [**\_ 拒絕存取 \_ 物件 \_ ace**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)的 **ObjectType** 成員、[**存取 \_ 允許的 \_ 物件 \_ ace**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)和類似的結構。 不應針對非 Active Directory 物件設定或修改此屬性。

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

如需詳細資訊，請參閱 [**\_ 拒絕存取 \_ 物件 \_ ace**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)的 **InheritedObjectType** 成員、[**存取 \_ 允許的 \_ 物件 \_ ace**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)和類似的結構。 不應針對非 Active Directory 物件設定或修改此屬性。

</dd> </dl>

一般來說， [**IADsSecurityUtility**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) 會取出安全描述項的所有部分，例如擁有者、群組、SACL 或 DACL。 同樣地， [**IADsSecurityUtility**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) 預設會覆寫安全描述項的所有部分。 您可以使用 [**IADsSecurityUtility SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) 屬性來指定要抓取或設定之安全描述項的個別部分。 例如，您可以在呼叫 **GetSecurityDescriptor** 之前將 **SecurityMask** 設定為 [**ADS \_ security \_ INFO \_ dacl**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) ，以只抓取 DACL 而不需要取得安全描述項的其他部分。

如需詳細資訊和使用 [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) 介面將 ace 新增至檔案的程式碼範例，請參閱 [將 ace 新增至](example-code-for-adding-an-ace-to-a-file.md)檔案的範例程式碼。

下列範例程式碼會為 [**AccessMask**](iadsaccesscontrolentry-property-methods.md)、 **AceType**、 **AceFlags** 和 **Flags** 屬性提供檔案、檔案共用和登錄物件的常數識別碼，以搭配 Visual Basic 和 Microsoft Visual Basic 腳本編寫版本使用。


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 