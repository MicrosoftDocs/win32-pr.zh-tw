---
title: WeeklyTrigger. DaysOfWeek 屬性
description: 針對腳本，取得或設定工作執行的星期幾。
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek 屬性工作排程器
- DaysOfWeek 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、DaysOfWeek 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509476"
---
# <a name="weeklytriggerdaysofweek-property"></a>WeeklyTrigger. DaysOfWeek 屬性

針對腳本，取得或設定工作執行的星期幾。

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>屬性值

位元遮罩，表示工作在一周中的哪幾天執行。

## <a name="remarks"></a>備註

下表顯示這個屬性所使用之位元遮罩的對應。



| Month     | 十六進位值 | 十進位值 |
|-----------|-----------|---------------|
| 星期日    | 0X01      | 1             |
| 星期一    | 0x02      | 2             |
| Tuesday   | 0X04      | 4             |
| 星期三 | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| 星期五    | 0x20      | 32            |
| 星期六  | 0X40      | 64            |



 

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) 元素來指定一周中的天數。

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
</dt> </dl>

 

 





