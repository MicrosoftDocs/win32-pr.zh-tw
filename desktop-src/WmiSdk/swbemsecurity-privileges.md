---
description: 許可權屬性是 SWbemPrivilegeSet 物件。 這個屬性是用來啟用或停用特定的 Windows 許可權。 您可能需要使用 Windows Management Instrumentation (WMI) API 來設定這些許可權的其中之一，以執行特定工作。
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: SWbemSecurity) 的許可權屬性 (>wbemdisp.tlb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192053"
---
# <a name="swbemsecurityprivileges-property"></a>SWbemSecurity 許可權屬性

**許可權** 屬性是 [**SWbemPrivilegeSet**](swbemprivilegeset.md)物件。 這個屬性是用來啟用或停用特定的 Windows 許可權。 您可能需要使用 Windows Management Instrumentation (WMI) API 來設定這些許可權的其中之一，以執行特定工作。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這項設定可讓您授與或撤銷許可權，作為 WMI 標記字串的一部分。 如需適用值的完整清單，請參閱 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) 和 [**許可權常數**](privilege-constants.md)。

您可以藉由將 [**wbemscripting.swbemlocator**](swbemprivilege.md)物件新增至 [**許可權**] 屬性，來變更為 [**SWbemServices**](swbemservices.md)、 [**SWbemObject**](swbemobject.md)、 [**swbemobjectset 搭配使用**](swbemobjectset.md)、 [**SWbemObjectPath**](swbemobjectpath.md)和 [**SWbemPrivilege**](swbemlocator.md)物件定義的許可權。

不同版本的 Windows 如何處理許可權的變更有一些基本差異。 如果您開發的應用程式只用于 Windows 平臺，您可以隨時設定或撤銷許可權。

下列範例會在初始的標記連接上設定 **SeDebugPrivilege** ，以取得 [**SWbemServices**](swbemservices.md) 物件。


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



如需有關如何針對標記連接格式化安全性字串的詳細資訊，請參閱 [**許可權常數**](privilege-constants.md)。

下列範例會執行相同的工作，但它會在初始登入 WMI 之後設定許可權。


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



請注意，若要呼叫 [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md)，您必須使用安全性許可權的完整名稱，例如 "SeDebugPrivilege" 而不是 "Debug"。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




