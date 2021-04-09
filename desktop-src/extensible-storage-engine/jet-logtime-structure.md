---
description: 深入瞭解： JET_LOGTIME 結構
title: JET_LOGTIME 結構
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696895"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_logtime-structure"></a>JET_LOGTIME 結構

**JET_LOGTIME** 結構會保存事件日期和時間的元素。

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>成員

**bSeconds**

事件的時間（以秒為單位）。 這個值可以是0到59。 當結構為 null 時，就會使用0。

**bMinutes**

事件的時間（以分鐘為單位）。 這個值可以是0到59。 當結構為 null 時，就會使用0。

**bHours**

事件的時間（以小時為單位）。 這個值可以是0到23。 當結構為 null 時，就會使用0。

**bDay**

事件月份的日期。 這個值可以是0到31。 當結構為 null 時，就會使用0。

**bMonth**

活動年度的月份。 這個值可以是0到12。 當結構為 null 時，就會使用0。

**bYear**

事件的年份 (以 1900) 位移。 若要達到實際年份，請將1900新增至此值。 當結構為 null 時，就會使用0。

**bFiller1**

應忽略此欄位。

**fTimeIsUTC**

時間是採用 UTC 格式。

**fUnused**

應忽略此欄位。

**bFiller2**

應忽略此欄位。

### <a name="remarks"></a>備註

此結構主要是用於偵錯工具中的使用方式。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
