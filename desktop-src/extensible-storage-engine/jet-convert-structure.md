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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848324"
---
# <a name="jet_convert-structure"></a>JET_CONVERT 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_convert-structure"></a>JET_CONVERT 結構

**JET_CONVERT** 結構包含舊版 ESE 版本 DLL 的名稱，此 DLL 是用來讀取使用舊版所建立的資料庫。 此外，還提供其他旗標來控制轉換的本質。

**Windows Server 2003：**[JetCompact](./jetcompact-function.md)中執行轉換的功能已從 Windows Server 2003 中的產品中移除。 只有在 Windows 2000 和 Windows XP 中才支援此功能。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_CONVERT_W</strong> (Unicode) 和 <strong>JET_CONVERT_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetCompact](./jetcompact-function.md)
