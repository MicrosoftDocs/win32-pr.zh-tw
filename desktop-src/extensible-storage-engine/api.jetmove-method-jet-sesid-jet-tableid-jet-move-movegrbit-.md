---
description: '深入瞭解： JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) '
title: 'JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) '
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b7ea09ae36160fc83fbee4dc3b7f94222f55125b992039aa15035c1d958c696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117718716"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a>JetMove 方法 (JET_SESID、JET_TABLEID、JET_Move、MoveGrbit) 

流覽索引。 資料指標可放置在索引的開頭或結尾，並以指定的索引項目數目向前移動和轉寄。 另請參閱 [TryMoveFirst (JET_SESID、JET_TABLEID) ](./api.trymovefirst-method.md)、 [TryMoveLast (JET_SESID、JET_TABLEID) ](./api.trymovelast-method.md)、 [TryMoveNext (JET_SESID、JET_TABLEID) ](./api.trymovenext-method.md)、 [TryMovePrevious (JET_SESID JET_TABLEID) ](./api.trymoveprevious-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要用於呼叫的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要放置的游標。

<!-- end list -->

  - numRows  
    類型： [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)  
    
    位移，表示移動游標的距離。

<!-- end list -->

  - grbit  
    型別： [MoveGrbit](./movegrbit-enumeration.md) 。  
    
    移動選項。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[JetMove 多載](./api.jetmove-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
