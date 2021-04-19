---
description: 您可以使用 SWbemPrivilegeSet 物件的 AddAsString 方法，將許可權新增至使用許可權字串的 SWbemPrivilegeSet 集合。
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet. AddAsString 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984737"
---
# <a name="swbemprivilegesetaddasstring-method"></a>SWbemPrivilegeSet. AddAsString 方法

您可以使用 [**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **AddAsString** 方法，將許可權新增至使用許可權字串的 **SWbemPrivilegeSet** 集合。 您可以使用這個方法來新增許可權，或啟用 [**SWbemSecurity**](swbemsecurity.md) 物件的許可權。 請參閱 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strPrivilege* 
</dt> <dd>

必要。 其中一個許可權字串。 如需這些字串和相關 WMI 常數的完整清單，請參閱 [**許可權常數**](privilege-constants.md)。 每個許可權字串都代表特定的許可權。 例如，若要新增用來關閉電腦系統的許可權，請使用 **SeShutdownPrivilege** 字串。

</dd> <dt>

*bIsEnabled* \[選\]
</dt> <dd>

啟用或停用此許可權的布林值。 預設值是 **True**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回代表新許可權的 [**SWbemPrivilege**](swbemprivilege.md) 物件。 否則，會傳回 null 物件。

## <a name="error-codes"></a>錯誤碼

**AddAsString** 方法完成後， **Err** 物件可能會包含下列清單中的錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> </dl>

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會使用 [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport)來建立列印伺服器的新埠。 這項作業需要 **SeLoadDriverPrivilege** 。 請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



使用這個方法的程式碼範例也會在 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 主題中說明。

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

[**SWbemPrivilegeSet 新增**](swbemprivilegeset-add.md)
</dt> <dt>

[**SWbemPrivilegeSet。移除**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**許可權常數**](privilege-constants.md)
</dt> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

