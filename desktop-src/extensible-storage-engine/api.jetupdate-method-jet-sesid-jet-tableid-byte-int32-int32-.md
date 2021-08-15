---
description: '深入瞭解： JetUpdate 方法 (JET_SESID、JET_TABLEID、位元組、Int32、Int32) '
title: 'JetUpdate 方法 (JET_SESID、JET_TABLEID、Byte、Int32、Int32) '
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bf9130715d35fb26b226a2b378f0eba2a853b742ee0a88319ed35f3a121f480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902463"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>JetUpdate 方法 (JET_SESID、JET_TABLEID、Byte、Int32、Int32) 

JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。 藉由呼叫 [JetDelete (JET_SESID JET_TABLEID) ](./api.jetdelete-method.md)來執行刪除資料表資料列。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    啟動更新的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要更新的資料指標。 應備妥更新。

<!-- end list -->

  - 書籤 (bookmark)  
    類型： \[\]  
    
    傳回已更新之記錄的書簽。 這個可以是 null。

<!-- end list -->

  - bookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    書簽緩衝區的大小。

<!-- end list -->

  - actualBookmarkSize  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回書簽的實際大小。

## <a name="remarks"></a>備註

JetUpdate 是執行插入或更新的最後一個步驟。 更新的開始方式是呼叫[JetPrepareUpdate (JET_SESID、JET_TABLEID、JET_prep) ](./api.jetprepareupdate-method.md) ，然後藉由呼叫[JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、Int32、SetColumnGrbit、JET_SETINFO) ](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md)一或多個時間來設定記錄狀態。 最後，會呼叫 JetUpdate (JET_SESID、JET_TABLEID、 \[ \] 、Int32、int32) ，以完成更新作業。 只有 JetUpdate 或而不是在 JetSetColumn 期間更新索引。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetUpdate 多載](./api.jetupdate-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
