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
ms.openlocfilehash: 477c84ee0b466fb43ee0bb06ef14a2a1be6dd00e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472184"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO 結構


_**適用于：** Windows |Windows伺服器_

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

**Windows vista： bklogtimeMark** 是 Windows vista 引進。

**genLow**

與此備份事件相關聯的低記錄產生編號。

**genHigh**

與此備份事件相關聯的高記錄產生編號。

### <a name="remarks"></a>備註

此結構是在 [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) 結構內用來表示有關資料庫備份事件的資料。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
