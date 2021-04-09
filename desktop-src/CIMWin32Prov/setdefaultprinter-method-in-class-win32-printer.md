---
description: SetDefaultPrinter WMI 類別方法會為呼叫方法的使用者設定預設系統印表機。
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Win32_Printer 類別的 SetDefaultPrinter 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847601"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a>Win32 Printer 類別的 SetDefaultPrinter 方法 \_

**SetDefaultPrinter** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會為呼叫方法的使用者設定預設系統印表機。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，則傳回 0 (零) ，如果發生錯誤，則傳回其他值。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

## <a name="examples"></a>範例

[安裝 Tcp/ip 印表機埠和印表機](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7)VBScript 範例會安裝 tcp/ip 印表機埠、安裝印表機，然後將印表機設定為預設值。

下列 VBScript 程式碼範例會設定電腦上的預設印表機。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> <dt>

[WMI 工作：印表機和列印](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[**Win32 \_ 印表機**](win32-printer.md)
</dt> </dl>

 

