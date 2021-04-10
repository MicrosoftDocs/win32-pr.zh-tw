---
description: 啟用網路介面卡。
ms.assetid: ceb71e1b-5107-420f-a677-814307340469
ms.tgt_platform: multiple
title: Enable Win32_NetworkAdapter 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a7653d0bcda28ca333bc5c70bdcd69bce382787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187684"
---
# <a name="enable-method-of-the-win32_networkadapter-class"></a>Enable Win32 \_ NetworkAdapter 類別的方法

**Enable** 方法可啟用網路介面卡。

## <a name="syntax"></a>語法


```mof
uint32 Enable();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。

## <a name="remarks"></a>備註

如果您的應用程式不是系統管理員存取權 privilidges，您可能會在使用此方法時遇到困難。

## <a name="examples"></a>範例

下列 Visual Basic 腳本範例會啟用第一個網路介面卡，並顯示 **NetEnabled** 屬性的狀態。 如需詳細資訊，請參閱 [**swbemobjectset 搭配使用. ItemIndex**](/windows/desktop/wmisdk/swbemobjectset-itemindex)。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colAdapters = _
    objWMIService.Execquery_
        ("Select * from Win32_NetworkAdapter Where NetEnabled=False")
For Each Adapter in colAdapters
    WScript.Echo Adapter.DeviceId & "    " & Adapter.Name
Next
errReturn = colAdapters.ItemIndex(0).Enable()
If errReturn <> 0 Then
    WScript.Echo "Enable Network adapter failed for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId
Else 
    WScript.Echo "Enable Network adapter succeeded for adapter= "_
        & colAdapters.ItemIndex(0).DeviceId 
End If 
WScript.Echo "NetEnabled= " & colAdapters.ItemIndex(0).NetEnabled
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ NetworkAdapter**](win32-networkadapter.md)
</dt> <dt>

[WMI 工作：網路功能](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[WMI 中的 IPv6 和 IPv4 支援](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

