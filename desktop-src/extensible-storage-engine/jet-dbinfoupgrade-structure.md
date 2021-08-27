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
ms.openlocfilehash: 57c9265f45412bd31e087a52ab2b923c9c55c430
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467655"
---
# <a name="jet_dbinfoupgrade-structure"></a>JET_DBINFOUPGRADE 結構


_**適用于：** Windows |Windows伺服器_

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


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
