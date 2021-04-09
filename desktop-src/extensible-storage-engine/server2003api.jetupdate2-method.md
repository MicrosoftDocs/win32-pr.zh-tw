---
description: 深入瞭解： Server2003Api. JetUpdate2 方法
title: 'Server2003Api. JetUpdate2 方法 (Server2003 的) '
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112040"
---
# <a name="server2003apijetupdate2-method"></a>Server2003Api. JetUpdate2 方法

JetUpdate 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。 藉由呼叫 [JetDelete (JET_SESID JET_TABLEID) ](./api.jetdelete-method.md)來執行刪除資料表資料列。

**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
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

<!-- end list -->

  - grbit  
    型別： [Server2003. UpdateGrbit](./updategrbit-enumeration.md)  
    
    更新選項。

## <a name="remarks"></a>備註

JetUpdate 是執行插入或更新的最後一個步驟。 更新的開始方式是呼叫[JetPrepareUpdate (JET_SESID、JET_TABLEID、JET_prep) ](./api.jetprepareupdate-method.md) ，然後藉由呼叫[JetSetColumn (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、Int32、SetColumnGrbit、JET_SETINFO) ](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md)一或多個時間來設定記錄狀態。 最後，會呼叫 JetUpdate2 (JET_SESID、JET_TABLEID、 \[ \] 、Int32、Int32、UpdateGrbit) ，以完成更新作業。 只有 JetUpdate 或而不是在 JetSetColumn 期間更新索引。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Api 類別](./server2003api-class.md)

[Server2003Api 成員](./server2003api-members.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
