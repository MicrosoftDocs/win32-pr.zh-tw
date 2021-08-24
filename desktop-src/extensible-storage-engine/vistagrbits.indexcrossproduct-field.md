---
description: 深入瞭解： VistaGrbits. IndexCrossProduct 欄位
title: VistaGrbits. IndexCrossProduct 欄位)  (的欄位
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3828411177d1c500c1b21b62797f093143ba1ac5b9770d9d6444d5c1a7aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471128"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>VistaGrbits. IndexCrossProduct 欄位

針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。 否則，索引在最重要的索引鍵資料行中的每個多重值都只會有一個專案，這是多重值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值（多重值資料行）。 例如，如果您在資料行 A 上針對具有值 "1" 和 "2" 的資料行 A 指定此旗標，則會建立下列索引項目： "red"、"1"、"red"、"2"、"blue"、"1"、"blue"、"2"。 否則，將會建立下列索引項目： "red"、"1"、"blue"、"1"。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaGrbits 類別](./vistagrbits-class.md)

[VistaGrbits 成員](./vistagrbits-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
