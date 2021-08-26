---
title: TaskSettings. StopIfGoingOnBatteries 屬性
description: 針對腳本，取得或設定布林值，這個值表示如果電腦正進入電池，工作將會停止。
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- StopIfGoingOnBatteries 屬性工作排程器
- StopIfGoingOnBatteries 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、StopIfGoingOnBatteries 屬性
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229d5d3beef974e9ce8758f9bd81fc3217bd9c3fcf9bf37be137abe6515cc62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974884"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>TaskSettings. StopIfGoingOnBatteries 屬性

針對腳本，取得或設定布林值，這個值表示如果電腦正進入電池，工作將會停止。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>屬性值

此為布林值，指出如果電腦即將進入電池，將會停止該工作。 若為 True，則屬性會指出如果電腦即將進入電池，將會停止該工作。 如果為 False，屬性工作表示如果電腦正在進入電池，將不會停止該工作。 預設值為 True。 如需詳細資訊，請參閱備註。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) 元素中指定。

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

 

 





