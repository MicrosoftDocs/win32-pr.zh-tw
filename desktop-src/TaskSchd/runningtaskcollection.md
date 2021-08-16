---
title: RunningTaskCollection 物件
description: 腳本物件，提供用來控制執行中工作的集合。
ms.assetid: b137fcf3-634c-4ac6-908d-357f54da3025
keywords:
- RunningTaskCollection 物件工作排程器
- RunningTaskCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RunningTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81651e62be3b787678ee77f2b997c24e99016041567b23da0c534d94633dfdcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059966"
---
# <a name="runningtaskcollection-object"></a>RunningTaskCollection 物件

腳本物件，提供用來控制執行中工作的集合。

## <a name="members"></a>成員

**RunningTaskCollection** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**RunningTaskCollection** 物件具有這些屬性。



| 屬性                                                | 描述                                                    |
|:--------------------------------------------------------|:---------------------------------------------------------------|
| [**計數**](runningtaskcollection-count.md)<br/> | 取得集合中執行中的工作數目。<br/> |
| [**項目**](runningtaskcollection-item.md)<br/>   | 從集合中取得指定的工作。 <br/>       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTask**](runningtask.md)
</dt> <dt>

[**TaskService. GetRunningTasks**](taskservice-getrunningtasks.md)
</dt> <dt>

[**RegisteredTask.GetInstances**](registeredtask-getinstances.md)
</dt> </dl>

 

 





