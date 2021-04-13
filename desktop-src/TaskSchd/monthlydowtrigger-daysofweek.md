---
title: MonthlyDOWTrigger. DaysOfWeek 屬性
description: 針對腳本，取得或設定工作在一周中的哪幾天執行。
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek 屬性工作排程器
- DaysOfWeek 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、DaysOfWeek 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466441"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger. DaysOfWeek 屬性

針對腳本，取得或設定工作在一周中的哪幾天執行。

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>屬性值

位元遮罩，表示工作在一周中的哪幾天執行。

## <a name="remarks"></a>備註

下表顯示這個屬性所使用之位元遮罩的對應。



| 週中的日 | 十六進位值 | 十進位值 |
|-------------|-----------|---------------|
| 星期日      | 0x01      | 1             |
| 星期一      | 0x02      | 2             |
| Tuesday     | 0x04      | 4             |
| 星期三   | 0x08      | 8             |
| Thursday    | 0x10      | 16            |
| 星期五      | 0x20      | 32            |
| 星期六    | 0x40      | 64            |



 

在讀取或寫入工作的 XML 時， [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) 專案會指定每週每月星期幾行事曆的第幾天。

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

 

 





