---
description: 使用各種新功能來擴充 IShellDispatch 物件。
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: 'IShellDispatch2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 481e64c00ced458be05255af451206a42d449c42d157794dfd1077cf2dda278a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721088"
---
# <a name="ishelldispatch2-object"></a>IShellDispatch2 物件

使用各種新功能來擴充 [**IShellDispatch**](ishelldispatch.md) 物件。

> [!Note]  
> **IShellDispatch2** 是透過 [**Shell**](shell.md) 物件來執行和存取。

 

## <a name="members"></a>成員

**IShellDispatch2** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IShellDispatch2** 物件有這些方法。



| 方法                                                               | 描述                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | 判斷目前的使用者是否可以啟動和停止命名服務。<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | 顯示 [ **尋找印表機** ] 對話方塊。<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | 捕獲系統資訊。<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | 從登錄抓取群組的限制設定。<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | 傳回值，這個值表示特定服務是否正在執行。<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | 啟動命名服務。<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | 停止已命名的服務。<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | 在指定的檔案上執行指定的作業。<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | 顯示瀏覽器列。<br/>                                                 |



 

## <a name="remarks"></a>備註

如需 Windows 服務的討論，請參閱[服務](../services/services.md)檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell 物件**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
