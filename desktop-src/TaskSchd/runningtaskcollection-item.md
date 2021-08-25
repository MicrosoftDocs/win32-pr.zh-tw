---
title: RunningTaskCollection 專案屬性
description: 針對腳本，從集合取得指定的工作。
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，RunningTaskCollection 物件
- RunningTaskCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7e2ca7abf5f1daa936509d5fae71211e8b139537fa1782daac6c08bf9a1017f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866778"
---
# <a name="runningtaskcollectionitem-property"></a>RunningTaskCollection 專案屬性

針對腳本，從集合取得指定的工作。

## <a name="syntax"></a>Syntax


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>屬性值

[**RunningTask**](runningtask.md)物件，其中包含要求的內容。

## <a name="remarks"></a>備註

集合以1為基礎。 換句話說，集合中第一個專案的索引為1。

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

 

 





