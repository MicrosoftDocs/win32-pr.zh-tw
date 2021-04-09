---
description: 深入瞭解： ColumnValue 類別
title: ColumnValue 類別
TOCTitle: ColumnValue class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue(v=EXCHG.10)
ms:contentKeyID: 55101189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcc0f011882cfb1f834ef317332948ce194c8de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848335"
---
# <a name="columnvalue-class"></a>ColumnValue 類別

物件的基類，代表要設定的資料行值。

## <a name="inheritance-hierarchy"></a>繼承階層

[System.Object](/dotnet/api/system.object)  
  ColumnValue （.）  
    [BytesColumnValue （.）](./bytescolumnvalue-class.md)  
    [ColumnValueOfStruct （.）\<T\>](./columnvalueofstruct-t-class.md)  
    [StringColumnValue （.）](./stringcolumnvalue-class.md)  

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustInherit Class ColumnValue
'Usage
Dim instance As ColumnValue
```

``` csharp
public abstract class ColumnValue
```

## <a name="thread-safety"></a>執行緒安全

這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。 並非所有的執行個體成員都是安全執行緒。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[ColumnValue 成員](./columnvalue-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
