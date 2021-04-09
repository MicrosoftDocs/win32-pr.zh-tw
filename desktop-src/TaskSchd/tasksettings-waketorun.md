---
title: TaskSettings. WakeToRun 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器會在執行工作時喚醒電腦。
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- WakeToRun 屬性工作排程器
- WakeToRun 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、WakeToRun 屬性
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685733"
---
# <a name="tasksettingswaketorun-property"></a>TaskSettings. WakeToRun 屬性

針對腳本，取得或設定布林值，指出工作排程器會在執行工作時喚醒電腦。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則屬性會指出工作排程器會在執行工作時喚醒電腦。

## <a name="remarks"></a>備註

當工作排程器服務喚醒電腦以執行工作時，即使電腦不再處於睡眠或睡眠模式，畫面仍會保持關閉狀態。 當 Windows Vista 偵測到使用者已回到使用電腦時，畫面會開啟。

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) 元素中指定。

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

 

 





