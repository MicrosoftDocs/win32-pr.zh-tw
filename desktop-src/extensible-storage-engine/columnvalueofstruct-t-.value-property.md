---
description: 深入瞭解： ColumnValueOfStruct <T> 。Value 屬性
title: ColumnValueOfStruct (T) 。Value 屬性
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Value
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334180(v=EXCHG.10)
ms:contentKeyID: 55100978
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.Value
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.set_Value
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef726e8926cd1887b79e4504adbccffcff1bed63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691363"
---
# <a name="columnvalueofstructtvalue-property"></a>ColumnValueOfStruct \<T\> 。Value 屬性

取得或設定結構中的值。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property Value As Nullable(Of T)
    Get
    Set
'Usage
Dim instance As ColumnValueOfStruct
Dim value As Nullable(Of T)

value = instance.Value

instance.Value = value
```

``` csharp
public Nullable<T> Value { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [可為 null](/dotnet/api/system.nullable-1)\<[T](./columnvalueofstruct-t-class.md)\>  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValueOfStruct \<T\> 類別](./columnvalueofstruct-t-class.md)

[ColumnValueOfStruct \<T\> 成員](./columnvalueofstruct-t-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
