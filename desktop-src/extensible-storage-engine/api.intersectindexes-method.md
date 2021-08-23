---
description: 深入瞭解： IntersectIndexes 方法
title: IntersectIndexes 方法
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88bcc872fc557e3942a119845206661bd48705317163520924059af5456f6e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983678"
---
# <a name="apiintersectindexes-method"></a>IntersectIndexes 方法

交集一組索引範圍，並傳回在所有索引範圍中找到之記錄的書簽。 另請參閱[JetIntersectIndexes (JET_SESID、 \[ \] 、Int32、JET_RECORDLIST、IntersectIndexesGrbit) ](./api.jetintersectindexes-method.md)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableids  
    類型： \[\]  
    
    要使用的 tableids。 每個 tableid 都必須來自相同資料表上的不同索引，並具有使用中的索引範圍。 使用 [JetSetIndexRange (JET_SESID、JET_TABLEID、SetIndexRangeGrbit) ](./api.jetsetindexrange-method.md) 建立索引範圍。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<\[\]\>  
在所有索引範圍中找到之記錄的書簽。 書簽會以主要索引鍵順序傳回。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Api 類別](./api-class.md)

[Api 成員](./api-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
