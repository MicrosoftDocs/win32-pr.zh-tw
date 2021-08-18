---
title: DailyTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |DailyTrigger. RandomDelay 屬性
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，DailyTrigger 物件
- DailyTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc3bfec997b50a1f9d802191387a2186576532ca027e1086fc311b31f0da5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139471"
---
# <a name="dailytriggerrandomdelay-property"></a>DailyTrigger. RandomDelay 屬性

針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>屬性值

隨機新增至觸發程式開始時間的延遲時間。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





