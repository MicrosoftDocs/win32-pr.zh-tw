---
title: MonthlyDOWTrigger. WeeksOfMonth 屬性
description: 針對腳本，取得或設定工作執行的月份周數。
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- WeeksOfMonth 屬性工作排程器
- WeeksOfMonth 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、WeeksOfMonth 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323ee8b93411d7ef176fa9dc2ffb3a4acfd1f902c0dc481fe48e07b82821227b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517438"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>MonthlyDOWTrigger. WeeksOfMonth 屬性

針對腳本，取得或設定工作執行的月份周數。

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>屬性值

位元遮罩，表示工作在一周中的哪幾天執行。

## <a name="remarks"></a>備註

下表顯示這個屬性所使用之位元遮罩的對應。



| 週                     | 十六進位值 | 十進位值 |
|--------------------------|-----------|---------------|
| 每月第一周  | 0X01      | 1             |
| 當月的第二周 | 0x02      | 2             |
| 當月的第三周  | 0X04      | 4             |
| 每月第四周 | 0X08      | 8             |



 

讀取或寫入工作的 XML 時，每週的每月星期幾日曆中的天數是由 [**week 元素所**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) 指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





