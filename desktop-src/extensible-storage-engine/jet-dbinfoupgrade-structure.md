---
description: 深入瞭解： JET_DBINFOUPGRADE 結構
title: JET_DBINFOUPGRADE 結構
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966707"
---
# <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE 結構

**JET_DBINFOUPGRADE** 結構會保存資料庫升級狀態的相關資訊。 只有當 **JET_DBINFOUPGRADE** 已傳遞至 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) 或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)時，才會抓取此值。 資料庫引擎目前的作業系統版本不需要此結構。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>成員

**cbStruct**

設定為 **JET_DBINFOUPGRADE** 結構的大小（以位元組為單位）。

**cbFilesizeLow**

可反映資料庫目前檔案大小的低 **DWORD** 。

**cbFilesizeHigh**

會反映資料庫目前檔案大小的高 **DWORD** 。

**cbFreeSpaceRequiredLow**

就地升級所需之估計可用磁碟空間的低 **DWORD** 。

**cbFreeSpaceRequiredHigh**

就地升級所需之估計可用磁碟空間的高 **DWORD** 。

**csecToUpgrade**

升級所需的預估時間（以秒為單位）。

**ulFlags**

由零或多個下列旗標所組成的位欄位： **fUpgradable**、 **fAlreadyUpgraded**。

**fUpgradable**

資料庫可升級。

**fAlreadyUpgraded**

資料庫會升級為目前的資料庫格式。

### <a name="remarks"></a>備註

[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)或 [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)的呼叫會填入 **JET_DBINFOUPGRADE** 結構。 如果函式不成功，則結構的內容是未定義的。

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
