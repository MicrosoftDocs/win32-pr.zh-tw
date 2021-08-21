---
description: 深入瞭解： ColumnValue. ValueAsObject 屬性
title: ColumnValue. ValueAsObject 屬性
TOCTitle: 'ValueAsObject property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.valueasobject(v=EXCHG.10)
ms:contentKeyID: 55101198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_ValueAsObject
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7b5117f75fb195fe065493d942cee6c244f56eed1fe6170bdd53fd243143d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083651"
---
# <a name="columnvaluevalueasobject-property"></a>ColumnValue. ValueAsObject 屬性

取得資料行的最後一個設定或抓取值。 此值會以泛型物件的形式傳回。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustOverride ReadOnly Property ValueAsObject As Object
    Get
'Usage
Dim instance As ColumnValue
Dim value As Object

value = instance.ValueAsObject
```

``` csharp
public abstract Object ValueAsObject { get; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.object)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValue 類別](./columnvalue-class.md)

[ColumnValue 成員](./columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
