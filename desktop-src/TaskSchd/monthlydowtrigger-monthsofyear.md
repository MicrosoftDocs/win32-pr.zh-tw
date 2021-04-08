---
title: MonthlyDOWTrigger. MonthsOfYear 屬性
description: 針對腳本，取得或設定工作在一年中執行的月份。 |MonthlyDOWTrigger. MonthsOfYear 屬性
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- MonthsOfYear 屬性工作排程器
- MonthsOfYear 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、MonthsOfYear 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853863"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>MonthlyDOWTrigger. MonthsOfYear 屬性

針對腳本，取得或設定工作在一年中執行的月份。

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>屬性值

位元遮罩，表示工作執行的年中月份。

## <a name="remarks"></a>備註

下表顯示這個屬性所使用之位元遮罩的對應。



| Month     | 十六進位值 | 十進位值 |
|-----------|-----------|---------------|
| 一月   | 0X01      | 1             |
| 二月  | 0x02      | 2             |
| 3 月     | 0X04      | 4             |
| 四月     | 0X08      | 8             |
| 五月       | 0X10      | 16            |
| 6 月      | 0X20      | 32            |
| 7 月      | 0x40      | 64            |
| 8 月    | 0X80      | 128           |
| 9 月 | 0X100     | 256           |
| 10 月   | 0X200     | 512           |
| 11 月  | 0X400     | 1024          |
| 12 月  | 0X800     | 2048          |



 

在讀取或寫入工作的 XML 時，每月的每月星期幾日曆中的月份是由工作排程器架構的 [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) 元素所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





