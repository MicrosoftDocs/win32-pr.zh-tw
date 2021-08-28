---
description: 深入瞭解： JET_LGPOS 結構
title: JET_LGPOS 結構
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986151"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_lgpos-structure"></a>JET_LGPOS 結構

**JET_LGPOS** 結構會保存資料庫引擎記錄機制內部的資料。 此結構會被視為內部。

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>成員

**Ib**

支援 ESE 基礎結構，無法從您的程式碼中使用。

**isec**

支援 ESE 基礎結構，無法從您的程式碼中使用。

**lGeneration**

支援 ESE 基礎結構，無法從您的程式碼中使用。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
