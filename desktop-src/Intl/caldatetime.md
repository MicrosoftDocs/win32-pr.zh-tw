---
description: 已取代。 代表時間的瞬間，通常表示為一天的日期和時間，以及對應的行事曆。
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992520"
---
# <a name="caldatetime-structure"></a>CALDATETIME 結構

已取代。 代表時間的瞬間，通常表示為一天的日期和時間，以及對應的行事曆。

## <a name="syntax"></a>語法


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>成員

<dl> <dt>

**CalId**
</dt> <dd>

瞬間時間的行事 [曆識別碼](calendar-identifiers.md) 。

</dd> <dt>

**時代**
</dt> <dd>

瞬間的時代資訊。

</dd> <dt>

**年**
</dt> <dd>

瞬間的時間。

</dd> <dt>

**月**
</dt> <dd>

瞬間的時間。

</dd> <dt>

**Day**
</dt> <dd>

瞬間的當日時間。

</dd> <dt>

**DayOfWeek**
</dt> <dd>

一周中的某一天的當日時間。

</dd> <dt>

**小時**
</dt> <dd>

瞬間的時數。

</dd> <dt>

**分鐘**
</dt> <dd>

瞬間時間的分鐘數。

</dd> <dt>

**第二**
</dt> <dd>

時間瞬間的第二個。

</dd> <dt>

**蜱**
</dt> <dd>

瞬間的時間刻度。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援結構](national-language-support-structures.md)
</dt> </dl>

 

 




