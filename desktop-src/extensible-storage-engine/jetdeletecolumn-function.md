---
description: 深入瞭解： JetDeleteColumn 函數
title: JetDeleteColumn 函式
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd20ba923157d50b3130250f4784ea9bfb19b9b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476444"
---
# <a name="jetdeletecolumn-function"></a>JetDeleteColumn 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdeletecolumn-function"></a>JetDeleteColumn 函式

**JetDeleteColumn** 函數會從 ESE 資料庫資料表中刪除資料行。

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

要從中刪除資料行的資料表。

*szColumnName*

要刪除的資料行名稱。

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

呼叫 **JetDeleteColumn** 等同于呼叫 [JetDeleteColumn2](./jetdeletecolumn2-function.md) ，並將 *grbit* 設定為零 (0) 。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDeleteColumnW</strong> (Unicode) 和 <strong>JetDeleteColumnA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
