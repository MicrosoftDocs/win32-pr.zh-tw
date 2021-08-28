---
description: 深入瞭解： JetCloseTable 函數
title: JetCloseTable 函式
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 48082b4ecf80b0b9c8da8a70efcb2c0cde1ff90a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482884"
---
# <a name="jetclosetable-function"></a>JetCloseTable 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetclosetable-function"></a>JetCloseTable 函式

**JetCloseTable** 函式會在資料庫中關閉開啟的資料表。 資料表可以是臨時表或一般資料表。

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>參數

*sesid*

識別將用於 API 呼叫的資料庫會話內容。

*tableid*

識別要關閉的資料表。

將 *tableid* 設定為 JET_tableidNil 釋放記憶體。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 



#### <a name="remarks"></a>備註

您必須在以 [JetOpenTable](./jetopentable-function.md)開啟的所有資料表上呼叫此函數。

在交易中呼叫 [JetOpenTable](./jetopentable-function.md) 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。 回復交易時，資料表會自動關閉。 在此情況下，使用 **JetCloseTable** 關閉資料表是錯誤的。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)
