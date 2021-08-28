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
ms.openlocfilehash: 0b54ba5bb6b4f5ed3f08b5d4cc950f77d199c525
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988241"
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


| <p>Name</p> | <p>值</p> | 
|-------------|--------------|
| <p>串流備份</p> | <p>0 (零)</p> | 
| <p>快照集備份</p> | <p>1</p> | 



**fReserved**

應忽略此欄位。

### <a name="remarks"></a>備註

此結構會在進行偵錯工具時使用。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
