---
title: TaskSettings. RunOnlyIfIdle 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器只有在電腦處於閒置狀態時，才會執行工作。
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- RunOnlyIfIdle 屬性工作排程器
- RunOnlyIfIdle 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RunOnlyIfIdle 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed423dc4cd34a03bd3b76401284a4d6bfb98270e7c0d0feed0a45046a82e7d3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990818"
---
# <a name="tasksettingsrunonlyifidle-property"></a>TaskSettings. RunOnlyIfIdle 屬性

針對腳本，取得或設定布林值，指出工作排程器只有在電腦處於閒置狀態時，才會執行工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則屬性會指出工作排程器只有在電腦處於閒置狀態時，才會執行工作。 預設值是 False。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





