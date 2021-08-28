---
description: 深入瞭解： JetDeleteColumn2 函數
title: JetDeleteColumn2 函式
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2e74c507483791f3090b43e436e01ce7b5173e0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984961"
---
# <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdeletecolumn2-function"></a>JetDeleteColumn2 函式

**JetDeleteColumn2** 函式會從 ESE 資料庫資料表中刪除資料行，並啟用 *grbit* 選項的設定。

**Windows xp： JetDeleteColumn2** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

包含要刪除之資料行的資料表。

*szColumnName*

要刪除的資料行名稱。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>設定 JET_bitDeleteColumIgnoreTemplateColumns 將導致 API 只會嘗試刪除衍生資料表中的資料行。 如果基表中有該名稱的資料行，則會忽略該名稱的資料行。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errColumnInUse</p> | <p>資料行目前正在使用中。 索引目前可能會使用它。</p> | 
| <p>JET_errFixedDDL</p> | <p>嘗試修改固定的 DDL。</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>在 <em>szColumnName</em> 中名為的資料行存在於樣板資料表中，且無法修改範本資料表的 DDL。</p> | 
| <p>JET_errInvalidName</p> | <p>如果指定了 <em>szColumnName</em> 的錯誤名稱，則可能會傳回此錯誤。</p> | 
| <p>JET_errPermissionDenied</p> | <p>資料表無法寫入。 如果資料庫是以唯讀模式開啟，可能會傳回此情況。</p> | 
| <p>JET_errTransReadOnly</p> | <p>交易是唯讀交易。</p> | 



#### <a name="remarks"></a>備註

呼叫 [JetDeleteColumn](./jetdeletecolumn-function.md) 等同于呼叫 **JetDeleteColumn2** ，並將 *grbit* 設定為零 (0) 。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDeleteColumn2W</strong> (Unicode) 和 <strong>JetDeleteColumn2A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
