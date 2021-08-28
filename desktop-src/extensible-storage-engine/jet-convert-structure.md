---
description: 深入瞭解： JET_CONVERT 結構
title: JET_CONVERT 結構
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: ce3fbcc7de9c7904689de3df923a87d575b1b92b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986781"
---
# <a name="jet_convert-structure"></a>JET_CONVERT 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_convert-structure"></a>JET_CONVERT 結構

**JET_CONVERT** 結構包含舊版 ESE 版本 DLL 的名稱，此 DLL 是用來讀取使用舊版所建立的資料庫。 此外，還提供其他旗標來控制轉換的本質。

**Windows Server 2003：**[JetCompact](./jetcompact-function.md)中執行轉換的功能已從產品的 Windows Server 2003 中移除。 只有 Windows 2000 和 Windows XP 才支援此功能。

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>成員

**SzOldDll**

較早版本的 ESE DLL 名稱，包括路徑資訊。

**fFlags**

保留供系統使用。

**fSchemaChangesOnly**

保留供系統使用。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JET_CONVERT_W</strong> (Unicode) 和 <strong>JET_CONVERT_A</strong> (ANSI) 。</p> | 



### <a name="see-also"></a>另請參閱

[JetCompact](./jetcompact-function.md)
