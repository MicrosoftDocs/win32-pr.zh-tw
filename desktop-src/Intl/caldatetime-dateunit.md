---
description: 已取代。 指定用於調整 CALDATETIME 結構的日期單位。
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: CALDATETIME_DATEUNIT 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: f73aeebe738a631bff95a07beaa0b5928d3d1935ac7b400ed5fa333e79c1f044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118391598"
---
# <a name="caldatetime_dateunit-enumeration"></a>CALDATETIME \_ DATEUNIT 列舉

已取代。 指定用於調整 [**CALDATETIME**](caldatetime.md) 結構的日期單位。

## <a name="syntax"></a>Syntax


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**
</dt> <dd>

紀元日期時間單位。

</dd> <dt>

<span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**
</dt> <dd>

年份日期時間單位。

</dd> <dt>

<span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**
</dt> <dd>

月份日期時間單位。

</dd> <dt>

<span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**
</dt> <dd>

周日期時間單位。

</dd> <dt>

<span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**
</dt> <dd>

日期日期時間單位。

</dd> <dt>

<span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**
</dt> <dd>

小時的日期時間單位。

</dd> <dt>

<span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**
</dt> <dd>

分鐘的日期時間單位。

</dd> <dt>

<span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**
</dt> <dd>

第二個日期時間單位。

</dd> <dt>

<span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**
</dt> <dd>

刻度日期時間單位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援列舉類型](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




