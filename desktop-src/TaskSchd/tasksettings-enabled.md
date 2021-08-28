---
title: TaskSettings 已啟用屬性
description: 針對腳本，取得或設定布林值，表示已啟用工作。 只有當這項設定為 True 時，才能執行此工作。
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Enabled 屬性工作排程器
- Enabled 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，Enabled 屬性
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7853177aecae963e4899a67d2ba5b39d1eaebdc75e25ce6e14523963a70c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738159"
---
# <a name="tasksettingsenabled-property"></a>TaskSettings 已啟用屬性

針對腳本，取得或設定布林值，表示已啟用工作。 只有當這項設定為 True 時，才能執行此工作。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>屬性值

若為 True，則會啟用工作。 如果為 False，則不會啟用工作。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會指定在工作排程器架構的 [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) 元素中。

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

 

 





