---
title: TaskSettings. AllowHardTerminate 屬性
description: 針對腳本，取得或設定布林值，這個值表示工作可能會由使用 TerminateProcess 的工作排程器服務終止。
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- AllowHardTerminate 屬性工作排程器
- AllowHardTerminate 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、AllowHardTerminate 屬性
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686136"
---
# <a name="tasksettingsallowhardterminate-property"></a>TaskSettings. AllowHardTerminate 屬性

針對腳本，取得或設定布林值，這個值表示工作可能會由使用 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)的工作排程器服務終止。 服務會藉由傳送 [**WM \_ 關閉**](../winmsg/wm-close.md) 通知來嘗試關閉執行中的工作，如果工作沒有回應，則只有在這個屬性設定為 true 時，才會終止工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則可使用 [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)來終止工作。 如果為 False，則無法使用 **TerminateProcess** 來終止工作。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

