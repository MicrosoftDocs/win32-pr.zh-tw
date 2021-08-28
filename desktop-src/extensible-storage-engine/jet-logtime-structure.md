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
ms.openlocfilehash: 4cb99f2a64877ec76afda993a76be4aeaa14c895
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987032"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME 結構


_**適用于：** Windows |Windows伺服器_

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


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
