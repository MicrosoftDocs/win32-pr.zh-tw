---
title: RepetitionPattern. Interval 屬性
description: 針對腳本，取得或設定每次重新開機工作之間的時間量。
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Interval 屬性工作排程器
- Interval 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器，Interval 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6efcaa56d2c251b5e044c87091bc646c21f8691aa384ad522b6062014fd496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072618"
---
# <a name="repetitionpatterninterval-property"></a>RepetitionPattern. Interval 屬性

針對腳本，取得或設定每次重新開機工作之間的時間量。

## <a name="syntax"></a>Syntax


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>屬性值

每次重新開機工作之間的時間量。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。 允許的時間上限為31天，而允許的最短時間為1分鐘。

## <a name="remarks"></a>備註

如果您指定工作的重複持續時間，您也必須指定重複間隔。

讀取或寫入工作的 XML 時，會在工作排程器架構的 [**interval**](taskschedulerschema-interval-repetitiontype-element.md) 元素中指定重複間隔。

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

 

 





