---
description: 深入瞭解： JET_BKINFO 結構
title: JET_BKINFO 結構
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194614"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO 結構

**JET_BKINFO** 結構會保存有關特定備份事件的資料集合。

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>成員

**lgposMark**

此備份的識別碼。

**logtimeMark**

此備份事件的時間。

**bklogtimeMark**

此備份事件的時間，以及表示快照集備份的其他位。

**Windows vista： bklogtimeMark** 是在 windows vista 中引進的。

**genLow**

與此備份事件相關聯的低記錄產生編號。

**genHigh**

與此備份事件相關聯的高記錄產生編號。

### <a name="remarks"></a>備註

此結構是在 [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) 結構內用來表示有關資料庫備份事件的資料。

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
