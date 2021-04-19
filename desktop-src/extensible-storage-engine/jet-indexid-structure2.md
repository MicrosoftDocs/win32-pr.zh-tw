---
description: 深入瞭解： JET_INDEXID 結構
title: JET_INDEXID 結構
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975918"
---
# <a name="jet_indexid-structure"></a>JET_INDEXID 結構

保存索引識別碼。 索引識別碼是用來加速使用 JetSetCurrentIndex 來選取目前索引的提示。 當資料表的索引數量非常龐大時，最有用。 您可以使用 JetGetIndexInfo 或 JetGetTableIndexInfo 來取出索引識別碼。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a>備註

因為 c + + 版本定義為位元組陣列，所以需要 Pack 屬性。 如果 C \# 編譯器在 Uint cbStruct 和 IntPtr 之間插入一般的填補，則結構最後會太大。

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXID 成員](./jet-indexid-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
