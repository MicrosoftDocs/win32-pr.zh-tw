---
description: 深入瞭解： ColumnValueOfStruct <T> 類別
title: ColumnValueOfStruct (T) 類別
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321412"
---
# <a name="columnvalueofstructt-class"></a>ColumnValueOfStruct \<T\> 類別

設定結構類型的資料行 (例如 Int32/Guid) 。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [ColumnValue （.）](./columnvalue-class.md)  
    ColumnValueOfStruct （.）\<T\>  
      

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>型別參數

  - T  
    要設定的類型。

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValueOfStruct \<T\> 成員](./columnvalueofstruct-t-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>衍生類型

[System.Object](/dotnet/api/system.object)  
  [ColumnValue （.）](./columnvalue-class.md)  
    ColumnValueOfStruct （.）\<T\>  
      [BoolColumnValue （.）](./boolcolumnvalue-class.md)  
      [ByteColumnValue （.）](./bytecolumnvalue-class.md)  
      [DateTimeColumnValue （.）](./datetimecolumnvalue-class.md)  
      [DoubleColumnValue （.）](./doublecolumnvalue-class.md)  
      [FloatColumnValue （.）](./floatcolumnvalue-class.md)  
      [GuidColumnValue （.）](./guidcolumnvalue-class.md)  
      [Int16ColumnValue （.）](./int16columnvalue-class.md)  
      [Int32ColumnValue （.）](./int32columnvalue-class.md)  
      [Int64ColumnValue （.）](./int64columnvalue-class.md)  
      [UInt16ColumnValue （.）](./uint16columnvalue-class.md)  
      [UInt32ColumnValue （.）](./uint32columnvalue-class.md)  
      [UInt64ColumnValue （.）](./uint64columnvalue-class.md)