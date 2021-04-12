---
description: SWbemPrivilegeSet 物件的 Item 方法會傳回集合中的 SWbemPrivilege 物件。 Item 方法是 SWbemPrivilegeSet 物件的預設方法。
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848615"
---
# <a name="swbemprivilegesetitem-method"></a>SWbemPrivilegeSet 專案方法

[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **Item** 方法會傳回集合中的 [**SWbemPrivilege**](swbemprivilege.md)物件。 **Item** 方法是 **SWbemPrivilegeSet** 物件的預設方法。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*iPrivilege* 
</dt> <dd>

必要。 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)群組中的其中一個 WMI 常數。 這些常數基本上是代表特定許可權的整數。 例如，若要取得可讓您關閉 Windows 系統的許可權，請使用 **wbemPrivilegeShutdown** 常數或等同于 23 (0x17) 的數位。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回要求的 [**SWbemPrivilege**](swbemprivilege.md) 物件。

## <a name="error-codes"></a>錯誤碼

當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

指定的許可權不存在。

</dd> </dl>

## <a name="examples"></a>範例

下列 VBScript 程式碼範例使用 **Item** 方法


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilege**](swbemprivilege.md)
</dt> </dl>

 

 




