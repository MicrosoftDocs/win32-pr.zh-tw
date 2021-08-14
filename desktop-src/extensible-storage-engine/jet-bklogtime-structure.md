---
description: 深入瞭解： JET_BKLOGTIME 結構
title: JET_BKLOGTIME 結構
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487720"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME 結構

**JET_BKLOGTIME** 結構會保存事件的日期和時間元素。 它是 [JET_LOGTIME](./jet-logtime-structure.md)的延伸。

**Windows vista： JET_BKLOGTIME** 是在 Windows vista 中引進。

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>成員

**bSeconds**

事件的時間（以秒為單位）。 這可以是 0 (零) 至60。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bMinutes**

事件的時間（以分鐘為單位）。 這可以是 0 (零) 至60。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bHours**

事件的時間（以小時為單位）。 這可以是 0 (零) 到24。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bDay**

事件月份的日期。 這可以是 0 (零) 到31。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bMonth**

活動年度的月份。 這可以是 0 (零) 到12。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bYear**

年份 (事件的 1900) 位移。 若要達到實際年份，請將1900新增至此值。 當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。

**bFiller1**

應忽略此欄位。

**fTimeIsUTC**

時間是採用 UTC 格式。

**fUnused**

應忽略此欄位。

**bFiller2**

應忽略此欄位。

**fOSSnapshot**

如果此事件是備份，此旗標會包含下列其中一個可能的值：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>值</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>串流備份</p></td>
<td><p>0 (零)</p></td>
</tr>
<tr class="even">
<td><p>快照集備份</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

應忽略此欄位。

### <a name="remarks"></a>備註

此結構會在進行偵錯工具時使用。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
