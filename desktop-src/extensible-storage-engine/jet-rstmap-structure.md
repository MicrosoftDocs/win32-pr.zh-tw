---
description: 深入瞭解： JET_RSTMAP 結構
title: JET_RSTMAP 結構
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: e1f3813be8e1ea076a401ce5cdabef3e454b98c1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983581"
---
# <a name="jet_rstmap-structure"></a>JET_RSTMAP 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_rstmap-structure"></a>JET_RSTMAP 結構

當 [JetInit](./jetinit-function.md)和 [JetExternalRestore](./jetexternalrestore-function.md)函式使用時， **JET_RSTMAP** 結構可重新對應儲存在交易記錄檔中的資料庫檔案路徑。 這可讓您在離線或從備份還原時，移動資料庫。

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>成員

**szDatabaseName**

在復原期間，與交易記錄檔相關聯之資料庫的目前絕對路徑。

**szNewDatabaseName**

資料庫的新絕對路徑。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JET_RSTMAP_W</strong> (Unicode) 和 <strong>JET_RSTMAP_A</strong> (ANSI) 。</p> | 



### <a name="see-also"></a>另請參閱

[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
