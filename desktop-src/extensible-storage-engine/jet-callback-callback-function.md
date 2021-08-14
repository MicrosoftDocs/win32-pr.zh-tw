---
description: 深入瞭解： JET_CALLBACK 回呼函數
title: JET_CALLBACK 回呼函數
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: d50f0f3a0908b725d7f704df962324a0f16af1fc6f7353515a8d604e87edd0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487611"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK 回呼函數


_**適用于：** Windows |Windows伺服器_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK 回呼函數

**JET_CALLBACK** 函式是一種多用途的回呼函式，由資料庫引擎用來通知應用程式涉及線上磁碟重組和資料指標狀態通知。

請參閱 [JET_CBTYP](./jet-cbtyp.md) ，以取得此函式的參數所使用的特定設定，因為這些設定會根據在 *CBTYP* 參數中選取要使用的 **JET_CBTYP** 選項而有所不同。

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>參數

*sesid*

正在進行回呼的會話。

*dbid*

正在進行回呼的資料庫。

*tableid*

正在進行回呼的資料指標。

*cbtyp*

執行回呼的作業中的點。 請參閱 [JET_CBTYP](./jet-cbtyp.md) ，以取得值清單和每個案例中下列參數的意義。

*pvArg1*

用來與使用回呼的應用程式通訊的參數。 如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。

*pvArg2*

用來與使用回呼的應用程式通訊的參數。 如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。

*pvCoNtext*

用來與使用回呼的應用程式通訊的參數。 如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。

*ulUnused*

用來與使用回呼的應用程式通訊的參數。 如需有關此參數的使用方式，請參閱 database engine 所支援的每個回呼的詳細資訊 [JET_CBTYP](./jet-cbtyp.md) 。

#### <a name="return-value"></a>傳回值

函數會傳回其中一個[可擴充的儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)。 如需如何將這些程式碼傳回為 Hresult 的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)。 成功時，發出回呼的作業可以正常執行。 在某些情況下，回呼可能會傳回會影響該作業的警告。 如需作業使用這些警告的詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md) 。

失敗時，發出回呼的作業可能會正常進行，或可能會失敗。 如需作業使用錯誤碼的詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md) 。

#### <a name="remarks"></a>備註

如果回呼將資料指標傳遞至應用程式，請務必知道此資料指標刻意限制為較小的一組功能，以避免遞迴和其他 ugliness。 允許下列作業：

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

當您設計回呼時，請考慮即使有這些限制，回呼仍可能失敗。

#### <a name="requirements"></a>規格需求

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
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
