---
description: 深入瞭解： UInt32ColumnValue 類別
title: UInt32ColumnValue 類別
TOCTitle: UInt32ColumnValue class
ms:assetid: T:Microsoft.Isam.Esent.Interop.UInt32ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint32columnvalue(v=EXCHG.10)
ms:contentKeyID: 55104174
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7511cf3d449002e9fed069fdb721dc3e4cc4b28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851928"
---
# <a name="uint32columnvalue-class"></a>UInt32ColumnValue 類別

[UInt32](/dotnet/api/system.uint32)資料行值。

此 API 不符合 CLS 規範。 

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  [ColumnValue （.）](./columnvalue-class.md)  
    [ColumnValueOfStruct （.）](./columnvalueofstruct-t-class.md)\<[UInt32](/dotnet/api/system.uint32)\>  
      UInt32ColumnValue （.）  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Class UInt32ColumnValue _
    Inherits ColumnValueOfStruct(Of UInteger)
'Usage
Dim instance As UInt32ColumnValue
```

``` csharp
[CLSCompliantAttribute(false)]
public class UInt32ColumnValue : ColumnValueOfStruct<uint>
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[UInt32ColumnValue 成員](./uint32columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
