---
title: MonthlyTrigger. DaysOfMonth 屬性
description: 針對腳本，取得或設定工作執行的月份天數。
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- DaysOfMonth 屬性工作排程器
- DaysOfMonth 屬性工作排程器，MonthlyTrigger 物件
- MonthlyTrigger 物件工作排程器、DaysOfMonth 屬性
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104358"
---
# <a name="monthlytriggerdaysofmonth-property"></a>MonthlyTrigger. DaysOfMonth 屬性

針對腳本，取得或設定工作執行的月份天數。

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a>屬性值

位元遮罩，表示工作執行的當月天數。

## <a name="remarks"></a>備註



| 月中的日 | 十六進位值  | 十進位值 |
|--------------|------------|---------------|
| 1            | 0x01       | 1             |
| 2            | 0x02       | 2             |
| 3            | 0x04       | 4             |
| 4            | 0x08       | 8             |
| 5            | 0x10       | 16            |
| 6            | 0x20       | 32            |
| 7            | 0x40       | 64            |
| 8            | 0x80       | 128           |
| 9            | 0x100      | 256           |
| 10           | 0x200      | 512           |
| 11           | 0x400      | 1024          |
| 12           | 0x800      | 2048          |
| 13           | 0x1000     | 4096          |
| 14           | 0x2000     | 8192          |
| 15           | 0x4000     | 16384         |
| 16           | 0x8000     | 32768         |
| 17           | 0x10000    | 65536         |
| 18           | 0x20000    | 131072        |
| 19           | 0x40000    | 262144        |
| 20           | 0x80000    | 524288        |
| 21           | 0x100000   | 1048576       |
| 22           | 0x200000   | 2097152       |
| 23           | 0x400000   | 4194304       |
| 24           | 0x800000   | 8388608       |
| 25           | 0x1000000  | 16777216      |
| 26           | 0x2000000  | 33554432      |
| 27           | 0x4000000  | 67108864      |
| 28           | 0x8000000  | 134217728     |
| 29           | 0x10000000 | 268435456     |
| 30           | 0x20000000 | 536870912     |
| 31           | 0x40000000 | 1073741824    |
| 最後一個         | 0x80000000 | 2147483648    |



 

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) 元素來指定月份的日期。

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
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





