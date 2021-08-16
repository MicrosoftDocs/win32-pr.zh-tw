---
description: 深入瞭解： JET_INSTANCE_INFO 結構
title: JET_INSTANCE_INFO 結構
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d6f561c3c630f5a0509e8ce46bd3a7b6404750d33b9c450ca15a2328c4f110f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890568"
---
# <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_instance_info-structure"></a>JET_INSTANCE_INFO 結構

當搭配 [JetGetInstanceInfo](./jetgetinstanceinfo-function.md)和 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)函數使用時， **JET_INSTANCE_INFO** 結構會接收有關執行中資料庫實例的資訊。

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>成員

**hInstanceId**

給定實例的 [JET_INSTANCE](./jet-instance.md) 。

**szInstanceName**

資料庫執行個體的名稱。 如果實例沒有名稱，這個值可以是 **Null** 。

**cDatabases**

附加至資料庫實例的資料庫數目。 **cDatabases** 也會保留 **szDatabaseFileName**、 **szDatabaseDisplayName** 和 **szDatabaseSLVFileName** 中所傳回之字串陣列的大小。

**szDatabaseFileName**

字串的陣列，每個字串都包含附加至資料庫實例的資料庫檔案名。 陣列具有 **cDatabases** 元素。

**szDatabaseDisplayName**

字串的陣列，每個字串都會保存資料庫的顯示名稱。 字串目前可以是 Null。 陣列具有 **cDatabases** 元素。

**szDatabaseSLVFileName**

字串的陣列，每個字串都包含附加至資料庫實例之 SLV 檔的檔案名。 陣列具有 **cDatabases** 元素。 不支援 SLV 檔案，因此應忽略此欄位。

### <a name="remarks"></a>備註

每個資料庫實例都可以有多個附加的資料庫。

針對給定的 **JET_INSTANCE_INFO** 結構，針對資料庫所傳回的字串陣列會採用相同的順序。 例如，"szDatabaseDisplayName \[ i \] " 和 "szDatabaseFileName \[ i \] " 都會參考相同的資料庫。

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
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_INSTANCE_INFO_W</strong> (Unicode) 和 <strong>JET_INSTANCE_INFO _A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)
