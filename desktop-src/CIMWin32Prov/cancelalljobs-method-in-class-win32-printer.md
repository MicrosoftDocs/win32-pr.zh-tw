---
description: 移除所有工作，包括目前從佇列中列印的工作。
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Win32_Printer 類別的 CancelAllJobs 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06aae96cec4e38c7ff9c213cd19dc35e9843a077c262aafcaf0aed43160505a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085838"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a>Win32 Printer 類別的 CancelAllJobs 方法 \_

**CancelAllJobs** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會移除所有的工作，包括目前從佇列中列印的工作。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

Success

</dd> <dt>

**5**
</dt> <dd>

拒絕存取

</dd> </dl>

## <a name="examples"></a>範例

[ [當列印佇列清除時通知使用者] 會](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) 使用 Msg.exe 將網路警示傳送給任何在列印佇列中有檔要清除的使用者。 傳送警示之後，腳本會清除列印佇列。

[ [刪除所有列印工作](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) ] VBScript 程式碼範例會刪除本機電腦上的所有列印工作。

下列 VBScript 範例會刪除名為 HP QuietJet 之印表機的所有列印工作。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
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

[**Win32 \_ 印表機**](win32-printer.md)
</dt> </dl>

 

