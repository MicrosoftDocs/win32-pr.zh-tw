---
description: 深入瞭解： IndexInfo. IndexSegments 屬性
title: IndexInfo. IndexSegments 屬性
TOCTitle: 'IndexSegments property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.indexsegments(v=EXCHG.10)
ms:contentKeyID: 55103239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
- Microsoft.Isam.Esent.Interop.IndexInfo.get_IndexSegments
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 966386c8698c101616d6b0c9292344572da5a0db21d36a12c4173111e689f6ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117896078"
---
# <a name="indexinfoindexsegments-property"></a>IndexInfo. IndexSegments 屬性

取得索引的區段。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property IndexSegments As IList(Of IndexSegment)
    Get
'Usage
Dim instance As IndexInfo
Dim value As IList(Of IndexSegment)

value = instance.IndexSegments
```

``` csharp
public IList<IndexSegment> IndexSegments { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.collections.generic.ilist-1) 。\<[IndexSegment](./indexsegment-class.md)\>  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[IndexInfo 類別](./indexinfo-class.md)

[IndexInfo 成員](./indexinfo-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
